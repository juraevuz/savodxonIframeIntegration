# Savodxon dasturi imkoniyatlarini boshqa saytga joriy qilish
Ushbu repoda siz Savodxon imlo dasturi tahrir oynasini o'z saytingiz tahrir sahifasiga integratsiya qilish usuli ko'rsatilgan.

mijoz.html faylida integratsiyaning eng oddiy ko'rinishi misol tariqasida keltirilgan.

### Foydalanishga misol
Sizning saytingizda tahrir oynasi bor (masalan, TinyMCE yoki CKEditor). Saytingiz foydalanuvchilari yoki tahrirchilariga saytning o'zida turib matnni tahrirlash va imlo xatolariga tekshirish imkonini yaratmoqchisiz. Ya'ni, foydalanuvchilaringiz matnni nusxalab, Savodxon dasturiga tashlab, tekshirib, keyin yana nusxalab saytingizga kiritishlariga chek qo'ymoqchisiz.

Buning uchun saytingizning tahrir oynasi joylashgan sahifasida popup yarating. Bu popup ichiga "https://savodxon.uz/iframe.php" manbayi bilan <iframe> element joylang. E'tibor bering - iframe balandligi 372px dan kichik bo'lmasligi kerak.
  
Tahrir oynasining o'zingiz istagan joyiga maxsus tugma joylang. Foydalanuvchi bu tugmani bosganda, popup oyna ochilib, tahrir oynasining HTML kodi nusxalab olinib, iframe ichiga postMassege yordamida uzatiladigan funskiya yozing (shunday funksiya musoli mijoz.html faylida keltirilgan).
  
Etribor bering - ma'lumot quyidagi formatda yuborilishi kerak:
<pre>var data = {type: 'postText', value: "Tahrir oynasi HTML kodi", alphabet: "lat|cyr"};</pre>

https://savodxon.uz/iframe.php sahifasidagi script aynan shunday strukturadagi ma'lumotni qabul qiladi va  "postText" turdagi HTML kodni Savodxon tahrir oynasiga joylab beradi. Natijada, foydalanuvchi shu yerning o'zida matn ustida ishlashi mumkin.

Ishni yakunlagandan so'ng, foydalanuvchi tahrir oynasi ostida chap burchakda joylashgan "Tatbiq qilish" tugmasini bosadi. Bu tugma bosilganda, iframe ichidagi script ishlov berilgan matnni HTML kod sifatida nusxalab olib, yuqori (parent) sahifaga (ya'ni sizning saytingiz sahifasiga) uzatadi. Sizning sahifangizda mana shunday murojaatni qabul qilib olib, undan kelgan HTML kodni saytingizdagi tahrir oynasiga joylaydigan va popupni yopadigan funskiya bo'lishi kerak (shunday funksiyaga misol mijoz.html faylida keltirilgan).

E'tibor bering - ushbu funskiya ishlashi uchun, saytingiz foydalanuvchisining Savodxon saytida hisobi va faol obunasi bo'lishi kerak. Shuningdek, foydalanuvchi o'zi ishlayotgan brauzerda Savodxon saytiga kirgan (login qilgan) bo'lishi lozim.
