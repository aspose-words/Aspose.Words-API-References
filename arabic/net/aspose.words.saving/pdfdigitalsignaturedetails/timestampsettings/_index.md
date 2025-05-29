---
title: PdfDigitalSignatureDetails.TimestampSettings
linktitle: TimestampSettings
articleTitle: TimestampSettings
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PdfDigitalSignatureDetails TimestampSettings لإدارة طوابع زمنية للتوقيع الرقمي بسهولة لتحسين أمان المستندات والامتثال لها.
type: docs
weight: 70
url: /ar/net/aspose.words.saving/pdfdigitalsignaturedetails/timestampsettings/
---
## PdfDigitalSignatureDetails.TimestampSettings property

يحصل على إعدادات طابع زمني للتوقيع الرقمي أو يعينها.

```csharp
public PdfDigitalSignatureTimestampSettings TimestampSettings { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`باطل` ولن يتم ختم التوقيع الرقمي بختم زمني. عندما يتم تعيين هذه الخاصية على قيمة صالحة[`PdfDigitalSignatureTimestampSettings`](../../pdfdigitalsignaturetimestampsettings/) الكائن، ثم سيتم ختم التوقيع الرقمي في مستند PDF بختم زمني.

## أمثلة

يوضح كيفية التوقيع على مستند PDF محفوظ رقميًا ووضع علامة زمنية عليه.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Signed PDF contents.");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// قم بإنشاء توقيع رقمي وقم بتعيينه إلى كائن SaveOptions الخاص بنا لتوقيع المستند عند حفظه بتنسيق PDF.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
options.DigitalSignatureDetails = new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "Aspose Office", DateTime.Now);

// إنشاء طابع زمني تم التحقق منه بواسطة السلطة.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr"، "JohnDoe"، "MyPassword");

//المدة الافتراضية لطابع الوقت هي 100 ثانية.
Assert.AreEqual(100.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);

//يمكننا ضبط فترة المهلة الزمنية الخاصة بنا عبر المنشئ.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr"، "JohnDoe"، "MyPassword"، TimeSpan.FromMinutes(30));

Assert.AreEqual(1800.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);
Assert.AreEqual("https://freetsa.org/tsr"، الخيارات. تفاصيل التوقيع الرقمي. إعدادات الطابع الزمني. عنوان URL للخادم);
Assert.AreEqual("JohnDoe", options.DigitalSignatureDetails.TimestampSettings.UserName);
Assert.AreEqual("MyPassword", options.DigitalSignatureDetails.TimestampSettings.Password);

// ستقوم طريقة "الحفظ" بتطبيق توقيعنا على المستند الناتج في هذا الوقت.
doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf", options);
```

### أنظر أيضا

* class [PdfDigitalSignatureTimestampSettings](../../pdfdigitalsignaturetimestampsettings/)
* class [PdfDigitalSignatureDetails](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
