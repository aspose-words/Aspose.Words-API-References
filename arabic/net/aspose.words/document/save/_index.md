---
title: Document.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words لـ .NET
description: احفظ مستنداتك بسهولة باستخدام طريقة الحفظ الذكية لدينا، والتي تحدد تلقائيًا التنسيق المناسب استنادًا إلى امتداد الملف لتخزين سلس.
type: docs
weight: 750
url: /ar/net/aspose.words/document/save/
---
## Save(*string*) {#save_2}

يحفظ المستند في ملف. يحدد تلقائيًا تنسيق الحفظ من الامتداد.

```csharp
public SaveOutputParameters Save(string fileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | اسم المستند. إذا كان هناك مستند يحمل اسم الملف المحدد ، فسيتم استبداله. |

### قيمة الإرجاع

معلومات إضافية يمكنك استخدامها اختياريا.

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

### أنظر أيضا

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## Save(*string, [SaveFormat](../../saveformat/)*) {#save_3}

يحفظ المستند في ملف بالتنسيق المحدد.

```csharp
public SaveOutputParameters Save(string fileName, SaveFormat saveFormat)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | اسم المستند. إذا كان هناك مستند يحمل اسم الملف المحدد ، فسيتم استبداله. |
| saveFormat | SaveFormat | التنسيق الذي سيتم حفظ المستند به. |

### قيمة الإرجاع

معلومات إضافية يمكنك استخدامها اختياريا.

## أمثلة

