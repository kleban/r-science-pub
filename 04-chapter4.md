# Читання та запис даних у R {#chapter4}


## План {-}

- [Загальний опис структури даних](#chapter41)
- [Опис набору даних `TelecomUsers`](#chapter42)
- [Імпорт даних засобами RStudio](#chapter43)
- [CSV: поняття, читання та запис](#chapter42)
- [XLSX: поняття, читання та запис](#chapter44)
- [JSON: поняття, читання та запис](#chapter45)
- [API: поняття, читання](#chapter46)
- [HTML: поняття, читання](#chapter47)
- [PDF: поняття, читання](#chapter48)
- [Сервіси Google](#chapter48)
  - [Spreadsheets](#chapter48)
  - [Keywords](#chapter48)

---

## Загальний опис структури даних {#chapter41}

<div class="alert alert-danger">
<i class="fa-2x fas fa-alert fa-battery-quarter"></i>
Матеріали розділу у процесі підготовки.
</div>

Усі дані, що використовуються для наукових досліджень можна розділити на 3 блоки:

- [x] Структуровані
- [x] Слабоструктуровані
- [x] Неструктуровані

**Структуровані дані** зазвичай зрозумілі для користувача, сформовані відповідно до певних вимог та дозволяють швидко їх вивчити, без додаткових процедур підготовки.

Важливою для нас характеристикою **структурованих даних** є те, що вони досить просто піддаються машинній обробці, аналізу та візуалізації.

**Слабоструктуровані дані** часто можуть бути сприйняті людиною, проте форма їх подачі не дозволяє швидко проаналізувати її машиною.

Найпростішим прикладом структурованих даних є табличні дані, наприклад, в Microsoft Excel, де кожен рядок - це одне спостереження, а кожен стовпець - це одна характеристика.

Слабоструктуровані дані можуть бути перетворені до структурованих за допомогою підготовлених спеціалістом з по роботі з дадними алгоритмом. Подібний етап зазвчай потребує детального аналізу полів, форми по дання, визначення шаблонів помилок у даних тощо.

**Неструктуровані дані**

## Опис набору даних `Telecom Users` {#chapter42}

<div class="alert alert-info">
Опис інформації про набір даних взято з сервісу [`kaggle.com`](https://kaggle.com).<br>
Оригінальний набір розміщений за адресою [`https://www.kaggle.com/radmirzosimov/telecom-users-dataset`](https://www.kaggle.com/radmirzosimov/telecom-users-dataset).
</div>

**Призначення**:

Описаний датасет призначений для практикування спеціалістами з машинного навчання розв'язування задач класифікації.

**Опис:**

Any business wants to maximize the number of customers. To achieve this goal, it is important not only to try to attract new ones, but also to retain existing ones. Retaining a client will cost the company less than attracting a new one. In addition, a new client may be weakly interested in business services and it will be difficult to work with him, while old clients already have the necessary data on interaction with the service.

Accordingly, predicting the churn, we can react in time and try to keep the client who wants to leave. Based on the data about the services that the client uses, we can make him a special offer, trying to change his decision to leave the operator. This will make the task of retention easier to implement than the task of attracting new users, about which we do not know anything yet.

You are provided with a dataset from a telecommunications company. The data contains information about almost six thousand users, their demographic characteristics, the services they use, the duration of using the operator's services, the method of payment, and the amount of payment.

The task is to analyze the data and predict the churn of users (to identify people who will and will not renew their contract). The work should include the following mandatory items:

1. Description of the data (with the calculation of basic statistics);
2. Research of dependencies and formulation of hypotheses;
3. Building models for predicting the outflow (with justification for the choice of a particular model) 4. based on tested hypotheses and identified relationships;
5. Comparison of the quality of the obtained models.

**Опис полів набору даних:**

- [x] `customerID` - customer id
- [x] `gender` - client gender (male / female)
- [x] `SeniorCitizen` - is the client retired (1, 0)
- [x] `Partner` - is the client married (Yes, No)
- [x] `tenure` - how many months a person has been a client of the company
- [x] `PhoneService` - is the telephone service connected (Yes, No)
- [x] `MultipleLines` - are multiple phone lines connected (Yes, No, No phone service)
- [x] `InternetService` - client's Internet service provider (DSL, Fiber optic, No)
- [x] `OnlineSecurity` - is the online security service connected (Yes, No, No internet service)
- [x] `OnlineBackup` - is the online backup service activated (Yes, No, No internet service)
- [x] `DeviceProtection` - does the client have equipment insurance (Yes, No, No internet service)
- [x] `TechSupport` - is the technical support service connected (Yes, No, No internet service)
- [x] `StreamingTV` - is the streaming TV service connected (Yes, No, No internet service)
- [x] `StreamingMovies` - is the streaming cinema service activated (Yes, No, No internet service)
- [x] `Contract` - type of customer contract (Month-to-month, One year, Two year)
- [x] `PaperlessBilling` - whether the client uses paperless billing (Yes, No)
- [x] `PaymentMethod` - payment method (Electronic check, Mailed check, Bank transfer (automatic), Credit card (automatic))
- [x] `MonthlyCharges` - current monthly payment
- [x] `TotalCharges` - the total amount that the client paid for the services for the entire time
- [x] `Churn - whether` there was a churn (Yes or No)

## Імпорт даних засобами RStudio {#chapter321}

`RStudio` має ряд засобів для

## CSV-файли: читання, {#chapter321}

**CSV** - це тип файлів, у якому інформація розділена комами (`Comma Separated Values`). CSV є досить зручним форматом даних для передачі між різними машинами, адже по суті є текстовим файлом і дозволяє легко його зчитати.

_Примітка. Наспрвді кома не завжди є роздільником CSV-файлів. Це можуть бути і інші символи._


