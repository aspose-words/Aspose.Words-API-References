---
title: HtmlLoadOptions
linktitle: HtmlLoadOptions
articleTitle: HtmlLoadOptions
second_title: Aspose.Words لـ .NET
description: HtmlLoadOptions البناء. تهيئة مثيل جديد لهذه الفئة بالقيم الافتراضية في C#.
type: docs
weight: 10
url: /ar/net/aspose.words.loading/htmlloadoptions/htmlloadoptions/
---
## HtmlLoadOptions() {#constructor}

تهيئة مثيل جديد لهذه الفئة بالقيم الافتراضية.

```csharp
public HtmlLoadOptions()
```

## أمثلة

يوضح كيفية دعم التعليقات الشرطية أثناء تحميل مستند HTML.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();

// إذا كانت القيمة صحيحة، فسنأخذ رمز VML في الاعتبار أثناء تحليل المستند الذي تم تحميله.
loadOptions.SupportVml = supportVml;

// يحتوي هذا المستند على صورة JPEG داخل "<!--[if gte vml 1]>" العلامات,
// وصورة PNG مختلفة داخل "<![if !vml]>" العلامات.
// إذا قمنا بتعيين علامة "SupportVml" على "صحيح"، فسيقوم Aspose.Words بتحميل ملف JPEG.
// إذا قمنا بتعيين هذه العلامة على "خطأ"، فسيقوم Aspose.Words بتحميل ملف PNG فقط.
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

اختصار لتهيئة مثيل جديد لهذه الفئة بكلمة المرور المحددة لتحميل مستند مشفر.

```csharp
public HtmlLoadOptions(string password)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| password | String | كلمة المرور لفتح مستند مشفر. يمكن ان يكون`باطل` أو سلسلة فارغة. |

## أمثلة

يوضح كيفية تشفير مستند Html، ثم فتحه باستخدام كلمة مرور.

```csharp
// قم بإنشاء وتوقيع مستند HTML مشفر من ملف .docx مشفر.
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

// لتحميل هذا المستند وقراءته، سنحتاج إلى اجتياز عملية فك التشفير
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

اختصار لتهيئة مثيل جديد لهذه الفئة مع تعيين الخصائص على القيم المحددة.

```csharp
public HtmlLoadOptions(LoadFormat loadFormat, string password, string baseUri)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| loadFormat | LoadFormat | تنسيق الوثيقة المراد تحميلها. |
| password | String | كلمة المرور لفتح مستند مشفر. يمكن ان يكون`باطل` أو سلسلة فارغة. |
| baseUri | String | السلسلة التي سيتم استخدامها لتحليل معرفات URI النسبية إلى مطلقة. يمكن ان يكون`باطل` أو سلسلة فارغة. |

## أمثلة

يوضح كيفية تحديد عنوان URI أساسي عند فتح مستند html.

```csharp
// لنفترض أننا نريد تحميل مستند .html يحتوي على صورة مرتبطة بمعرف URI نسبي
// أثناء وجود الصورة في موقع مختلف. في هذه الحالة، سنحتاج إلى تحويل معرف URI النسبي إلى عنوان مطلق.
 // يمكننا توفير عنوان URI أساسي باستخدام كائن HtmlLoadOptions.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// أثناء تعطل الصورة في ملف الإدخال .html، ساعدنا عنوان URI الأساسي المخصص لدينا في إصلاح الرابط.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// سيعرض مستند الإخراج هذا الصورة المفقودة.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

### أنظر أيضا

* enum [LoadFormat](../../../aspose.words/loadformat/)
* class [HtmlLoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
