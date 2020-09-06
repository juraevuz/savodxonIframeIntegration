# Savodxon dasturi imkoniyatlarini boshqa saytga joriy qilish
Ushbu repoda siz Savodxon imlo dasturi tahrir oynasini o'z saytingiz tahrir sahifasiga integratsiya qilish usuli ko'rsatilgan.

mijoz.html faylida integratsiyaning eng oddiy ko'rinishi misol tariqasida keltirilgan.

### Ishlash prinsipi
Sizning saytingizda tahrir oynasi bor (masalan, TinyMCE yoki CKEditor). Saytingiz foydalanuvchilari yoki tahrirchilariga saytning o'zida turib matnni tahrirlash va imlo xatolariga tekshirish imkonini yaratmoqchisiz. Ya'ni, foydalanuvchilaringiz matnni nusxalab, Savodxon dasturiga tashlab, tekshirib, keyin yana nusxalab saytingizga kiritishlariga chek qo'ymoqchisiz.

Buning saytingizning tahrir oynasi joylashgan sahifasida popup yarating. Bu popup ichiga <iframe> element joylang. Tahrir oynasining o'zingiz istagan joyiga maxsus tugma joylang. Foydalanuvchi bu tugmani bosganda, popup oyna ochilib, tahrir oynasining HTML kodi nusxalab olinib, iframe ichiga postMassege yordamida uzatiladigan funskiya yozing (shunday funksiya musoli mijoz.html faylida keltirilgan).
  
Etribor bering, ma'lumot quyidagi formatda yuborilishi kerak:
var data = {type: 'postText', value: "Tahrir oynasi HTML kodi"};

