---
title: PdfDigitalSignatureTimestampSettings.PdfDigitalSignatureTimestampSettings
second_title: Справочник по API Aspose.Words для .NET
description: PdfDigitalSignatureTimestampSettings строитель. Инициализирует экземпляр этого класса.
type: docs
weight: 10
url: /ru/net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/pdfdigitalsignaturetimestampsettings/
---
## PdfDigitalSignatureTimestampSettings() {#constructor}

Инициализирует экземпляр этого класса.

```csharp
public PdfDigitalSignatureTimestampSettings()
```

### Примеры

Показывает, как подписать сохраненный PDF-документ цифровой подписью и поставить на нем метку времени.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Signed PDF contents.");

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Создайте цифровую подпись и назначьте ее нашему объекту SaveOptions, чтобы подписывать документ при сохранении его в PDF.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
options.DigitalSignatureDetails = new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "Aspose Office", DateTime.Now);

// Создаем временную метку, проверенную авторитетным органом.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword");

// Срок действия метки времени по умолчанию составляет 100 секунд.
Assert.AreEqual(100.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);

// Мы можем установить период ожидания через конструктор.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword", TimeSpan.FromMinutes(30));

Assert.AreEqual(1800.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);
Assert.AreEqual("https://freetsa.org/tsr", options.DigitalSignatureDetails.TimestampSettings.ServerUrl);
Assert.AreEqual("JohnDoe", options.DigitalSignatureDetails.TimestampSettings.UserName);
Assert.AreEqual("MyPassword", options.DigitalSignatureDetails.TimestampSettings.Password);

// В это время метод «Сохранить» применит нашу подпись к выходному документу.
doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf", options);
```

### Смотрите также

* class [PdfDigitalSignatureTimestampSettings](../)
* пространство имен [Aspose.Words.Saving](../../pdfdigitalsignaturetimestampsettings/)
* сборка [Aspose.Words](../../../)

---

## PdfDigitalSignatureTimestampSettings(string, string, string) {#constructor_1}

Инициализирует экземпляр этого класса.

```csharp
public PdfDigitalSignatureTimestampSettings(string serverUrl, string userName, string password)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| serverUrl | String | URL-адрес сервера меток времени. |
| userName | String | Имя пользователя сервера меток времени. |
| password | String | Пароль сервера меток времени. |

### Примеры

Показывает, как подписать сохраненный PDF-документ цифровой подписью и поставить на нем метку времени.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Signed PDF contents.");

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Создайте цифровую подпись и назначьте ее нашему объекту SaveOptions, чтобы подписывать документ при сохранении его в PDF.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
options.DigitalSignatureDetails = new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "Aspose Office", DateTime.Now);

// Создаем временную метку, проверенную авторитетным органом.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword");

// Срок действия метки времени по умолчанию составляет 100 секунд.
Assert.AreEqual(100.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);

// Мы можем установить период ожидания через конструктор.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword", TimeSpan.FromMinutes(30));

Assert.AreEqual(1800.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);
Assert.AreEqual("https://freetsa.org/tsr", options.DigitalSignatureDetails.TimestampSettings.ServerUrl);
Assert.AreEqual("JohnDoe", options.DigitalSignatureDetails.TimestampSettings.UserName);
Assert.AreEqual("MyPassword", options.DigitalSignatureDetails.TimestampSettings.Password);

// В это время метод «Сохранить» применит нашу подпись к выходному документу.
doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf", options);
```

### Смотрите также

* class [PdfDigitalSignatureTimestampSettings](../)
* пространство имен [Aspose.Words.Saving](../../pdfdigitalsignaturetimestampsettings/)
* сборка [Aspose.Words](../../../)

---

## PdfDigitalSignatureTimestampSettings(string, string, string, TimeSpan) {#constructor_2}

Инициализирует экземпляр этого класса.

```csharp
public PdfDigitalSignatureTimestampSettings(string serverUrl, string userName, string password, 
    TimeSpan timeout)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| serverUrl | String | URL-адрес сервера меток времени. |
| userName | String | Имя пользователя сервера меток времени. |
| password | String | Пароль сервера меток времени. |
| timeout | TimeSpan | Значение времени ожидания для доступа к серверу меток времени. |

### Примеры

Показывает, как подписать сохраненный PDF-документ цифровой подписью и поставить на нем метку времени.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Signed PDF contents.");

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Создайте цифровую подпись и назначьте ее нашему объекту SaveOptions, чтобы подписывать документ при сохранении его в PDF.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
options.DigitalSignatureDetails = new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "Aspose Office", DateTime.Now);

// Создаем временную метку, проверенную авторитетным органом.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword");

// Срок действия метки времени по умолчанию составляет 100 секунд.
Assert.AreEqual(100.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);

// Мы можем установить период ожидания через конструктор.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword", TimeSpan.FromMinutes(30));

Assert.AreEqual(1800.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);
Assert.AreEqual("https://freetsa.org/tsr", options.DigitalSignatureDetails.TimestampSettings.ServerUrl);
Assert.AreEqual("JohnDoe", options.DigitalSignatureDetails.TimestampSettings.UserName);
Assert.AreEqual("MyPassword", options.DigitalSignatureDetails.TimestampSettings.Password);

// В это время метод «Сохранить» применит нашу подпись к выходному документу.
doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf", options);
```

### Смотрите также

* class [PdfDigitalSignatureTimestampSettings](../)
* пространство имен [Aspose.Words.Saving](../../pdfdigitalsignaturetimestampsettings/)
* сборка [Aspose.Words](../../../)


