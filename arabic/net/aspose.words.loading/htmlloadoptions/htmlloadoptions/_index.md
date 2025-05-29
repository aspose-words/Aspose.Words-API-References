---
title: HtmlLoadOptions
linktitle: HtmlLoadOptions
articleTitle: HtmlLoadOptions
second_title: Aspose.Words لـ .NET
description: اكتشف منشئ HtmlLoadOptions، المصمم لتهيئة الحالات بسهولة باستخدام الإعدادات الافتراضية لتطوير ويب سلس.
type: docs
weight: 10
url: /ar/net/aspose.words.loading/htmlloadoptions/htmlloadoptions/
---
## HtmlLoadOptions() {#constructor}

يقوم بتهيئة مثيل جديد لهذه الفئة بالقيم الافتراضية.

```csharp
public HtmlLoadOptions()
```

## أمثلة

يوضح كيفية دعم التعليقات الشرطية أثناء تحميل مستند HTML.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();

// إذا كانت القيمة صحيحة، فإننا نأخذ كود VML في الاعتبار أثناء تحليل المستند المحمّل.
loadOptions.SupportVml = supportVml;

// تحتوي هذه الوثيقة على صورة JPEG ضمن علامات "<!--[if gte vml 1]>"،
// وصورة PNG مختلفة ضمن علامات "<![if !vml]>".
// إذا قمنا بتعيين علامة "SupportVml" إلى "true"، فسوف يقوم Aspose.Words بتحميل ملف JPEG.
// إذا قمنا بتعيين هذا العلم إلى "false"، فسوف يقوم Aspose.Words بتحميل PNG فقط.
Document doc = new Document(MyDir + "VML conditional.htm", loadOptions);

if (supportVml)
    Assert.AreEqual(ImageType.Jpeg, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
else
    Assert.AreEqual(ImageType.Png, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
```

### أنظر أيضا

* class [HtmlLoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)

---

## HtmlLoadOptions(*string*) {#constructor_2}

اختصار لتهيئة مثيل جديد لهذه الفئة باستخدام كلمة المرور المحددة لتحميل مستند مشفر.

```csharp
public HtmlLoadOptions(string password)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| password | String | كلمة المرور لفتح مستند مشفر. يمكن`باطل` أو سلسلة فارغة. |

## أمثلة

يوضح كيفية تشفير مستند HTML، ثم فتحه باستخدام كلمة مرور.

```csharp
// إنشاء وتوقيع مستند HTML مشفر من ملف .docx مشفر.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

SignOptions signOptions = new SignOptions
{
    Comments = "Comment",
    SignTime = DateTime.Now,
    DecryptionPassword = "docPassword"
};

string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "HtmlLoadOptions.EncryptedHtml.html";
DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);

// لتحميل هذه الوثيقة وقراءتها، سنحتاج إلى تمرير فك تشفيرها
// كلمة المرور باستخدام كائن HtmlLoadOptions.
HtmlLoadOptions loadOptions = new HtmlLoadOptions("docPassword");

Assert.AreEqual(signOptions.DecryptionPassword, loadOptions.Password);

Document doc = new Document(outputFileName, loadOptions);

Assert.AreEqual("Test encrypted document.", doc.GetText().Trim());
```

### أنظر أيضا

* class [HtmlLoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)

---

## HtmlLoadOptions(*[LoadFormat](../../../aspose.words/loadformat/), string, string*) {#constructor_1}

اختصار لتهيئة مثيل جديد لهذه الفئة مع تعيين الخصائص إلى القيم المحددة.

```csharp
public HtmlLoadOptions(LoadFormat loadFormat, string password, string baseUri)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| loadFormat | LoadFormat | تنسيق المستند الذي سيتم تحميله. |
| password | String | كلمة المرور لفتح مستند مشفر. يمكن`باطل` أو سلسلة فارغة. |
| baseUri | String | السلسلة التي سيتم استخدامها لتحويل عناوين URI النسبية إلى عناوين مطلقة. يمكن أن تكون`باطل` أو سلسلة فارغة. |

## أمثلة

يوضح كيفية تحديد عنوان URI الأساسي عند فتح مستند html.

```csharp
// افترض أننا نريد تحميل مستند .html يحتوي على صورة مرتبطة بمعرف URI نسبي
// بينما الصورة في موقع مختلف. في هذه الحالة، سنحتاج إلى تحويل عنوان URI النسبي إلى عنوان URI مطلق.
 // يمكننا توفير عنوان URI أساسي باستخدام كائن HtmlLoadOptions.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// بينما كانت الصورة معطلة في ملف .html المدخل، ساعدنا عنوان URI الأساسي المخصص في إصلاح الرابط.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// ستعرض وثيقة الإخراج هذه الصورة المفقودة.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

### أنظر أيضا

* enum [LoadFormat](../../../aspose.words/loadformat/)
* class [HtmlLoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
