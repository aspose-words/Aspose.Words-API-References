---
title: Document
second_title: Aspose.Words لمراجع .NET API
description: إنشاء مستند Word فارغ .
type: docs
weight: 10
url: /ar/net/aspose.words/document/document/
---
## Document() {#constructor}

إنشاء مستند Word فارغ .

```csharp
public Document()
```

### ملاحظات

حجم ورق المستند هو Letter افتراضيًا. إذا كنت تريد تغيير إعداد الصفحة ، فاستخدم [`القسم. إعداد الصفحة`](../../section/pagesetup/).

بعد الإنشاء ، يمكنك استخدام ملفات[`DocumentBuilder`](../../documentbuilder/) لإضافة محتوى الوثيقة بسهولة.

### أمثلة

يوضح كيفية تنسيق مجموعة من النص باستخدام خاصية الخط الخاصة به.

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

يوضح كيفية إنشاء المستندات وتحميلها.

```csharp
// هناك طريقتان لإنشاء كائن مستند باستخدام Aspose.Words.
// 1 - إنشاء مستند فارغ:
Document doc = new Document();

// كائنات المستند الجديد بشكل افتراضي تأتي مع الحد الأدنى من مجموعة العقد
// مطلوب لبدء إضافة محتوى مثل النص والأشكال: قسم ، ونص ، وفقرة.
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 - تحميل مستند موجود في نظام الملفات المحلي:
doc = new Document(MyDir + "Document.docx");

// ستحتوي المستندات المحملة على محتويات يمكننا الوصول إليها وتحريرها.
Assert.AreEqual("Hello World!", doc.FirstSection.Body.FirstParagraph.GetText().Trim());

// بعض العمليات التي يجب أن تحدث أثناء التحميل ، مثل استخدام كلمة مرور لفك تشفير مستند ،
// يمكن أن يتم عن طريق تمرير كائن LoadOptions عند تحميل المستند.
doc = new Document(MyDir + "Encrypted.docx", new LoadOptions("docPassword"));

Assert.AreEqual("Test encrypted document.", doc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)

---

## Document(string) {#constructor_3}

يفتح وثيقة موجودة من ملف. يكتشف تنسيق الملف تلقائيًا.

```csharp
public Document(string fileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | اسم ملف المستند المراد فتحه. |

### استثناءات

| استثناء | حالة |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | تنسيق المستند غير معروف أو غير مدعوم. |
| [FileCorruptedException](../../filecorruptedexception/) | يبدو أن المستند تالف ولا يمكن تحميله. |
| Exception | توجد مشكلة في المستند ويجب إبلاغ مطوري Aspose.Words بها. |
| IOException | هناك استثناء الإدخال / الإخراج. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | المستند مشفر ويتطلب كلمة مرور لفتحه ، لكنك أدخلت كلمة مرور غير صحيحة. |
| ArgumentException | لا يمكن أن يكون اسم الملف سلسلة فارغة أو فارغة. |

### أمثلة

يوضح كيفية فتح مستند وتحويله إلى PDF.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToPdf.pdf");
```

يوضح كيفية تحويل ملف PDF إلى ملف docx.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

// قم بتحميل مستند PDF الذي حفظناه للتو ، وقم بتحويله إلى .docx.
Document pdfDoc = new Document(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

pdfDoc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.docx");
```

يوضح كيفية تحميل ملف PDF.

```csharp
Aspose.Words.Document doc = new Aspose.Words.Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

// فيما يلي طريقتان لتحميل مستندات PDF باستخدام منتجات Aspose.
// 1 - التحميل كوثيقة Aspose.Words:
Aspose.Words.Document asposeWordsDoc = new Aspose.Words.Document(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

Assert.AreEqual("Hello world!", asposeWordsDoc.GetText().Trim());

// 2 - تحميل كمستند Aspose.Pdf:
Aspose.Pdf.Document asposePdfDoc = new Aspose.Pdf.Document(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

TextFragmentAbsorber textFragmentAbsorber = new TextFragmentAbsorber();
asposePdfDoc.Pages.Accept(textFragmentAbsorber);

Assert.AreEqual("Hello world!", textFragmentAbsorber.Text.Trim());
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)

---

## Document(string, LoadOptions) {#constructor_4}

يفتح وثيقة موجودة من ملف. يسمح بتحديد خيارات إضافية مثل كلمة مرور التشفير.

```csharp
public Document(string fileName, LoadOptions loadOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | اسم ملف المستند المراد فتحه. |
| loadOptions | LoadOptions | خيارات إضافية لاستخدامها عند تحميل مستند. يمكن أن تكون خالية. |

### استثناءات

| استثناء | حالة |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | تنسيق المستند غير معروف أو غير مدعوم. |
| [FileCorruptedException](../../filecorruptedexception/) | يبدو أن المستند تالف ولا يمكن تحميله. |
| Exception | توجد مشكلة في المستند ويجب إبلاغ مطوري Aspose.Words بها. |
| IOException | هناك استثناء الإدخال / الإخراج. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | المستند مشفر ويتطلب كلمة مرور لفتحه ، لكنك أدخلت كلمة مرور غير صحيحة. |
| ArgumentException | لا يمكن أن يكون اسم الملف سلسلة فارغة أو فارغة. |

### أمثلة

يوضح كيفية تحميل مستند Microsoft Word مشفر.

```csharp
Document doc;

// Aspose.Words استثناء إذا حاولنا فتح مستند مشفر بدون كلمة المرور الخاصة به.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// عند تحميل مثل هذا المستند ، يتم تمرير كلمة المرور إلى مُنشئ المستند باستخدام كائن LoadOptions.
LoadOptions options = new LoadOptions("docPassword");

// هناك طريقتان لتحميل مستند مشفر باستخدام كائن LoadOptions.
// 1 - قم بتحميل المستند من نظام الملفات المحلي حسب اسم الملف:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - تحميل المستند من دفق:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
```

يوضح كيفية إنشاء المستندات وتحميلها.

```csharp
// هناك طريقتان لإنشاء كائن مستند باستخدام Aspose.Words.
// 1 - إنشاء مستند فارغ:
Document doc = new Document();

// كائنات المستند الجديد بشكل افتراضي تأتي مع الحد الأدنى من مجموعة العقد
// مطلوب لبدء إضافة محتوى مثل النص والأشكال: قسم ، ونص ، وفقرة.
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 - تحميل مستند موجود في نظام الملفات المحلي:
doc = new Document(MyDir + "Document.docx");

// ستحتوي المستندات المحملة على محتويات يمكننا الوصول إليها وتحريرها.
Assert.AreEqual("Hello World!", doc.FirstSection.Body.FirstParagraph.GetText().Trim());

// بعض العمليات التي يجب أن تحدث أثناء التحميل ، مثل استخدام كلمة مرور لفك تشفير مستند ،
// يمكن أن يتم عن طريق تمرير كائن LoadOptions عند تحميل المستند.
doc = new Document(MyDir + "Encrypted.docx", new LoadOptions("docPassword"));

Assert.AreEqual("Test encrypted document.", doc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### أنظر أيضا

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)

---

## Document(Stream) {#constructor_1}

يفتح مستندًا موجودًا من دفق. يكتشف تنسيق الملف تلقائيًا.

```csharp
public Document(Stream stream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | دفق مكان تحميل المستند منه. |

### استثناءات

| استثناء | حالة |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | تنسيق المستند غير معروف أو غير مدعوم. |
| [FileCorruptedException](../../filecorruptedexception/) | يبدو أن المستند تالف ولا يمكن تحميله. |
| Exception | توجد مشكلة في المستند ويجب إبلاغ مطوري Aspose.Words بها. |
| IOException | هناك استثناء الإدخال / الإخراج. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | المستند مشفر ويتطلب كلمة مرور لفتحه ، لكنك أدخلت كلمة مرور غير صحيحة. |
| ArgumentNullException | لا يمكن أن يكون الدفق فارغًا. |
| NotSupportedException | الدفق لا يدعم القراءة أو البحث. |
| ObjectDisposedException | الدفق هو كائن تم التخلص منه. |

### ملاحظات

يجب تخزين المستند في بداية الدفق. يجب أن يدعم الدفق تحديد المواقع العشوائية.

### أمثلة

يوضح كيفية تحميل مستند باستخدام دفق.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.docx"))
{
    Document doc = new Document(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

يوضح كيفية تحميل مستند من عنوان URL.

```csharp
// أنشئ عنوان URL يشير إلى مستند Microsoft Word.
const string url = "https://omextemplates.content.office.net/support/templates/en-us/tf16402488.dotx ";

// قم بتنزيل المستند في مصفوفة بايت ، ثم قم بتحميل هذه المجموعة في مستند باستخدام تدفق الذاكرة.
using (WebClient webClient = new WebClient())
{
    byte[] dataBytes = webClient.DownloadData(url);

    using (MemoryStream byteStream = new MemoryStream(dataBytes))
    {
        Document doc = new Document(byteStream);

        // في هذه المرحلة ، يمكننا قراءة محتويات المستند وتحريرها ثم حفظها في نظام الملفات المحلي.
        Assert.AreEqual("Use this section to highlight your relevant passions, activities, and how you like to give back. " +
                        "It’s good to include Leadership and volunteer experiences here. " +
                        "Or show off important extras like publications, certifications, languages and more.",
            doc.FirstSection.Body.Paragraphs[4].GetText().Trim());

        doc.Save(ArtifactsDir + "Document.LoadFromWeb.docx");
    }
}
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)

---

## Document(Stream, LoadOptions) {#constructor_2}

يفتح مستندًا موجودًا من دفق. يسمح بتحديد خيارات إضافية مثل كلمة مرور التشفير.

```csharp
public Document(Stream stream, LoadOptions loadOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | الدفق الذي سيتم تحميل المستند منه. |
| loadOptions | LoadOptions | خيارات إضافية لاستخدامها عند تحميل مستند. يمكن أن تكون خالية. |

### استثناءات

| استثناء | حالة |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | تنسيق المستند غير معروف أو غير مدعوم. |
| [FileCorruptedException](../../filecorruptedexception/) | يبدو أن المستند تالف ولا يمكن تحميله. |
| Exception | توجد مشكلة في المستند ويجب إبلاغ مطوري Aspose.Words بها. |
| IOException | هناك استثناء الإدخال / الإخراج. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | المستند مشفر ويتطلب كلمة مرور لفتحه ، لكنك أدخلت كلمة مرور غير صحيحة. |
| ArgumentNullException | لا يمكن أن يكون الدفق فارغًا. |
| NotSupportedException | الدفق لا يدعم القراءة أو البحث. |
| ObjectDisposedException | الدفق هو كائن تم التخلص منه. |

### ملاحظات

يجب تخزين المستند في بداية الدفق. يجب أن يدعم الدفق تحديد المواقع العشوائية.

### أمثلة

يوضح كيفية حفظ صفحة ويب كملف docx.

```csharp
const string url = "http://www.aspose.com/ ";

using (WebClient client = new WebClient()) 
{ 
    using (MemoryStream stream = new MemoryStream(client.DownloadData(url)))
    {
        // يتم استخدام عنوان URL مرة أخرى باعتباره baseUri لضمان استرداد أي مسارات صور ذات صلة بشكل صحيح.
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // قم بتحميل مستند HTML من الدفق وتمرير كائن LoadOptions.
        Document doc = new Document(stream, options);

        // في هذه المرحلة ، يمكننا قراءة محتويات المستند وتحريرها ثم حفظها في نظام الملفات المحلي.
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

يوضح كيفية فتح مستند HTML بصور من دفق باستخدام URI أساسي.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // قم بتمرير URI للمجلد الأساسي أثناء تحميله
    // بحيث يمكن العثور على أي صور ذات URIs ذات صلة في مستند HTML.
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

يوضح كيفية تحميل مستند Microsoft Word مشفر.

```csharp
Document doc;

// Aspose.Words استثناء إذا حاولنا فتح مستند مشفر بدون كلمة المرور الخاصة به.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// عند تحميل مثل هذا المستند ، يتم تمرير كلمة المرور إلى مُنشئ المستند باستخدام كائن LoadOptions.
LoadOptions options = new LoadOptions("docPassword");

// هناك طريقتان لتحميل مستند مشفر باستخدام كائن LoadOptions.
// 1 - قم بتحميل المستند من نظام الملفات المحلي حسب اسم الملف:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - تحميل المستند من دفق:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
```

### أنظر أيضا

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
