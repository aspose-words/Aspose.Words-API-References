---
title: PdfDigitalSignatureTimestampSettings Class
linktitle: PdfDigitalSignatureTimestampSettings
articleTitle: PdfDigitalSignatureTimestampSettings
second_title: Aspose.Words لـ .NET
description: اكتشف إعدادات Aspose.Words.PdfDigitalSignatureTimestamp لإدارة سلسة لتوقيعاتك الرقمية. حسّن أمان ملفات PDF الخاصة بك بسهولة!
type: docs
weight: 6240
url: /ar/net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/
---
## PdfDigitalSignatureTimestampSettings class

يحتوي على إعدادات الطابع الزمني للتوقيع الرقمي.

لمعرفة المزيد، قم بزيارة[العمل مع التوقيعات الرقمية](https://docs.aspose.com/words/net/working-with-digital-signatures/) مقالة توثيقية.

```csharp
public class PdfDigitalSignatureTimestampSettings
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [PdfDigitalSignatureTimestampSettings](pdfdigitalsignaturetimestampsettings/#constructor)() | يقوم بتهيئة مثيل لهذه الفئة. |
| [PdfDigitalSignatureTimestampSettings](pdfdigitalsignaturetimestampsettings/#constructor_1)(*string, string, string*) | يقوم بتهيئة مثيل لهذه الفئة. |
| [PdfDigitalSignatureTimestampSettings](pdfdigitalsignaturetimestampsettings/#constructor_2)(*string, string, string, TimeSpan*) | يقوم بتهيئة مثيل لهذه الفئة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Password](../../aspose.words.saving/pdfdigitalsignaturetimestampsettings/password/) { get; set; } | كلمة مرور خادم الطابع الزمني. |
| [ServerUrl](../../aspose.words.saving/pdfdigitalsignaturetimestampsettings/serverurl/) { get; set; } | عنوان URL لخادم الطابع الزمني. |
| [Timeout](../../aspose.words.saving/pdfdigitalsignaturetimestampsettings/timeout/) { get; set; } | قيمة مهلة الوصول إلى خادم الطابع الزمني. |
| [UserName](../../aspose.words.saving/pdfdigitalsignaturetimestampsettings/username/) { get; set; } | اسم مستخدم خادم الطابع الزمني. |

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
