# 📡 Матеріали по збірці КВ трансивера **STEP II**

## 🖼️ Фото процесу збірки

| Вид | Зображення |
|-----|------------|
| **Фронтальний вигляд** | ![Front view](https://github.com/Vitech-UA/SW-Tranceiver-HW/raw/main/MEDIA/Front.jpg) |
| **Процес монтажу (1)** | ![Assembly 1](https://github.com/Vitech-UA/SW-Tranceiver-HW/raw/main/MEDIA/photo_2025-10-07_23-35-20.jpg) |
| **Процес монтажу (2)** | ![Assembly 2](https://github.com/Vitech-UA/SW-Tranceiver-HW/raw/main/MEDIA/photo_2025-10-07_23-35-20%20(2).jpg) |

---

## ⚙️ Хард синтезатора

- **Схема та плата синтезатора**  
  📁 [SW-transceiver-controller-HW (GitHub)](https://github.com/Vitech-UA/SW-transceiver-controller-HW)

- **Прошивка STM32 для синтезатора**  
  💾 [SW-transceiver-controller-FW (GitHub)](https://github.com/Vitech-UA/SW-transceiver-controller-FW)

---

## 📈 Перевірка та налаштування вхідних смугових фільтрів

**Тестування проведено за допомогою векторного аналізатора LibreVNA.**  
Фото стенду нижче.

| Діапазон | Графік АЧХ |
|-----------|------------|
| **10 М** | ![10M Filter](https://github.com/Vitech-UA/SW-Tranceiver-HW/blob/main/MEDIA/TEST_IN_FILTER/10M.png) |
| **20 М** | ![20M Filter](https://github.com/Vitech-UA/SW-Tranceiver-HW/blob/main/MEDIA/TEST_IN_FILTER/20M.png) |
| **40 М** | ![40M Filter](https://github.com/Vitech-UA/SW-Tranceiver-HW/blob/main/MEDIA/TEST_IN_FILTER/40M.png) |
| **160 М** | ![160M Filter](https://github.com/Vitech-UA/SW-Tranceiver-HW/blob/main/MEDIA/TEST_IN_FILTER/160M.png) |

---

## 🔧 Перевірка атенюатора та підсилювача (на прикладі діапазону 40 М)

| Етап перевірки | Зображення |
|----------------|-------------|
| **АЧХ фільтра + атенюатор** | ![40M+ATT](https://github.com/Vitech-UA/SW-Tranceiver-HW/blob/main/MEDIA/TEST_IN_FILTER/40M%2BATT.png) |
| **АЧХ фільтра + підсилювач** | ![40M+AMPL](https://github.com/Vitech-UA/SW-Tranceiver-HW/blob/main/MEDIA/TEST_IN_FILTER/40M%2BAMPL.png) |

---

## 🧰 Фото стенду тестування

![Test Stand](https://github.com/Vitech-UA/SW-Tranceiver-HW/blob/main/MEDIA/TEST_IN_FILTER/TEST_STAND.jpg)

**Використане обладнання:**  
🔹 [LibreVNA – проєкт на GitHub](https://github.com/jankae/LibreVNA)

---

## 📖 Документація та підтримка

- **Стаття на сайті автора про основну плату**  
  📰 [us5msq.com.ua – STEP II: основна плата](https://us5msq.com.ua/kv-transiver-step-ii-osnovnaya-plata/)

- **Обговорення на форумі**  
  💬 [us5msq.com.ua – Форум по STEP II](https://us5msq.com.ua/forum/viewtopic.php?f=23&t=254)
