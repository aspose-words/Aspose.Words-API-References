---
title: PdfDigitalSignatureTimestampSettings.ServerUrl
linktitle: ServerUrl
articleTitle: ServerUrl
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PdfDigitalSignatureTimestampSettings ServerUrl для безопасного временного штампа. Обеспечьте целостность документа с помощью надежных URL-адресов сервера временных штампов.
type: docs
weight: 30
url: /ru/net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/serverurl/
---
## PdfDigitalSignatureTimestampSettings.ServerUrl property

URL сервера временных меток.

```csharp
public string ServerUrl { get; set; }
```

## Примечания

Значение по умолчанию:`нулевой` . Если`нулевой` , то цифровая подпись не будет иметь временной отметки.

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
