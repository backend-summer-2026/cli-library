# CLI Kutubxona

Python yordamida yaratiladigan sodda **CLI (Command Line Interface)** kutubxona dasturi.

Dastur orqali foydalanuvchi kitoblarni qo‘shishi, ko‘rishi, qidirishi va turli mezonlar bo‘yicha saralashi mumkin.

## Maqsad

Ushbu loyiha Python'da:

- `list` bilan ishlash;
- obyekt yoki ma'lumotlarni saqlash;
- `input()` orqali foydalanuvchidan ma'lumot olish;
- `if/elif/else` shart operatorlari;
- `while` sikli;
- funksiyalar;
- qidirish va oddiy hisob-kitoblar

bo‘yicha amaliy ko‘nikmalarni mustahkamlash uchun ishlab chiqiladi.

---

## Ma'lumotlar strukturasi

Dasturda barcha kitoblar **bitta `list`** ichida saqlanadi.

Har bir kitob quyidagi ma'lumotlardan iborat:

- **Muallif** — kitob muallifi
- **Nomi** — kitob nomi
- **Sahifalar soni** — kitobdagi sahifalar soni

Masalan, bitta kitob quyidagi ma'lumotlarni o‘z ichiga oladi:

> Muallif: Abdulla Qodiriy  
> Nomi: O'tkan kunlar  
> Sahifalar soni: 384

Barcha kitoblar esa bitta umumiy `kitoblar` ro‘yxida saqlanadi.

---

# Asosiy menyu

Dastur ishga tushganda foydalanuvchiga quyidagi menyu ko‘rsatilishi kerak:

```text
===== KUTUBXONA =====

1. Kitoblar ro'yxati
2. Kitob qo'shish
3. Eng ko'p sahifali kitob
4. Eng kam sahifali kitob
5. Muallif bo'yicha qidirish
6. Kitob nomi bo'yicha qidirish
7. Kitoblar sonini ko'rish
0. Chiqish

Tanlang:
```

Foydalanuvchi menyudan kerakli amalni tanlaydi.

Dastur foydalanuvchi **"0. Chiqish"** variantini tanlamaguncha ishlashda davom etadi.

---

## 1. Kitoblar ro'yxati

Ushbu bo'lim barcha mavjud kitoblarni ekranga chiqaradi.

Har bir kitob uchun:

- tartib raqami;
- muallif;
- kitob nomi;
- sahifalar soni

ko‘rsatilishi kerak.

Agar kutubxonada hali hech qanday kitob bo‘lmasa:

> Hozircha kitoblar mavjud emas.

degan xabar chiqarilsin.

---

## 2. Kitob qo'shish

Foydalanuvchidan quyidagi ma'lumotlar ketma-ket so‘raladi:

1. Muallif
2. Kitob nomi
3. Sahifalar soni

Kiritilgan ma'lumotlar asosida yangi kitob yaratiladi va **kitoblar ro‘yxatiga qo‘shiladi**.

Muvaffaqiyatli qo‘shilgandan so‘ng:

> Kitob muvaffaqiyatli qo'shildi.

degan xabar chiqarilsin.

### Validatsiya

Sahifalar soni:

- son bo‘lishi;
- 0 dan katta bo‘lishi

kerak.

Noto‘g‘ri qiymat kiritilsa, foydalanuvchiga xatolik haqida tushunarli xabar berilsin.

---

## 3. Eng ko'p sahifali kitob

Kutubxonadagi kitoblar orasidan **eng ko‘p sahifaga ega kitob** aniqlanadi.

Natijada ushbu kitobning:

- muallifi;
- nomi;
- sahifalar soni

ko‘rsatiladi.

Agar kitoblar mavjud bo‘lmasa:

> Hozircha kitoblar mavjud emas.

degan xabar chiqarilsin.

---

## 4. Eng kam sahifali kitob

Kutubxonadagi kitoblar orasidan **eng kam sahifaga ega kitob** aniqlanadi.

