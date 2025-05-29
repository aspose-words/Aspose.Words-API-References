---
title: PdfDigitalSignatureTimestampSettings
linktitle: PdfDigitalSignatureTimestampSettings
articleTitle: PdfDigitalSignatureTimestampSettings
second_title: Aspose.Words для .NET
description: Откройте для себя конструктор PdfDigitalSignatureTimestampSettings, который позволяет легко инициализировать параметры цифровой подписи для повышения безопасности документов и соответствия нормативным требованиям.
type: docs
weight: 10
url: /ru/net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/pdfdigitalsignaturetimestampsettings/
---
## PdfDigitalSignatureTimestampSettings() {#constructor}

Инициализирует экземпляр этого класса.

```csharp
public PdfDigitalSignatureTimestampSettings()
```

## Примеры

Показывает, как подписать сохраненный PDF-документ цифровой подписью и поставить на нем временную метку.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Signed PDF contents.");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Создаем цифровую подпись и назначаем ее нашему объекту SaveOptions для подписи документа при сохранении его в формате PDF.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
options.DigitalSignatureDetails = new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "Aspose Office", DateTime.Now);

// Создать временную метку, проверенную органом власти.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword");

// Срок действия временной метки по умолчанию составляет 100 секунд.
Assert.AreEqual(100.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);

// Мы можем установить период ожидания через конструктор.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword", TimeSpan.FromMinutes(30));

Assert.AreEqual(1800.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);
Assert.AreEqual("https://freetsa.org/tsr", options.DigitalSignatureDetails.TimestampSettings.ServerUrl);
Assert.AreEqual("JohnDoe", options.DigitalSignatureDetails.TimestampSettings.UserName);
Assert.AreEqual("MyPassword", options.DigitalSignatureDetails.TimestampSettings.Password);

// Метод «Сохранить» в этот раз применит нашу подпись к выходному документу.
doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf", options);
```

### Смотрите также

* class [PdfDigitalSignatureTimestampSettings](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)

---

## PdfDigitalSignatureTimestampSettings(*string, string, string*) {#constructor_1}

Инициализирует экземпляр этого класса.

```csharp
public PdfDigitalSignatureTimestampSettings(string serverUrl, string userName, string password)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| serverUrl | String | URL-адрес сервера временных меток. |
| userName | String | Имя пользователя сервера временных меток. |
| password | String | Пароль сервера отметок времени. |

## Примеры

Показывает, как подписать сохраненный PDF-документ цифровой подписью и поставить на нем временную метку.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Signed PDF contents.");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Создаем цифровую подпись и назначаем ее нашему объекту SaveOptions для подписи документа при сохранении его в формате PDF.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
options.DigitalSignatureDetails = new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "Aspose Office", DateTime.Now);

// Создать временную метку, проверенную органом власти.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword");

// Срок действия временной метки по умолчанию составляет 100 секунд.
Assert.AreEqual(100.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);

// Мы можем установить период ожидания через конструктор.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword", TimeSpan.FromMinutes(30));

Assert.AreEqual(1800.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);
Assert.AreEqual("https://freetsa.org/tsr", options.DigitalSignatureDetails.TimestampSettings.ServerUrl);
Assert.AreEqual("JohnDoe", options.DigitalSignatureDetails.TimestampSettings.UserName);
Assert.AreEqual("MyPassword", options.DigitalSignatureDetails.TimestampSettings.Password);

// Метод «Сохранить» в этот раз применит нашу подпись к выходному документу.
doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf", options);
```

### Смотрите также

* class [PdfDigitalSignatureTimestampSettings](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)

---

## PdfDigitalSignatureTimestampSettings(*string, string, string, TimeSpan*) {#constructor_2}

Инициализирует экземпляр этого класса.

```csharp
public PdfDigitalSignatureTimestampSettings(string serverUrl, string userName, string password, 
    TimeSpan timeout)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| serverUrl | String | URL-адрес сервера временных меток. |
| userName | String | Имя пользователя сервера временных меток. |
| password | String | Пароль сервера отметок времени. |
| timeout | TimeSpan | Значение тайм-аута для доступа к серверу временных меток. |

## Примеры

Показывает, как подписать сохраненный PDF-документ цифровой подписью и поставить на нем временную метку.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Signed PDF contents.");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Создаем цифровую подпись и назначаем ее нашему объекту SaveOptions для подписи документа при сохранении его в формате PDF.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
options.DigitalSignatureDetails = new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "Aspose Office", DateTime.Now);

// Создать временную метку, проверенную органом власти.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword");

// Срок действия временной метки по умолчанию составляет 100 секунд.
Assert.AreEqual(100.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);

// Мы можем установить период ожидания через конструктор.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword", TimeSpan.FromMinutes(30));

Assert.AreEqual(1800.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);
Assert.AreEqual("https://freetsa.org/tsr", options.DigitalSignatureDetails.TimestampSettings.ServerUrl);
Assert.AreEqual("JohnDoe", options.DigitalSignatureDetails.TimestampSettings.UserName);
Assert.AreEqual("MyPassword", options.DigitalSignatureDetails.TimestampSettings.Password);

// Метод «Сохранить» в этот раз применит нашу подпись к выходному документу.
doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf", options);
```

### Смотрите также

* class [PdfDigitalSignatureTimestampSettings](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
