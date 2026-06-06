# Hidmat Waitlist — Sozlash qo'llanmasi

Landing page tayyor va ishlaydi. Yozilishlar (email + telefon) **Google Sheets**ga tushishi uchun quyidagi 4 qadamni bajaring. Bu butunlay bepul va 5 daqiqa vaqt oladi.

> Hozir sahifa **test rejim**da: forma ishlaydi, lekin yozuvlar faqat brauzerda saqlanadi. Pastdagi qadamlar bajarilgach, yozuvlar to'g'ridan-to'g'ri Google jadvalingizga tushadi.

---

## 1-qadam — Google Sheets jadval yaratish

1. [sheets.google.com](https://sheets.google.com) ga kiring va yangi bo'sh jadval oching.
2. Birinchi qatorga ustun nomlarini yozing (aynan shu tartibda):

   | A | B | C | D | E | F | G | H |
   |-----------|------|-----------|-----------|--------|-------|---------|--------|
   | timestamp | role | firstName | lastName | fields | email | contact | source |

   (`role` — xizmat sotib oluvchi yoki sotuvchi; `fields` — tanlangan soha(lar), vergul bilan; `contact` — telefon yoki Telegram username)

3. Jadvalga nom bering, masalan `Hidmat Waitlist`.

---

## 2-qadam — Apps Script qo'shish

1. Jadvalda yuqoridagi menyudan **Extensions → Apps Script** ni bosing.
2. Ochilgan oynadagi barcha kodni o'chirib, quyidagini joylashtiring:

```javascript
function doPost(e) {
  try {
    var sheet = SpreadsheetApp.getActiveSpreadsheet().getSheets()[0];
    var data = JSON.parse(e.postData.contents);
    sheet.appendRow([
      data.timestamp || new Date().toISOString(),
      data.role || "",
      data.firstName || "",
      data.lastName || "",
      data.fields || "",
      data.email || "",
      data.contact || "",
      data.source || ""
    ]);
    return ContentService
      .createTextOutput(JSON.stringify({ result: "success" }))
      .setMimeType(ContentService.MimeType.JSON);
  } catch (err) {
    return ContentService
      .createTextOutput(JSON.stringify({ result: "error", message: err.toString() }))
      .setMimeType(ContentService.MimeType.JSON);
  }
}
```

3. Yuqoridagi disk (💾) belgisini bosib saqlang.

---

## 3-qadam — Web app sifatida nashr qilish (Deploy)

1. O'ng yuqoridagi **Deploy → New deployment** tugmasini bosing.
2. **Select type** (tishli g'ildirak belgisi) → **Web app** ni tanlang.
3. Sozlamalar:
   - **Description**: `Hidmat waitlist`
   - **Execute as**: `Me` (o'zingiz)
   - **Who has access**: `Anyone` ← **muhim**, aks holda forma yuborilmaydi.
4. **Deploy** ni bosing. Google ruxsat so'raydi — hisobingizni tanlab, **Allow** bering.
   - "Google hasn't verified this app" chiqsa: **Advanced → Go to ... (unsafe)** → **Allow**. Bu o'zingizning skriptingiz, xavfsiz.
5. Chiqqan **Web app URL** ni nusxalang. U shunday ko'rinadi:
   `https://script.google.com/macros/s/AKfyc..../exec`

---

## 4-qadam — URL ni sahifaga qo'yish

1. `code.html` (va `index.html`) faylini oching.
2. Skript bo'limidagi shu qatorni toping (taxminan oxirida):

   ```javascript
   const WAITLIST_ENDPOINT = "";
   ```

3. Tirnoq ichiga nusxalagan URL ni qo'ying:

   ```javascript
   const WAITLIST_ENDPOINT = "https://script.google.com/macros/s/AKfyc..../exec";
   ```

4. Saqlang. Tamom! Endi har bir yozilish Google jadvalingizga avtomatik tushadi.

> **Eslatma:** `code.html` va `index.html` bir xil. Saytni internetga joylashda `index.html` ishlatiladi. URL ni **ikkala faylga ham** qo'ying yoki bittasini o'chirib tashlang.

---

## Tekshirish

1. Faylni brauzerda oching, formaga test email kiriting va **Yuborish** ni bosing.
2. "Rahmat! Siz navbatga muvaffaqiyatli yozildingiz ✓" chiqishi kerak.
3. Google jadvalga qaytib, yangi qator paydo bo'lganini tekshiring.

---

## Saytni internetga qo'yish (ixtiyoriy)

Eng oson bepul variantlar — `index.html` faylli papkani shu saytlardan biriga tortib tashlang:

- **Netlify Drop** — [app.netlify.com/drop](https://app.netlify.com/drop)
- **Vercel** — [vercel.com](https://vercel.com)
- **GitHub Pages** — repozitoriyaga yuklab, Pages'ni yoqing.

Domen ulagandan keyin ham `WAITLIST_ENDPOINT` o'zgarmaydi — ishlayveradi.