يوضح كيفية التحويل من تنسيق DOCX إلى تنسيق HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToHtml.html", SaveFormat.Html);
```

### أنظر أيضا

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* enum [SaveFormat](../../saveformat/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## Save(*string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#save_4}

يحفظ المستند في ملف باستخدام خيارات الحفظ المحددة.

```csharp
public SaveOutputParameters Save(string fileName, SaveOptions saveOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | اسم المستند. إذا كان هناك مستند يحمل اسم الملف المحدد ، فسيتم استبداله. |
| saveOptions | SaveOptions | يحدد الخيارات التي تتحكم في كيفية حفظ المستند. يمكن`باطل`. |

### قيمة الإرجاع

معلومات إضافية يمكنك استخدامها اختياريا.

## أمثلة

يوضح كيفية تحسين جودة المستند المقدم باستخدام SaveOptions.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 60;
builder.Writeln("Some text.");

SaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
doc.Save(ArtifactsDir + "Document.ImageSaveOptions.Default.jpg", options);

options.UseAntiAliasing = true;
options.UseHighQualityRendering = true;

doc.Save(ArtifactsDir + "Document.ImageSaveOptions.HighQuality.jpg", options);
```

يوضح كيفية تحويل ملف PDF إلى ملف .docx وتخصيص عملية الحفظ باستخدام كائن SaveOptions.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocxCustom.pdf");

// قم بتحميل مستند PDF الذي قمنا بحفظه للتو، وقم بتحويله إلى .docx.
Document pdfDoc = new Document(ArtifactsDir + "PDF2Word.ConvertPdfToDocxCustom.pdf");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);

// قم بتعيين خاصية "كلمة المرور" لتشفير المستند المحفوظ بكلمة مرور.
saveOptions.Password = "MyPassword";

pdfDoc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocxCustom.docx", saveOptions);
```

يوضح كيفية عرض كل صفحة من المستند إلى صورة TIFF منفصلة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// قم بإنشاء كائن "ImageSaveOptions" الذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل الطريقة التي تقوم بها هذه الطريقة بتحويل المستند إلى صورة.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

for (int i = 0; i < doc.PageCount; i++)
{
    // اضبط خاصية "PageSet" على رقم الصفحة الأولى من
    // الذي سيتم البدء في عرض المستند منه.
    options.PageSet = new PageSet(i);
    // تصدير الصفحة بدقة 2325 × 5325 بكسل و 600 نقطة في البوصة.
    options.Resolution = 600;
    options.ImageSize = new Size(2325, 5325);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

يوضح كيفية عرض صفحة واحدة من مستند إلى صورة JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// قم بإنشاء كائن "ImageSaveOptions" الذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل الطريقة التي تقوم بها هذه الطريقة بتحويل المستند إلى صورة.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
// اضبط "PageSet" على "1" لتحديد الصفحة الثانية عبر
// الفهرس المبني على الصفر لبدء عرض المستند منه.
options.PageSet = new PageSet(1);

// عندما نحفظ المستند بتنسيق JPEG، يقوم Aspose.Words بعرض صفحة واحدة فقط.
// ستحتوي هذه الصورة على صفحة واحدة بدءًا من الصفحة الثانية،
// والتي ستكون فقط الصفحة الثانية من المستند الأصلي.
doc.Save(ArtifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

يوضح كيفية تكوين الضغط أثناء حفظ مستند بتنسيق JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// قم بإنشاء كائن "ImageSaveOptions" الذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل الطريقة التي تقوم بها هذه الطريقة بتحويل المستند إلى صورة.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);
// قم بضبط خاصية "JpegQuality" على "10" لاستخدام ضغط أقوى عند عرض المستند.
// سيؤدي هذا إلى تقليل حجم ملف المستند، ولكن الصورة ستعرض آثار ضغط أكثر وضوحًا.
imageOptions.JpegQuality = 10;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// قم بضبط خاصية "JpegQuality" على "100" لاستخدام ضغط أضعف عند عرض المستند.
// سيؤدي هذا إلى تحسين جودة الصورة على حساب زيادة حجم الملف.
imageOptions.JpegQuality = 100;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

يوضح كيفية تحويل مستند كامل إلى PDF بثلاثة مستويات في مخطط المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إدراج عناوين المستويات من 1 إلى 5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;

builder.Writeln("Heading 1.2.2.1");
builder.Writeln("Heading 1.2.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.2.2.2.1");
builder.Writeln("Heading 1.2.2.2.2");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// سيحتوي مستند PDF الناتج على مخطط تفصيلي، وهو عبارة عن جدول محتويات يسرد العناوين الموجودة في نص المستند.
// النقر على إدخال في هذا المخطط سيأخذنا إلى موقع العنوان الخاص به.
// قم بضبط خاصية "HeadingsOutlineLevels" على "4" لاستبعاد جميع العناوين التي تكون مستوياتها أعلى من 4 من المخطط التفصيلي.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// إذا كان إدخال المخطط التفصيلي يحتوي على إدخالات لاحقة بمستوى أعلى بينها وبين الإدخال التالي من نفس المستوى أو المستوى الأدنى،
// سيظهر سهم على يسار المُدخلة. هذه المُدخلة هي "مالكة" العديد من هذه "المُدخلات الفرعية".
// في مستندنا، تعتبر إدخالات المخطط التفصيلي من مستوى العنوان الخامس إدخالات فرعية لإدخال المخطط التفصيلي الثاني من المستوى الرابع،
// إدخالات المستوى الرابع والخامس هي إدخالات فرعية للإدخال الثاني على المستوى الثالث، وهكذا.
// في المخطط التفصيلي، يمكننا النقر على سهم إدخال "المالك" لإخفاء/توسيع جميع إدخالاته الفرعية.
// اضبط خاصية "ExpandedOutlineLevels" على "2" لتوسيع جميع عناوين المستوى 2 وإدخالات المخطط التفصيلي السفلية تلقائيًا
// وانهيار جميع الإدخالات من المستوى 3 وما فوق عندما نفتح المستند.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### أنظر أيضا

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## Save(*Stream, [SaveFormat](../../saveformat/)*) {#save}

يحفظ المستند في مجرى باستخدام التنسيق المحدد.

```csharp
public SaveOutputParameters Save(Stream stream, SaveFormat saveFormat)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | حدد المكان الذي تريد حفظ المستند فيه. |
| saveFormat | SaveFormat | التنسيق الذي سيتم حفظ المستند به. |

### قيمة الإرجاع

معلومات إضافية يمكنك استخدامها اختياريا.

## أمثلة

يوضح كيفية حفظ مستند في مجرى.

```csharp
Document doc = new Document(MyDir + "Document.docx");

using (MemoryStream dstStream = new MemoryStream())
{
    doc.Save(dstStream, SaveFormat.Docx);

    // تأكد من أن الدفق يحتوي على المستند.
    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", new Document(dstStream).GetText().Trim());
}
```

يوضح كيفية حفظ مستند في صورة عبر التدفق، ثم قراءة الصورة من هذا التدفق.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Font.Name = "Times New Roman";
            builder.Font.Size = 24;
            builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

            builder.InsertImage(ImageDir + "Logo.jpg");

#if NET461_OR_GREATER || JAVA
            using (MemoryStream stream = new MemoryStream())
            {
                doc.Save(stream, SaveFormat.Bmp);

                stream.Position = 0;

                // قراءة التدفق مرة أخرى في صورة.
                using (Image image = Image.FromStream(stream))
                {
                    Assert.AreEqual(ImageFormat.Bmp, image.RawFormat);
                    Assert.AreEqual(816, image.Width);
                    Assert.AreEqual(1056, image.Height);
                }
            }
#elif NET5_0_OR_GREATER
            using (MemoryStream stream = new MemoryStream())
            {
                doc.Save(stream, SaveFormat.Bmp);

                stream.Position = 0;

                SKCodec codec = SKCodec.Create(stream);
                Assert.AreEqual(SKEncodedImageFormat.Bmp, codec.EncodedFormat);

                stream.Position = 0;

                using (SKBitmap image = SKBitmap.Decode(stream))
                {
                    Assert.AreEqual(816, image.Width);
                    Assert.AreEqual(1056, image.Height);
                }
            }
#endif
```

### أنظر أيضا

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* enum [SaveFormat](../../saveformat/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## Save(*Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#save_1}

يحفظ المستند في مجرى باستخدام خيارات الحفظ المحددة.

```csharp
public SaveOutputParameters Save(Stream stream, SaveOptions saveOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | حدد المكان الذي تريد حفظ المستند فيه. |
| saveOptions | SaveOptions | يحدد الخيارات التي تتحكم في كيفية حفظ المستند. يمكن`باطل` . إذا كان هذا هو`باطل`سيتم حفظ المستند بتنسيق DOC الثنائي. |

### قيمة الإرجاع

معلومات إضافية يمكنك استخدامها اختياريا.

## أمثلة

يوضح كيفية تحويل بعض الصفحات فقط في مستند إلى PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

using (Stream stream = File.Create(ArtifactsDir + "PdfSaveOptions.OnePage.pdf"))
{
    // قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
    // لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
    PdfSaveOptions options = new PdfSaveOptions();

    // قم بتعيين "PageIndex" إلى "1" لعرض جزء من المستند بدءًا من الصفحة الثانية.
    options.PageSet = new PageSet(1);

    // ستحتوي هذه الوثيقة على صفحة واحدة بدءًا من الصفحة الثانية، والتي ستحتوي فقط على الصفحة الثانية.
    doc.Save(stream, options);
}
```

### أنظر أيضا

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## Save(*HttpResponse, string, [ContentDisposition](../../contentdisposition/), [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#save_5}

يرسل المستند إلى متصفح العميل.

```csharp
public SaveOutputParameters Save(HttpResponse response, string fileName, 
    ContentDisposition contentDisposition, SaveOptions saveOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| response | HttpResponse | كائن الاستجابة حيث يتم حفظ المستند. |
| fileName | String | اسم المستند الذي سيظهر في متصفح العميل. لا ينبغي أن يحتوي الاسم على مسار. |
| contentDisposition | ContentDisposition | أ[`ContentDisposition`](../../contentdisposition/) القيمة that تحدد كيفية عرض المستند في متصفح العميل. |
| saveOptions | SaveOptions | يحدد الخيارات التي تتحكم في كيفية حفظ المستند. يمكن`باطل`. |

### قيمة الإرجاع

معلومات إضافية يمكنك استخدامها اختياريا.

## ملاحظات

داخليًا، تقوم هذه الطريقة بالحفظ في مجرى الذاكرة أولاً ثم نسخها إلى مجرى الاستجابة لأن مجرى الاستجابة لا يدعم البحث.

## أمثلة

يوضح كيفية تنفيذ عملية دمج البريد، ثم حفظ المستند في متصفح العميل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD FullName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Company ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Address ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

doc.MailMerge.Execute(new string[] { "FullName", "Company", "Address", "City" },
    new object[] { "James Bond", "MI5 Headquarters", "Milbank", "London" });

//إرسال المستند إلى متصفح العميل.
//تم إلقاؤه لأن HttpResponse فارغ في الاختبار.
Assert.Throws<ArgumentNullException>(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null));

// سوف نحتاج إلى إغلاق هذه الاستجابة يدويًا للتأكد من عدم إضافة أي محتوى غير ضروري إلى المستند بعد الحفظ.
Assert.Throws<NullReferenceException>(() => response.End());
```

### أنظر أيضا

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* enum [ContentDisposition](../../contentdisposition/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
