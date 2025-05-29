---
title: LoadOptions
linktitle: LoadOptions
articleTitle: LoadOptions
second_title: Aspose.Words لـ .NET
description: اكتشف منشئ LoadOptions، المصمم لتهيئة مثيل جديد بسهولة باستخدام القيم الافتراضية لتحقيق الأداء والكفاءة الأمثل.
type: docs
weight: 10
url: /ar/net/aspose.words.loading/loadoptions/loadoptions/
---
## LoadOptions() {#constructor}

يقوم بتهيئة مثيل جديد لهذه الفئة بالقيم الافتراضية.

```csharp
public LoadOptions()
```

## أمثلة

يوضح كيفية فتح مستند HTML يحتوي على صور من مجرى باستخدام عنوان URI أساسي.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // قم بتمرير عنوان URI للمجلد الأساسي أثناء تحميله
    // بحيث يمكن العثور على أي صور تحتوي على عناوين URI نسبية في مستند HTML.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // تأكد من أن الشكل الأول للمستند يحتوي على صورة صالحة.
    Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    Assert.IsTrue(shape.IsImage);
    Assert.IsNotNull(shape.ImageData.ImageBytes);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Width), 0.01);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Height), 0.01);
}
```

### أنظر أيضا

* class [LoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)

---

## LoadOptions(*string*) {#constructor_2}

اختصار لتهيئة مثيل جديد لهذه الفئة باستخدام كلمة المرور المحددة لتحميل مستند مشفر.

```csharp
public LoadOptions(string password)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| password | String | كلمة المرور لفتح مستند مشفر. يمكن`باطل` أو سلسلة فارغة. |

## أمثلة

يوضح كيفية تحميل مستند Microsoft Word مشفر.

```csharp
Document doc;

// يطرح Aspose.Words استثناءً إذا حاولنا فتح مستند مشفر بدون كلمة المرور الخاصة به.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// عند تحميل مثل هذه الوثيقة، يتم تمرير كلمة المرور إلى منشئ الوثيقة باستخدام كائن LoadOptions.
LoadOptions options = new LoadOptions("docPassword");

// هناك طريقتان لتحميل مستند مشفر باستخدام كائن LoadOptions.
// 1 - قم بتحميل المستند من نظام الملفات المحلي حسب اسم الملف:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - تحميل المستند من مجرى:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

### أنظر أيضا

* class [LoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)

---

## LoadOptions(*[LoadFormat](../../../aspose.words/loadformat/), string, string*) {#constructor_1}

اختصار لتهيئة مثيل جديد لهذه الفئة مع تعيين الخصائص إلى القيم المحددة.

```csharp
public LoadOptions(LoadFormat loadFormat, string password, string baseUri)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| loadFormat | LoadFormat | تنسيق المستند الذي سيتم تحميله. |
| password | String | كلمة المرور لفتح مستند مشفر. يمكن`باطل` أو سلسلة فارغة. |
| baseUri | String | السلسلة التي سيتم استخدامها لتحويل عناوين URI النسبية إلى عناوين مطلقة. يمكن أن تكون`باطل` أو سلسلة فارغة. |

## أمثلة

يوضح كيفية حفظ صفحة الويب كملف .docx.

```csharp
const string url = "https://products.aspose.com/words/";

using (WebClient client = new WebClient())
{
    var bytes = client.DownloadData(url);
    using (MemoryStream stream = new MemoryStream(bytes))
    {
        // يتم استخدام عنوان URL مرة أخرى باعتباره Uri أساسيًا للتأكد من استرداد أي مسارات صور نسبية بشكل صحيح.
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // قم بتحميل مستند HTML من الدفق ومرر كائن LoadOptions.
        Document doc = new Document(stream, options);

        // في هذه المرحلة، يمكننا قراءة محتويات المستند وتحريرها ثم حفظها في نظام الملفات المحلي.
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

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
* class [LoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
