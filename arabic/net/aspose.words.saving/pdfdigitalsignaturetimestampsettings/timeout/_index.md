---
title: PdfDigitalSignatureTimestampSettings.Timeout
second_title: Aspose.Words لمراجع .NET API
description: PdfDigitalSignatureTimestampSettings ملكية. قيمة المهلة للوصول إلى خادم الطابع الزمني.
type: docs
weight: 40
url: /ar/net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/timeout/
---
## PdfDigitalSignatureTimestampSettings.Timeout property

قيمة المهلة للوصول إلى خادم الطابع الزمني.

```csharp
public TimeSpan Timeout { get; set; }
```

### ملاحظات

القيمة الافتراضية هي 100 ثانية .

### أمثلة

يوضح كيفية توقيع مستند PDF محفوظ رقميًا وطابعه الزمني.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Signed PDF contents.");

// قم بإنشاء كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة المستند إلى PDF.
PdfSaveOptions options = new PdfSaveOptions();

 // أنشئ توقيعًا رقميًا وقم بتعيينه إلى كائن SaveOptions الخاص بنا لتوقيع المستند عندما نحفظه في PDF.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
options.DigitalSignatureDetails = new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "Aspose Office", DateTime.Now);

// إنشاء طابع زمني تم التحقق منه من قِبل السلطة.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr "،" JohnDoe "،" MyPassword ");

// العمر الافتراضي للطابع الزمني هو 100 ثانية.
Assert.AreEqual(100.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);

// يمكننا ضبط فترة المهلة عبر المُنشئ.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr "،" JohnDoe "،" MyPassword "، TimeSpan.FromMinutes (30)) ;

Assert.AreEqual(1800.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);
Assert.AreEqual("https://freetsa.org/tsr "، options.DigitalSignatureDetails.TimestampSettings.ServerUrl) ;
Assert.AreEqual("JohnDoe", options.DigitalSignatureDetails.TimestampSettings.UserName);
Assert.AreEqual("MyPassword", options.DigitalSignatureDetails.TimestampSettings.Password);

// ستطبق طريقة "Save" توقيعنا على المستند الناتج في هذا الوقت.
doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf", options);
```

### أنظر أيضا

* class [PdfDigitalSignatureTimestampSettings](../)
* مساحة الاسم [Aspose.Words.Saving](../../pdfdigitalsignaturetimestampsettings/)
* المجسم [Aspose.Words](../../../)


