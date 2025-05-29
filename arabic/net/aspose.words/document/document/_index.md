---
title: Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words لـ .NET
description: أنشئ مستندات وورد فارغة بكل سهولة باستخدام مُنشئ المستندات سهل الاستخدام. بسّط عملية كتابتك اليوم!
type: docs
weight: 10
url: /ar/net/aspose.words/document/document/
---
## Document() {#constructor}

ينشئ مستند Word فارغًا.

```csharp
public Document()
```

## ملاحظات

يتم استرداد مستند فارغ من الموارد، وبشكل افتراضي، يبدو المستند الناتج أكثر مثل الذي تم إنشاؤه بواسطةWord2007. تحتوي هذه الوثيقة الفارغة على جدول الخطوط الافتراضية، والأنماط الافتراضية الدنيا، والأنماط الكامنة.

[`OptimizeFor`](../../../aspose.words.settings/compatibilityoptions/optimizefor/) يمكن استخدام الطريقة لتحسين محتويات المستند بالإضافة إلى سلوك Aspose.Words الافتراضي لإصدار معين من MS Word.

حجم ورق المستند الافتراضي هو Letter. لتغيير إعدادات الصفحة، استخدم [`PageSetup`](../../section/pagesetup/).

بعد الإنشاء، يمكنك استخدام[`DocumentBuilder`](../../documentbuilder/) لإضافة محتوى المستند بسهولة.

## أمثلة

يوضح كيفية تنسيق سلسلة من النص باستخدام خاصية الخط الخاصة به.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

يوضح كيفية إنشاء مستند بسيط.

```csharp
Document doc = new Document();

// تأتي كائنات المستند الجديد بشكل افتراضي مع الحد الأدنى من مجموعة العقد
// مطلوب لبدء إضافة محتوى مثل النص والأشكال: قسم، ونص، وفقرة.
doc.AppendChild(new Section(doc))
    .AppendChild(new Body(doc))
    .AppendChild(new Paragraph(doc))
    .AppendChild(new Run(doc, "Hello world!"));
```

يوضح كيفية إنشاء المستندات وتحميلها.

