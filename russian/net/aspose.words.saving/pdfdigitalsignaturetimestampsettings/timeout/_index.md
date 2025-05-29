---
title: PdfDigitalSignatureTimestampSettings.Timeout
linktitle: Timeout
articleTitle: Timeout
second_title: Aspose.Words для .NET
description: Оптимизируйте свой PdfDigitalSignature с помощью настраиваемых параметров тайм-аута для бесперебойного доступа к серверам временных меток. Повысьте безопасность и эффективность сегодня!
type: docs
weight: 40
url: /ru/net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/timeout/
---
## PdfDigitalSignatureTimestampSettings.Timeout property

Значение тайм-аута для доступа к серверу временных меток.

```csharp
public TimeSpan Timeout { get; set; }
```

## Примечания

Значение по умолчанию — 100 секунд.

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
