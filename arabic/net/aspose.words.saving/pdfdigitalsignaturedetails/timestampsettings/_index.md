---
title: PdfDigitalSignatureDetails.TimestampSettings
second_title: Aspose.Words لمراجع .NET API
description: PdfDigitalSignatureDetails ملكية. الحصول على إعدادات الطابع الزمني للتوقيع الرقمي أو تعيينها.
type: docs
weight: 70
url: /ar/net/aspose.words.saving/pdfdigitalsignaturedetails/timestampsettings/
---
## PdfDigitalSignatureDetails.TimestampSettings property

الحصول على إعدادات الطابع الزمني للتوقيع الرقمي أو تعيينها.

```csharp
public PdfDigitalSignatureTimestampSettings TimestampSettings { get; set; }
```

### ملاحظات

القيمة الافتراضية هي`باطل` ولن يتم ختم التوقيع الرقمي بالوقت. عندما يتم تعيين هذه الخاصية على قيمة صالحة[`PdfDigitalSignatureTimestampSettings`](../../pdfdigitalsignaturetimestampsettings/) object, ثم سيتم ختم التوقيع الرقمي في مستند PDF بالوقت.

### أمثلة

يوضح كيفية توقيع مستند PDF محفوظ رقميًا ووضع طابع زمني عليه.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Signed PDF contents.");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// أنشئ توقيعًا رقميًا وقم بتعيينه لكائن SaveOptions الخاص بنا لتوقيع المستند عندما نحفظه في ملف PDF.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
options.DigitalSignatureDetails = new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "Aspose Office", DateTime.Now);

// قم بإنشاء طابع زمني تم التحقق منه بواسطة سلطة الطابع الزمني.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr"، "JohnDoe"، "MyPassword");

// العمر الافتراضي للطابع الزمني هو 100 ثانية.
Assert.AreEqual(100.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);

// يمكننا ضبط فترة المهلة الخاصة بنا عبر المنشئ.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr"، "JohnDoe"، "MyPassword"، TimeSpan.FromMinutes(30));

Assert.AreEqual(1800.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);
Assert.AreEqual("https://freetsa.org/tsr"، options.DigitalSignatureDetails.TimestampSettings.ServerUrl);
Assert.AreEqual("JohnDoe", options.DigitalSignatureDetails.TimestampSettings.UserName);
Assert.AreEqual("MyPassword", options.DigitalSignatureDetails.TimestampSettings.Password);

// ستطبق طريقة "الحفظ" توقيعنا على مستند الإخراج في هذا الوقت.
doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf", options);
```

### أنظر أيضا

* class [PdfDigitalSignatureTimestampSettings](../../pdfdigitalsignaturetimestampsettings/)
* class [PdfDigitalSignatureDetails](../)
* مساحة الاسم [Aspose.Words.Saving](../../pdfdigitalsignaturedetails/)
* المجسم [Aspose.Words](../../../)


