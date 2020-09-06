# Savodxon dasturi imkoniyatlarini boshqa saytga joriy qilish

Ushbu repoda siz Savodxon imlo dasturi tahrir oynasini oʻz saytingiz tahrir sahifasiga integratsiya qilish usuli koʻrsatilgan.

mijoz.html faylida integratsiyaning eng oddiy koʻrinishi misol tariqasida keltirilgan.

### Foydalanishga misol

Sizning saytingizda tahrir oynasi bor (masalan, TinyMCE yoki CKEditor). Saytingiz foydalanuvchilari yoki tahrirchilariga saytning oʻzida turib matnni tahrirlash va imlo xatolariga tekshirish imkonini yaratmoqchisiz. Yaʼni, foydalanuvchilaringiz matnni nusxalab, Savodxon dasturiga tashlab, tekshirib, keyin yana nusxalab saytingizga kiritishlariga chek qoʻymoqchisiz.

Buning uchun saytingizning tahrir oynasi joylashgan sahifasida popup yarating. Bu popup ichiga “https://savodxon.uz/iframe.php” manbayi bilan 

Tahrir oynasining oʻzingiz istagan joyiga maxsus tugma joylang. Foydalanuvchi bu tugmani bosganda, popup oyna ochilib, tahrir oynasining HTML kodi nusxalab olinib, iframe ichiga postMassege yordamida uzatiladigan funksiya yozing (shunday funksiya misoli mijoz.html faylida keltirilgan).

Etibor bering — maʼlumot quyidagi formatda yuborilishi kerak:
<pre>var data = {type: 'postText', value: "Tahrir oynasi HTML kodi", alphabet: "lat|cyr"};</pre>

https://savodxon.uz/iframe.php sahifasidagi script aynan shunday strukturadagi maʼlumotni qabul qiladi va “postText” turdagi HTML kodni Savodxon tahrir oynasiga joylab beradi. Natijada, foydalanuvchi shu yerning oʻzida matn ustida ishlashi mumkin.

Ishni yakunlagandan soʻng, foydalanuvchi tahrir oynasi ostida chap burchakda joylashgan “Tatbiq qilish” tugmasini bosadi. Bu tugma bosilganda, iframe ichidagi script ishlov berilgan matnni HTML kod sifatida nusxalab olib, yuqori (parent) sahifaga (yaʼni sizning saytingiz sahifasiga) uzatadi. Sizning sahifangizda mana shunday murojaatni qabul qilib olib, undan kelgan HTML kodni saytingizdagi tahrir oynasiga joylaydigan va popupni yopadigan funksiya boʻlishi kerak (shunday funksiyaga misol mijoz.html faylida keltirilgan).

Eʼtibor bering — ushbu funksiya ishlashi uchun, saytingiz foydalanuvchisining Savodxon saytida hisobi va faol obunasi boʻlishi kerak. Shuningdek, foydalanuvchi oʻzi ishlayotgan brauzerda Savodxon saytiga kirgan (login qilgan) boʻlishi lozim.
