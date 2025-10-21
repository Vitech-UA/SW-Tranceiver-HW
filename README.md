# 📡 Матеріали по збірці КВ трансивера **STEP II**

## 🖼️ Фото процесу збірки

| Вид | Зображення |
|-----|-------------|
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
Фото стенду наведено нижче.

| Діапазон | Графік АЧХ |
|-----------|------------|
| **10 м** | ![10M Filter](https://github.com/Vitech-UA/SW-Tranceiver-HW/blob/main/MEDIA/TEST_IN_FILTER/10M.png) |
| **20 м** | ![20M Filter](https://github.com/Vitech-UA/SW-Tranceiver-HW/blob/main/MEDIA/TEST_IN_FILTER/20M.png) |
| **40 м** | ![40M Filter](https://github.com/Vitech-UA/SW-Tranceiver-HW/blob/main/MEDIA/TEST_IN_FILTER/40M.png) |
| **160 м** | ![160M Filter](https://github.com/Vitech-UA/SW-Tranceiver-HW/blob/main/MEDIA/TEST_IN_FILTER/160M.png) |

---

## 📊 Результати вимірювань АЧХ смугових фільтрів

Вимірювання виконані у режимі **S21 (Transmission)** на аналізаторі **LibreVNA**.  
Нижче наведено основні параметри для кожного діапазону: центральна частота, рівень втрат у смузі та частоти зрізу (−3 дБ).

| Діапазон | Центральна частота | Рівень у смузі (≈) | Частоти −3 дБ |
|:----------|:------------------:|:-------------------:|:----------------|
| **160 м** | 1.99 МГц | −3.6 дБ | 1.83 МГц / 2.14 МГц |
| **40 м**  | 7.00 МГц | −4.5 дБ | 6.61 МГц / 7.31 МГц |
| **20 м**  | 14.57 МГц | −4.7 дБ | 13.55 МГц / 15.58 МГц |
| **10 м**  | 28.06 МГц | −9.0 дБ | 26.27 МГц / 29.78 МГц |

---

### 🔬 Аналіз результатів

- Усі фільтри демонструють симетричну частотну характеристику з рівнем втрат у смузі 4–9 дБ.  
- Частоти зрізу відповідають стандартним межам КВ-діапазонів  
  🔗 [Діапазони радіоаматорів України](https://vrl.org.ua/index.php?option=com_content&view=article&id=129&Itemid=1143).  
- Придушення позасмугових складових перевищує −30 дБ, що забезпечує ефективне відсікання гармонік і взаємних перешкод.  
- Вимірювання виконано після калібрування комплекту LibreVNA за допомогою стандартного **SMA Open-Short-Load набору**.

---

## 🔧 Перевірка атенюатора та підсилювача (на прикладі діапазону 40 м)

| Етап перевірки | Зображення |
|----------------|-------------|
| **АЧХ фільтра + атенюатор** | ![40M+ATT](https://github.com/Vitech-UA/SW-Tranceiver-HW/blob/main/MEDIA/TEST_IN_FILTER/40M%2BATT.png) |
| **АЧХ фільтра + підсилювач** | ![40M+AMPL](https://github.com/Vitech-UA/SW-Tranceiver-HW/blob/main/MEDIA/TEST_IN_FILTER/40M%2BAMPL.png) |

**Висновки:**
- Вбудований підсилювач підвищує рівень сигналу приблизно на **+8.5 дБ**.  
- Вбудований атенюатор ослаблює сигнал на **−20 дБ**.  

---

## 🧰 Фото стенду тестування

![Test Stand](https://github.com/Vitech-UA/SW-Tranceiver-HW/blob/main/MEDIA/TEST_IN_FILTER/TEST_STAND.jpg)

**Використане обладнання:**  
🔹 [LibreVNA – проект на GitHub](https://github.com/jankae/LibreVNA)

---

## 📖 Документація та підтримка

- **Стаття на сайті автора про основну плату:**  
  📰 [us5msq.com.ua – STEP II: основна плата](https://us5msq.com.ua/kv-transiver-step-ii-osnovnaya-plata/)

- **Обговорення на форумі:**  
  💬 [us5msq.com.ua – Форум по STEP II](https://us5msq.com.ua/forum/viewtopic.php?f=23&t=254)
