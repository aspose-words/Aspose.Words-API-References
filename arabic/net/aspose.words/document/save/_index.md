---
title: Document.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words لـ .NET
description: Document Save طريقة. يحفظ المستند في ملف. يحدد تنسيق الحفظ تلقائيًا من الامتداد في C#.
type: docs
weight: 700
url: /ar/net/aspose.words/document/save/
---
## Save(*string*) {#save_2}

يحفظ المستند في ملف. يحدد تنسيق الحفظ تلقائيًا من الامتداد.

```csharp
public SaveOutputParameters Save(string fileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | اسم الوثيقة. إذا كان هناك مستند يحمل اسم الملف المحدد موجود بالفعل، فسيتم الكتابة فوق المستند الموجود. |

### قيمة الإرجاع

معلومات إضافية يمكنك استخدامها اختياريًا.

## أمثلة

يوضح كيفية فتح مستند وتحويله إلى .PDF.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToPdf.pdf");
```

يوضح كيفية تحويل ملف PDF إلى ملف .docx.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

// قم بتحميل مستند PDF الذي حفظناه للتو، وقم بتحويله إلى .docx.
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
| fileName | String | اسم الوثيقة. إذا كان هناك مستند يحمل اسم الملف المحدد موجود بالفعل، فسيتم الكتابة فوق المستند الموجود. |
| saveFormat | SaveFormat | التنسيق الذي سيتم حفظ المستند به. |

### قيمة الإرجاع

معلومات إضافية يمكنك استخدامها اختياريًا.

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
| fileName | String | اسم الوثيقة. إذا كان هناك مستند يحمل اسم الملف المحدد موجود بالفعل، فسيتم الكتابة فوق المستند الموجود. |
| saveOptions | SaveOptions | يحدد الخيارات التي تتحكم في كيفية حفظ المستند. يمكن ان يكون`باطل`. |

### قيمة الإرجاع

معلومات إضافية يمكنك استخدامها اختياريًا.

## أمثلة

يوضح كيفية تحسين جودة المستند المعروض باستخدام SaveOptions.

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

// قم بتحميل مستند PDF الذي حفظناه للتو، وقم بتحويله إلى .docx.
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

// أنشئ كائن "ImageSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل الطريقة التي تعرض بها هذه الطريقة المستند إلى صورة.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