Natijada:

- muallif;
- kitob nomi;
- sahifalar soni

ko‘rsatiladi.

Agar kitoblar mavjud bo‘lmasa, foydalanuvchiga tegishli xabar chiqarilsin.

---

## 5. Muallif bo'yicha qidirish

Foydalanuvchidan muallif nomi so‘raladi.

Dastur kitoblar ro‘yxatidan shu muallifga tegishli kitoblarni qidiradi.

Bir nechta kitob topilishi mumkin.

Masalan:

```text
Muallif nomini kiriting: Abdulla Qodiriy

Natijalar:

1. O'tkan kunlar — 384 sahifa
2. Mehrobdan chayon — 320 sahifa
```

Agar hech qanday kitob topilmasa:

> Bu muallifga tegishli kitob topilmadi.

degan xabar chiqarilsin.

Qidiruvda katta-kichik harflarga bog‘liq bo‘lmaslik tavsiya etiladi.

---

## 6. Kitob nomi bo'yicha qidirish

Foydalanuvchidan kitob nomi yoki nomining bir qismi so‘raladi.

Dastur kitoblar ro‘yxidan mos keladigan kitoblarni qidiradi.

Masalan, foydalanuvchi:

> `O'tkan`

deb qidirsa, `O'tkan kunlar` kitobi topilishi kerak.

Natijada topilgan kitoblarning:

- muallifi;
- nomi;
- sahifalar soni

ko‘rsatiladi.

Agar mos kitob topilmasa:

> Bunday kitob topilmadi.

degan xabar chiqarilsin.

Qidiruv katta-kichik harflarga bog‘liq bo‘lmasligi kerak.

---

## 7. Kitoblar sonini ko'rish

Kutubxonadagi jami kitoblar soni ko‘rsatiladi.

Masalan:

```text
Kutubxonadagi kitoblar soni: 15
```

Agar hech qanday kitob bo‘lmasa:

```text
Kutubxonadagi kitoblar soni: 0
```

---

## 0. Chiqish

Foydalanuvchi `0` ni tanlaganda dastur to‘xtaydi.

Chiqishdan oldin:

> Dasturdan chiqildi. Xayr!

kabi xabar chiqarish mumkin.

---

# Muhim talablar

- Barcha kitoblar **bitta list** ichida saqlansin.
- Dastur faqat **CLI** orqali ishlasin.
- Ma'lumotlar dastur ishlayotgan vaqt davomida xotirada saqlanadi.
- Database yoki fayldan foydalanish shart emas.
- Dastur menyu asosida ishlashi kerak.
- Foydalanuvchi `0` ni tanlamaguncha menyu qayta-qayta ko‘rsatiladi.
- Noto‘g‘ri menyu tanlovi uchun xatolik xabari chiqarilsin.
- Bo‘sh kitoblar ro‘yxati bilan ishlash holati ham hisobga olinsin.
- Qidiruvlar foydalanuvchi uchun qulay bo‘lishi kerak.
- Kod funksiyalarga mantiqiy ajratilishi tavsiya etiladi.

# Kutilayotgan natija

Loyiha yakunida foydalanuvchi terminal orqali quyidagi ishlarni bajara olishi kerak:

- kitoblarni ko‘rish;
- yangi kitob qo‘shish;
- eng ko‘p sahifali kitobni topish;
- eng kam sahifali kitobni topish;
- muallif bo‘yicha qidirish;
- kitob nomi bo‘yicha qidirish;
- jami kitoblar sonini ko‘rish;
- dasturdan chiqish.

## Cheklov

Bu loyihaning birinchi versiyasida:

- database ishlatilmaydi;
- faylga yozish ishlatilmaydi;
- login/register tizimi bo‘lmaydi;
- kitobni o‘chirish yoki tahrirlash funksiyasi bo‘lmaydi.

Asosiy maqsad — **Python asoslari yordamida sodda, tushunarli va funksional CLI kutubxona dasturini yaratish**.
