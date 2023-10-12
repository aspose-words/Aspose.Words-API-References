---
title: LoadOptions.LoadOptions
second_title: Aspose.Words لمراجع .NET API
description: LoadOptions البناء. تهيئة مثيل جديد لهذه الفئة بالقيم الافتراضية.
type: docs
weight: 10
url: /ar/net/aspose.words.loading/loadoptions/loadoptions/
---
## LoadOptions() {#constructor}

تهيئة مثيل جديد لهذه الفئة بالقيم الافتراضية.

```csharp
public LoadOptions()
```

### أمثلة

يوضح كيفية فتح مستند HTML يحتوي على صور من دفق باستخدام عنوان URI أساسي.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // قم بتمرير URI للمجلد الأساسي أثناء تحميله
    // بحيث يمكن العثور على أي صور ذات عناوين URI نسبية في مستند HTML.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // تحقق من أن الشكل الأول للمستند يحتوي على صورة صالحة.
    Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    Assert.IsTrue(shape.IsImage);
    Assert.IsNotNull(shape.ImageData.ImageBytes);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Width), 0.01);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Height), 0.01);
}
```

### أنظر أيضا

* class [LoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../loadoptions/)
* المجسم [Aspose.Words](../../../)

---

## LoadOptions(string) {#constructor_2}

اختصار لتهيئة مثيل جديد لهذه الفئة بكلمة المرور المحددة لتحميل مستند مشفر.

```csharp
public LoadOptions(string password)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| password | String | كلمة المرور لفتح مستند مشفر. يمكن ان يكون`باطل` أو سلسلة فارغة. |

### أمثلة

يوضح كيفية تحميل مستند Microsoft Word المشفر.

```csharp
Document doc;

// Aspose.Words يطرح استثناءً إذا حاولنا فتح مستند مشفر بدون كلمة المرور الخاصة به.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// عند تحميل مثل هذا المستند، يتم تمرير كلمة المرور إلى مُنشئ المستند باستخدام كائن LoadOptions.
LoadOptions options = new LoadOptions("docPassword");

// هناك طريقتان لتحميل مستند مشفر باستخدام كائن LoadOptions.
// 1 - قم بتحميل المستند من نظام الملفات المحلي حسب اسم الملف:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - تحميل المستند من الدفق:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

### أنظر أيضا

* class [LoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../loadoptions/)
* المجسم [Aspose.Words](../../../)

---

## LoadOptions(LoadFormat, string, string) {#constructor_1}

اختصار لتهيئة مثيل جديد لهذه الفئة مع تعيين الخصائص على القيم المحددة.

```csharp
public LoadOptions(LoadFormat loadFormat, string password, string baseUri)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| loadFormat | LoadFormat | تنسيق الوثيقة المراد تحميلها. |
| password | String | كلمة المرور لفتح مستند مشفر. يمكن ان يكون`باطل` أو سلسلة فارغة. |
| baseUri | String | السلسلة التي سيتم استخدامها لتحليل معرفات URI النسبية إلى مطلقة. يمكن ان يكون`باطل` أو سلسلة فارغة. |

### أمثلة

يوضح كيفية حفظ صفحة ويب كملف .docx.

```csharp
const string url = "https://www.aspose.com/";

using (HttpClient client = new HttpClient()) 
{
    var bytes = await client.GetByteArrayAsync(url);
    using (MemoryStream stream = new MemoryStream(bytes))
    {
        // يتم استخدام عنوان URL مرة أخرى باعتباره BaseUri لضمان استرداد أي مسارات صور نسبية بشكل صحيح.
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // قم بتحميل مستند HTML من الدفق وتمرير كائن LoadOptions.
        Document doc = new Document(stream, options);

        // في هذه المرحلة، يمكننا قراءة محتويات المستند وتحريرها ثم حفظها في نظام الملفات المحلي.
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

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
* class [LoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../loadoptions/)
* المجسم [Aspose.Words](../../../)


