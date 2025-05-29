---
title: PdfDigitalSignatureTimestampSettings.UserName
linktitle: UserName
articleTitle: UserName
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية اسم المستخدم في PdfDigitalSignatureTimestampSettings لختم زمني آمن. عزز سلامة مستندك من خلال مصادقة خادم موثوقة.
type: docs
weight: 50
url: /ar/net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/username/
---
## PdfDigitalSignatureTimestampSettings.UserName property

اسم مستخدم خادم الطابع الزمني.

```csharp
public string UserName { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`باطل` .

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

* class [PdfDigitalSignatureTimestampSettings](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
