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

## 📈 Результати вимірювання АЧХ смугових фільтрів

Вимірювання виконані за допомогою **LibreVNA** у режимі **S21 (Transmission)**.  
Для кожного діапазону наведено центральну частоту, рівень втрат у смузі, частоти зрізу (−3 дБ) та ефективність придушення поза робочою смугою.

| Діапазон | Центр частоти | Рівень у смузі (≈) | Частоти −3 дБ |
|:----------|:---------------|:-------------------|:----------------|
| **160 м** | 1.99 МГц | −3.6 дБ | 1.83 МГц / 2.14 МГц |
| **40 м** | 7.00 МГц | −4.5 дБ | 6.61 МГц / 7.31 МГц |
| **20 м** | 14.57 МГц | −4.7 дБ | 13.55 МГц / 15.58 МГц |
| **10 м** | 28.06 МГц | −9 дБ | 26.27 МГц / 29.78 МГц |

---

### 🔬 Аналіз

- Усі фільтри демонструють симетричну характеристику з рівнем втрат у смузі 4–9 дБ.  
- Частоти зрізу відповідають стандартним межам КВ-діапазонів. (Про діапазони в Україні можна прочитати тут: https://vrl.org.ua/index.php?option=com_content&view=article&id=129&Itemid=1143) 
- Придушення позасмугових складових перевищує -30 дБ, що гарантує ефективне відсікання гармонік і взаємних перешкод.  
- Для вимірювань використовувався **LibreVNA** із калібруванням зі стандартного набору по **SMA-кабелях**.

---

**Графіки АЧХ:**  
| 160 м | 40 м | 20 м |
|:--:|:--:|:--:|
| ![160M](./160M.png) | ![40M](./40M.png) | ![20M](./20M.png) |

---

## 🔧 Перевірка атенюатора та підсилювача (на прикладі діапазону 40 М)

| Етап перевірки | Зображення |
|----------------|-------------|
| **АЧХ фільтра + атенюатор** | ![40M+ATT](https://github.com/Vitech-UA/SW-Tranceiver-HW/blob/main/MEDIA/TEST_IN_FILTER/40M%2BATT.png) |
| **АЧХ фільтра + підсилювач** | ![40M+AMPL](https://github.com/Vitech-UA/SW-Tranceiver-HW/blob/main/MEDIA/TEST_IN_FILTER/40M%2BAMPL.png) |
# Висновки:
- Вбудований підсилювач підсилює сигнал на величину ~8.5 dB
- Вбудований аттенюатор ослаблює сигнал на величину ~20 dB
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