```csharp
// هناك طريقتان لإنشاء كائن مستند باستخدام Aspose.Words.
// 1 - إنشاء مستند فارغ:
Document doc = new Document();

// تأتي كائنات المستند الجديد بشكل افتراضي مع الحد الأدنى من مجموعة العقد
// مطلوب لبدء إضافة محتوى مثل النص والأشكال: قسم، ونص، وفقرة.
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 - تحميل مستند موجود في نظام الملفات المحلي:
doc = new Document(MyDir + "Document.docx");

// ستحتوي المستندات المحملة على محتويات يمكننا الوصول إليها وتحريرها.
Assert.AreEqual("Hello World!", doc.FirstSection.Body.FirstParagraph.GetText().Trim());

// بعض العمليات التي يجب أن تحدث أثناء التحميل، مثل استخدام كلمة مرور لفك تشفير مستند،
//يمكن القيام بذلك عن طريق تمرير كائن LoadOptions عند تحميل المستند.
doc = new Document(MyDir + "Encrypted.docx", new LoadOptions("docPassword"));

Assert.AreEqual("Test encrypted document.", doc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## Document(*string*) {#constructor_3}

يفتح مستندًا موجودًا من ملف. يكتشف تنسيق الملف تلقائيًا.

```csharp
public Document(string fileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | اسم ملف المستند الذي سيتم فتحه. |

### استثناءات

| استثناء | حالة |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | لم يتم التعرف على تنسيق المستند أو لم يتم دعمه. |
| [FileCorruptedException](../../filecorruptedexception/) | يبدو أن المستند تالف ولا يمكن تحميله. |
| Exception | هناك مشكلة في المستند ويجب الإبلاغ عنها إلى مطوري Aspose.Words. |
| IOException | هناك استثناء الإدخال/الإخراج. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | تم تشفير المستند ويتطلب كلمة مرور لفتحه، ولكنك أدخلت كلمة مرور غير صحيحة. |
| ArgumentException | لا يمكن أن يكون اسم الملف فارغًا أو سلسلة فارغة. |

## أمثلة

يوضح كيفية فتح مستند وتحويله إلى صيغة .PDF.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToPdf.pdf");
```

يوضح كيفية تحويل ملف PDF إلى .docx.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

// قم بتحميل مستند PDF الذي قمنا بحفظه للتو، وقم بتحويله إلى .docx.
Document pdfDoc = new Document(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

pdfDoc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.docx");
```

يوضح كيفية تحميل ملف PDF.

```csharp
Document doc = new Aspose.Words.Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

// فيما يلي طريقتان لتحميل مستندات PDF باستخدام منتجات Aspose.
// 1 - التحميل كمستند Aspose.Words:
Document asposeWordsDoc = new Document(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

Assert.AreEqual("Hello world!", asposeWordsDoc.GetText().Trim());

// 2 - التحميل كمستند Aspose.Pdf:
Aspose.Pdf.Document asposePdfDoc = new Aspose.Pdf.Document(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

TextFragmentAbsorber textFragmentAbsorber = new TextFragmentAbsorber();
asposePdfDoc.Pages.Accept(textFragmentAbsorber);

Assert.AreEqual("Hello world!", textFragmentAbsorber.Text.Trim());
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## Document(*string, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_4}

يفتح مستندًا موجودًا من ملف. يسمح بتحديد خيارات إضافية، مثل كلمة مرور التشفير.

```csharp
public Document(string fileName, LoadOptions loadOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | اسم ملف المستند الذي سيتم فتحه. |
| loadOptions | LoadOptions | خيارات إضافية لاستخدامها عند تحميل مستند. يمكن`باطل`. |

### استثناءات

| استثناء | حالة |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | لم يتم التعرف على تنسيق المستند أو لم يتم دعمه. |
| [FileCorruptedException](../../filecorruptedexception/) | يبدو أن المستند تالف ولا يمكن تحميله. |
| Exception | هناك مشكلة في المستند ويجب الإبلاغ عنها إلى مطوري Aspose.Words. |
| IOException | هناك استثناء الإدخال/الإخراج. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | تم تشفير المستند ويتطلب كلمة مرور لفتحه، ولكنك أدخلت كلمة مرور غير صحيحة. |
| ArgumentException | لا يمكن أن يكون اسم الملف فارغًا أو سلسلة فارغة. |

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

يوضح كيفية إنشاء المستندات وتحميلها.

```csharp
// هناك طريقتان لإنشاء كائن مستند باستخدام Aspose.Words.
// 1 - إنشاء مستند فارغ:
Document doc = new Document();

// تأتي كائنات المستند الجديد بشكل افتراضي مع الحد الأدنى من مجموعة العقد
// مطلوب لبدء إضافة محتوى مثل النص والأشكال: قسم، ونص، وفقرة.
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 - تحميل مستند موجود في نظام الملفات المحلي:
doc = new Document(MyDir + "Document.docx");

// ستحتوي المستندات المحملة على محتويات يمكننا الوصول إليها وتحريرها.
Assert.AreEqual("Hello World!", doc.FirstSection.Body.FirstParagraph.GetText().Trim());

// بعض العمليات التي يجب أن تحدث أثناء التحميل، مثل استخدام كلمة مرور لفك تشفير مستند،
//يمكن القيام بذلك عن طريق تمرير كائن LoadOptions عند تحميل المستند.
doc = new Document(MyDir + "Encrypted.docx", new LoadOptions("docPassword"));

Assert.AreEqual("Test encrypted document.", doc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### أنظر أيضا

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## Document(*Stream*) {#constructor_1}

يفتح مستندًا موجودًا من مصدر. يكتشف تنسيق الملف تلقائيًا.

```csharp
public Document(Stream stream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | قم بتحديد المكان الذي سيتم تحميل المستند منه. |

### استثناءات

| استثناء | حالة |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | لم يتم التعرف على تنسيق المستند أو لم يتم دعمه. |
| [FileCorruptedException](../../filecorruptedexception/) | يبدو أن المستند تالف ولا يمكن تحميله. |
| Exception | هناك مشكلة في المستند ويجب الإبلاغ عنها إلى مطوري Aspose.Words. |
| IOException | هناك استثناء الإدخال/الإخراج. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | تم تشفير المستند ويتطلب كلمة مرور لفتحه، ولكنك أدخلت كلمة مرور غير صحيحة. |
| ArgumentNullException | لا يمكن أن يكون الدفق فارغًا. |
| NotSupportedException | لا يدعم البث القراءة أو البحث. |
| ObjectDisposedException | الدفق هو كائن متصرف. |

## ملاحظات

يجب تخزين المستند في بداية الدفق. يجب أن يدعم الدفق التموضع العشوائي.

## أمثلة

يوضح كيفية تحميل مستند باستخدام تيار.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.docx"))
{
    Document doc = new Document(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

يوضح كيفية تحميل مستند من عنوان URL.

```csharp
// قم بإنشاء عنوان URL يشير إلى مستند Microsoft Word.
const string url = "https://filesamples.com/samples/document/docx/sample3.docx";

// قم بتنزيل المستند إلى مصفوفة بايتات، ثم قم بتحميل تلك المصفوفة إلى مستند باستخدام مجرى الذاكرة.
using (WebClient webClient = new WebClient())
{
    byte[] dataBytes = webClient.DownloadData(url);

    using (MemoryStream byteStream = new MemoryStream(dataBytes))
    {
        Document doc = new Document(byteStream);

        // في هذه المرحلة، يمكننا قراءة محتويات المستند وتحريرها ثم حفظها في نظام الملفات المحلي.
        Assert.AreEqual("There are eight section headings in this document. At the beginning, \"Sample Document\" is a level 1 heading. " +
                        "The main section headings, such as \"Headings\" and \"Lists\" are level 2 headings. " +
                        "The Tables section contains two sub-headings, \"Simple Table\" and \"Complex Table,\" which are both level 3 headings.",
            doc.FirstSection.Body.Paragraphs[3].GetText().Trim());

        doc.Save(ArtifactsDir + "Document.LoadFromWeb.docx");
    }
}
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## Document(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_2}

يفتح مستندًا موجودًا من مصدر. يسمح بتحديد خيارات إضافية، مثل كلمة مرور التشفير.

```csharp
public Document(Stream stream, LoadOptions loadOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | المصدر الذي سيتم تحميل المستند منه. |
| loadOptions | LoadOptions | خيارات إضافية لاستخدامها عند تحميل مستند. يمكن`باطل`. |

### استثناءات

| استثناء | حالة |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | لم يتم التعرف على تنسيق المستند أو لم يتم دعمه. |
| [FileCorruptedException](../../filecorruptedexception/) | يبدو أن المستند تالف ولا يمكن تحميله. |
| Exception | هناك مشكلة في المستند ويجب الإبلاغ عنها إلى مطوري Aspose.Words. |
| IOException | هناك استثناء الإدخال/الإخراج. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | تم تشفير المستند ويتطلب كلمة مرور لفتحه، ولكنك أدخلت كلمة مرور غير صحيحة. |
| ArgumentNullException | لا يمكن أن يكون الدفق فارغًا. |
| NotSupportedException | لا يدعم البث القراءة أو البحث. |
| ObjectDisposedException | الدفق هو كائن متصرف. |

## ملاحظات

يجب تخزين المستند في بداية الدفق. يجب أن يدعم الدفق التموضع العشوائي.

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

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