for (int i = 0; i < doc.PageCount; i++)
{
    // قم بتعيين خاصية "PageSet" على رقم الصفحة الأولى من
    // الذي يبدأ عرض المستند منه.
    options.PageSet = new PageSet(i);
    // تصدير الصفحة بحجم 2325 × 5325 بكسل و600 نقطة في البوصة.
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

// أنشئ كائن "ImageSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل الطريقة التي تعرض بها هذه الطريقة المستند إلى صورة.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);

// اضبط "PageSet" على "1" لتحديد الصفحة الثانية عبر
// الفهرس الصفري الذي سيتم البدء في عرض المستند منه.
options.PageSet = new PageSet(1);

// عندما نحفظ المستند بتنسيق JPEG، يعرض Aspose.Words صفحة واحدة فقط.
// ستحتوي هذه الصورة على صفحة واحدة تبدأ من الصفحة الثانية،
// والتي ستكون مجرد الصفحة الثانية من المستند الأصلي.
doc.Save(ArtifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

يوضح كيفية تكوين الضغط أثناء حفظ مستند بتنسيق JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// أنشئ كائن "ImageSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل الطريقة التي تعرض بها هذه الطريقة المستند إلى صورة.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);

// اضبط خاصية "JpegQuality" على "10" لاستخدام ضغط أقوى عند عرض المستند.
// سيؤدي هذا إلى تقليل حجم ملف المستند، لكن الصورة ستعرض عناصر ضغط أكثر وضوحًا.
imageOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg").Length));

// اضبط خاصية "JpegQuality" على "100" لاستخدام ضغط أضعف عند تقطيع المستند.
// سيؤدي هذا إلى تحسين جودة الصورة على حساب زيادة حجم الملف.
imageOptions.JpegQuality = 100;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

Assert.That(60000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg").Length));
```

يوضح كيفية تحويل مستند كامل إلى PDF بثلاثة مستويات في مخطط المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل عناوين المستويات من 1 إلى 5.
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

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// سيحتوي مستند PDF الناتج على مخطط تفصيلي، وهو عبارة عن جدول محتويات يسرد العناوين في نص المستند.
// سيؤدي النقر فوق أحد الإدخالات في هذا المخطط إلى نقلنا إلى موقع العنوان الخاص به.
// قم بتعيين خاصية "HeadingsOutlineLevels" على "4" لاستبعاد كافة العناوين التي تكون مستوياتها أعلى من 4 من المخطط التفصيلي.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// إذا كان الإدخال التفصيلي يحتوي على إدخالات لاحقة بمستوى أعلى بينه وبين الإدخال التالي من نفس المستوى أو مستوى أقل،
// سيظهر سهم على يسار الإدخال. هذا الإدخال هو "مالك" العديد من هذه "الإدخالات الفرعية".
// في مستندنا، إدخالات المخطط التفصيلي من مستوى العنوان الخامس هي إدخالات فرعية لإدخال المخطط التفصيلي للمستوى الرابع الثاني،
// إدخالات مستوى العنوان الرابع والخامس هي إدخالات فرعية لإدخال المستوى الثالث الثاني، وهكذا.
// في المخطط التفصيلي، يمكننا النقر على سهم إدخال "المالك" لطي/توسيع جميع إدخالاته الفرعية.
// قم بتعيين خاصية "ExpandedOutlineLevels" على "2" لتوسيع كل مستوى العناوين 2 وإدخالات المخطط التفصيلي السفلية تلقائيًا
// وقم بطي جميع المستويات والإدخالات الثلاثة والأعلى عندما نفتح المستند.
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

يحفظ المستند في دفق باستخدام التنسيق المحدد.

```csharp
public SaveOutputParameters Save(Stream stream, SaveFormat saveFormat)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | تيار حيث لحفظ المستند. |
| saveFormat | SaveFormat | التنسيق الذي سيتم حفظ المستند به. |

### قيمة الإرجاع

معلومات إضافية يمكنك استخدامها اختياريًا.

## أمثلة

يوضح كيفية حفظ مستند في الدفق.

```csharp
Document doc = new Document(MyDir + "Document.docx");

using (MemoryStream dstStream = new MemoryStream())
{
    doc.Save(dstStream, SaveFormat.Docx);

    // تحقق من أن الدفق يحتوي على المستند.
    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", new Document(dstStream).GetText().Trim());
}
```

يوضح كيفية حفظ مستند في صورة عبر الدفق، ثم قراءة الصورة من هذا الدفق.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Font.Name = "Times New Roman";
            builder.Font.Size = 24;
            builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

            builder.InsertImage(ImageDir + "Logo.jpg");

#if NET48 || JAVA
            using (MemoryStream stream = new MemoryStream())
            {
                doc.Save(stream, SaveFormat.Bmp);

                stream.Position = 0;

                // اقرأ الدفق مرة أخرى في الصورة.
                using (Image image = Image.FromStream(stream))
                {
                    Assert.AreEqual(ImageFormat.Bmp, image.RawFormat);
                    Assert.AreEqual(816, image.Width);
                    Assert.AreEqual(1056, image.Height);
                }
            }
#elif NET5_0_OR_GREATER || __MOBILE__
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

يحفظ المستند في دفق باستخدام خيارات الحفظ المحددة.

```csharp
public SaveOutputParameters Save(Stream stream, SaveOptions saveOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | تيار حيث لحفظ المستند. |
| saveOptions | SaveOptions | يحدد الخيارات التي تتحكم في كيفية حفظ المستند. يمكن ان يكون`باطل` . إذا كان هذا`باطل`سيتم حفظ المستند بتنسيق DOC الثنائي. |

### قيمة الإرجاع

معلومات إضافية يمكنك استخدامها اختياريًا.

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
    // قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
    // لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
    PdfSaveOptions options = new PdfSaveOptions();

    // اضبط "PageIndex" على "1" لعرض جزء من المستند بدءًا من الصفحة الثانية.
    options.PageSet = new PageSet(1);

    // سيحتوي هذا المستند على صفحة واحدة تبدأ من الصفحة الثانية، والتي ستحتوي على الصفحة الثانية فقط.
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
| fileName | String | اسم المستند الذي سيظهر في متصفح العميل. يجب ألا يحتوي الاسم على مسار. |
| contentDisposition | ContentDisposition | أ[`ContentDisposition`](../../contentdisposition/)تحدد القيمة that كيفية عرض المستند في متصفح العميل. |
| saveOptions | SaveOptions | يحدد الخيارات التي تتحكم في كيفية حفظ المستند. يمكن ان يكون`باطل`. |

### قيمة الإرجاع

معلومات إضافية يمكنك استخدامها اختياريًا.

## ملاحظات

داخليًا، تقوم هذه الطريقة بالحفظ في دفق الذاكرة أولاً ثم نسخها إلى دفق الاستجابة لأن دفق الاستجابة لا يدعم البحث.

## أمثلة

يوضح كيفية إجراء دمج البريد، ثم حفظ المستند في مستعرض العميل.

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

// أرسل المستند إلى متصفح العميل.
Assert.That(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null),
    Throws.TypeOf<ArgumentNullException>()); // تم طرحه لأن HttpResponse فارغ في الاختبار.

// سنحتاج إلى إغلاق هذه الاستجابة يدويًا للتأكد من أننا لا نضيف أي محتوى غير ضروري إلى المستند بعد الحفظ.
Assert.That(() => response.End(), Throws.TypeOf<NullReferenceException>());
```

### أنظر أيضا

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* enum [ContentDisposition](../../contentdisposition/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
