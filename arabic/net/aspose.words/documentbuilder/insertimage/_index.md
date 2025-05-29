---
title: DocumentBuilder.InsertImage
linktitle: InsertImage
articleTitle: InsertImage
second_title: Aspose.Words لـ .NET
description: قم بتعزيز مستنداتك بسهولة باستخدام طريقة InsertImage في DocumentBuilder، مما يسمح بإدراج صور .NET بشكل سلس بالحجم الكامل للحصول على صور مذهلة.
type: docs
weight: 400
url: /ar/net/aspose.words/documentbuilder/insertimage/
---
## InsertImage(*Image*) {#insertimage_3}

إدراج صورة من .NETImage كائن في المستند. الصورة مُدرجة ضمنيًا وبمقياس ١٠٠٪.

```csharp
public Shape InsertImage(Image image)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| image | Image | الصورة التي سيتم إدراجها في المستند. |

### قيمة الإرجاع

عقدة الصورة التي تم إدراجها للتو.

## ملاحظات

يمكنك تغيير حجم الصورة وموقعها وطريقة تحديد الموقع والإعدادات الأخرى باستخدام [`Shape`](../../../aspose.words.drawing/shape/) الكائن الذي تم إرجاعه بواسطة هذه الطريقة.

## أمثلة

يوضح كيفية إدراج صورة من كائن إلى مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFile = ImageDir + "Logo.jpg";

// فيما يلي ثلاث طرق لإدراج صورة من مثيل كائن الصورة.
// 1 - شكل مضمن بحجم افتراضي يعتمد على الأبعاد الأصلية للصورة:
builder.InsertImage(imageFile);

builder.InsertBreak(BreakType.PageBreak);

// 2 - شكل مضمن بأبعاد مخصصة:
builder.InsertImage(imageFile, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - الشكل العائم مع الأبعاد المخصصة:
builder.InsertImage(imageFile, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## InsertImage(*string*) {#insertimage_9}

يُدرج صورة من ملف أو رابط في المستند. تُدرج الصورة مضمنةً وبمقياس ١٠٠٪.

```csharp
public Shape InsertImage(string fileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | الملف الذي يحتوي على الصورة. يمكن أن يكون أي عنوان URI صالح محليًا أو بعيدًا. |

### قيمة الإرجاع

عقدة الصورة التي تم إدراجها للتو.

## ملاحظات

سيؤدي هذا التحميل الزائد إلى تنزيل الصورة تلقائيًا قبل إدراجها في document إذا قمت بتحديد عنوان URI بعيد.

يمكنك تغيير حجم الصورة وموقعها وطريقة تحديد الموقع والإعدادات الأخرى باستخدام [`Shape`](../../../aspose.words.drawing/shape/) الكائن الذي تم إرجاعه بواسطة هذه الطريقة.

## أمثلة

يوضح كيفية إدراج صورة WebP.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "WebP image.webp");

doc.Save(ArtifactsDir + "Image.InsertWebpImage.docx");
```

يوضح كيفية إدراج صورة gif إلى المستند.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// يمكننا إدراج صورة gif باستخدام المسار أو مجموعة البايتات.
// يعمل فقط إذا تم تحسين DocumentBuilder إلى إصدار Word 2010 أو أعلى.
// لاحظ أن الوصول إلى بايتات الصورة يؤدي إلى تحويل Gif إلى Png.
Shape gifImage = builder.InsertImage(ImageDir + "Graphics Interchange Format.gif");

gifImage = builder.InsertImage(File.ReadAllBytes(ImageDir + "Graphics Interchange Format.gif"));

builder.Document.Save(ArtifactsDir + "InsertGif.docx");
```

يوضح كيفية إدراج شكل مع صورة في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي موقعان حيث يتم استخدام طريقة "InsertShape" الخاصة بمنشئ المستندات
//يمكن الحصول على مصدر الصورة التي سيتم عرض الشكل.
// 1 - قم بتمرير اسم ملف نظام الملفات المحلي لملف الصورة:
builder.Write("Image from local file: ");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.Writeln();

// 2 - قم بتمرير عنوان URL الذي يشير إلى صورة.
builder.Write("Image from a URL: ");
builder.InsertImage(ImageUrl);
builder.Writeln();

doc.Save(ArtifactsDir + "Image.FromUrl.docx");
```

يوضح كيفية إدراج صورة عائمة في وسط الصفحة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج صورة عائمة ستظهر خلف النص المتداخل وقم بمحاذاتها مع مركز الصفحة.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

يوضح كيفية تحديد الصورة التي سيتم إدراجها.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Scalable Vector Graphics.svg");

// يقوم Aspose.Words بإدراج صورة SVG في المستند بصيغة PNG مع امتداد svgBlip
// التي تحتوي على تمثيل صورة SVG المتجهة الأصلية.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.SvgWithSvgBlip.docx");

// يقوم Aspose.Words بإدراج صورة SVG في المستند بصيغة PNG، تمامًا كما يفعل Microsoft Word للتنسيق القديم.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.Svg.doc");

doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);

// يقوم Aspose.Words بإدراج صورة SVG في المستند كملف EMF للحفاظ على الصورة في تمثيل متجه.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.Emf.docx");
```

يوضح كيفية إدراج صورة من نظام الملفات المحلي في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي ثلاث طرق لإدراج صورة من اسم ملف النظام المحلي.
// 1 - شكل مضمن بحجم افتراضي يعتمد على الأبعاد الأصلية للصورة:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - شكل مضمن بأبعاد مخصصة:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - الشكل العائم مع الأبعاد المخصصة:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## InsertImage(*Stream*) {#insertimage_6}

يُدرج صورة من تدفق في المستند. تُدرج الصورة مضمنةً وبمقياس ١٠٠٪.

```csharp
public Shape InsertImage(Stream stream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | الدفق الذي يحتوي على الصورة. |

### قيمة الإرجاع

عقدة الصورة التي تم إدراجها للتو.

## ملاحظات

يمكنك تغيير حجم الصورة وموقعها وطريقة تحديد الموقع والإعدادات الأخرى باستخدام [`Shape`](../../../aspose.words.drawing/shape/) الكائن الذي تم إرجاعه بواسطة هذه الطريقة.

## أمثلة

يوضح كيفية إدراج شكل مع صورة من مجرى إلى مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    builder.Write("Image from stream: ");
    builder.InsertImage(stream);
}

doc.Save(ArtifactsDir + "Image.FromStream.docx");
```

يوضح كيفية إدراج صورة من مجرى إلى مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // فيما يلي ثلاث طرق لإدراج صورة من مجرى.
    // 1 - شكل مضمن بحجم افتراضي يعتمد على الأبعاد الأصلية للصورة:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - شكل مضمن بأبعاد مخصصة:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - الشكل العائم مع الأبعاد المخصصة:
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## InsertImage(*byte[]*) {#insertimage}

يُدرج صورة من مصفوفة بايتات في المستند. تُدرج الصورة مضمنةً وبمقياس ١٠٠٪.

```csharp
public Shape InsertImage(byte[] imageBytes)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| imageBytes | Byte[] | مجموعة البايتات التي تحتوي على الصورة. |

### قيمة الإرجاع

عقدة الصورة التي تم إدراجها للتو.

## ملاحظات

يمكنك تغيير حجم الصورة وموقعها وطريقة تحديد الموقع والإعدادات الأخرى باستخدام [`Shape`](../../../aspose.words.drawing/shape/) الكائن الذي تم إرجاعه بواسطة هذه الطريقة.

## أمثلة

يوضح كيفية إدراج صورة من مجموعة بايتات في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

byte[] imageByteArray = TestUtil.ImageToByteArray(ImageDir + "Logo.jpg");

// فيما يلي ثلاث طرق لإدراج صورة من مجموعة بايتات.
// 1 - شكل مضمن بحجم افتراضي يعتمد على الأبعاد الأصلية للصورة:
builder.InsertImage(imageByteArray);

builder.InsertBreak(BreakType.PageBreak);

// 2 - شكل مضمن بأبعاد مخصصة:
builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - الشكل العائم مع الأبعاد المخصصة:
builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## InsertImage(*Image, double, double*) {#insertimage_5}

يقوم بإدراج صورة مضمنة من .NETImage الكائن في المستند ويقوم بتغيير حجمه إلى الحجم المحدد.

```csharp
public Shape InsertImage(Image image, double width, double height)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| image | Image | الصورة التي سيتم إدراجها في المستند. |
| width | Double | عرض الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس ١٠٠٪. |
| height | Double | ارتفاع الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس ١٠٠٪. |

### قيمة الإرجاع

عقدة الصورة التي تم إدراجها للتو.

## ملاحظات

يمكنك تغيير حجم الصورة وموقعها وطريقة تحديد الموقع والإعدادات الأخرى باستخدام [`Shape`](../../../aspose.words.drawing/shape/) الكائن الذي تم إرجاعه بواسطة هذه الطريقة.

## أمثلة

يوضح كيفية إدراج صورة من كائن إلى مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFile = ImageDir + "Logo.jpg";

// فيما يلي ثلاث طرق لإدراج صورة من مثيل كائن الصورة.
// 1 - شكل مضمن بحجم افتراضي يعتمد على الأبعاد الأصلية للصورة:
builder.InsertImage(imageFile);

builder.InsertBreak(BreakType.PageBreak);

// 2 - شكل مضمن بأبعاد مخصصة:
builder.InsertImage(imageFile, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - الشكل العائم مع الأبعاد المخصصة:
builder.InsertImage(imageFile, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## InsertImage(*string, double, double*) {#insertimage_11}

يقوم بإدراج صورة مضمنة من ملف أو عنوان URL في المستند ويقوم بتغيير حجمها إلى الحجم المحدد.

```csharp
public Shape InsertImage(string fileName, double width, double height)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | الملف الذي يحتوي على الصورة. |
| width | Double | عرض الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس ١٠٠٪. |
| height | Double | ارتفاع الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس ١٠٠٪. |

### قيمة الإرجاع

عقدة الصورة التي تم إدراجها للتو.

## ملاحظات

يمكنك تغيير حجم الصورة وموقعها وطريقة تحديد الموقع والإعدادات الأخرى باستخدام [`Shape`](../../../aspose.words.drawing/shape/) الكائن الذي تم إرجاعه بواسطة هذه الطريقة.

## أمثلة

يوضح كيفية إدراج صورة من نظام الملفات المحلي في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي ثلاث طرق لإدراج صورة من اسم ملف النظام المحلي.
// 1 - شكل مضمن بحجم افتراضي يعتمد على الأبعاد الأصلية للصورة:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - شكل مضمن بأبعاد مخصصة:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - الشكل العائم مع الأبعاد المخصصة:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## InsertImage(*Stream, double, double*) {#insertimage_8}

يقوم بإدراج صورة مضمنة من مجرى في المستند ويقوم بتغيير حجمها إلى الحجم المحدد.

```csharp
public Shape InsertImage(Stream stream, double width, double height)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | التيار الذي يحتوي على الصورة. |
| width | Double | عرض الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس ١٠٠٪. |
| height | Double | ارتفاع الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس ١٠٠٪. |

### قيمة الإرجاع

عقدة الصورة التي تم إدراجها للتو.

## ملاحظات

يمكنك تغيير حجم الصورة وموقعها وطريقة تحديد الموقع والإعدادات الأخرى باستخدام [`Shape`](../../../aspose.words.drawing/shape/) الكائن الذي تم إرجاعه بواسطة هذه الطريقة.

## أمثلة

يوضح كيفية إدراج صورة من مجرى إلى مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // فيما يلي ثلاث طرق لإدراج صورة من مجرى.
    // 1 - شكل مضمن بحجم افتراضي يعتمد على الأبعاد الأصلية للصورة:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - شكل مضمن بأبعاد مخصصة:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - الشكل العائم مع الأبعاد المخصصة:
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## InsertImage(*byte[], double, double*) {#insertimage_2}

يقوم بإدراج صورة مضمنة من مجموعة بايتات في المستند ويقوم بتغيير حجمها إلى الحجم المحدد.

```csharp
public Shape InsertImage(byte[] imageBytes, double width, double height)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| imageBytes | Byte[] | مجموعة البايتات التي تحتوي على الصورة. |
| width | Double | عرض الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس ١٠٠٪. |
| height | Double | ارتفاع الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس ١٠٠٪. |

### قيمة الإرجاع

عقدة الصورة التي تم إدراجها للتو.

## ملاحظات

يمكنك تغيير حجم الصورة وموقعها وطريقة تحديد الموقع والإعدادات الأخرى باستخدام [`Shape`](../../../aspose.words.drawing/shape/) الكائن الذي تم إرجاعه بواسطة هذه الطريقة.

## أمثلة

يوضح كيفية إدراج صورة من مجموعة بايتات في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

byte[] imageByteArray = TestUtil.ImageToByteArray(ImageDir + "Logo.jpg");

// فيما يلي ثلاث طرق لإدراج صورة من مجموعة بايتات.
// 1 - شكل مضمن بحجم افتراضي يعتمد على الأبعاد الأصلية للصورة:
builder.InsertImage(imageByteArray);

builder.InsertBreak(BreakType.PageBreak);

// 2 - شكل مضمن بأبعاد مخصصة:
builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - الشكل العائم مع الأبعاد المخصصة:
builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## InsertImage(*Image, [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertimage_4}

إدراج صورة من .NETImage الكائن في الموضع والحجم المحددين.

```csharp
public Shape InsertImage(Image image, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| image | Image | الصورة التي سيتم إدراجها في المستند. |
| horzPos | RelativeHorizontalPosition | يحدد المكان الذي يتم قياس المسافة منه إلى الصورة. |
| left | Double | المسافة بالنقاط من الأصل إلى الجانب الأيسر من الصورة. |
| vertPos | RelativeVerticalPosition | يحدد المكان الذي يتم قياس المسافة منه إلى الصورة. |
| top | Double | المسافة بالنقاط من الأصل إلى الجانب العلوي من الصورة. |
| width | Double | عرض الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس ١٠٠٪. |
| height | Double | ارتفاع الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس ١٠٠٪. |
| wrapType | WrapType | يحدد كيفية لف النص حول الصورة. |

### قيمة الإرجاع

عقدة الصورة التي تم إدراجها للتو.

## ملاحظات

يمكنك تغيير حجم الصورة وموقعها وطريقة تحديد الموقع والإعدادات الأخرى باستخدام [`Shape`](../../../aspose.words.drawing/shape/) الكائن الذي تم إرجاعه بواسطة هذه الطريقة.

## أمثلة

يوضح كيفية إدراج صورة من كائن إلى مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFile = ImageDir + "Logo.jpg";

// فيما يلي ثلاث طرق لإدراج صورة من مثيل كائن الصورة.
// 1 - شكل مضمن بحجم افتراضي يعتمد على الأبعاد الأصلية للصورة:
builder.InsertImage(imageFile);

builder.InsertBreak(BreakType.PageBreak);

// 2 - شكل مضمن بأبعاد مخصصة:
builder.InsertImage(imageFile, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - الشكل العائم مع الأبعاد المخصصة:
builder.InsertImage(imageFile, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## InsertImage(*string, [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertimage_10}

يقوم بإدراج صورة من ملف أو عنوان URL في الموضع والحجم المحددين.

```csharp
public Shape InsertImage(string fileName, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | الملف الذي يحتوي على الصورة. |
| horzPos | RelativeHorizontalPosition | يحدد المكان الذي يتم قياس المسافة منه إلى الصورة. |
| left | Double | المسافة بالنقاط من الأصل إلى الجانب الأيسر من الصورة. |
| vertPos | RelativeVerticalPosition | يحدد المكان الذي يتم قياس المسافة منه إلى الصورة. |
| top | Double | المسافة بالنقاط من الأصل إلى الجانب العلوي من الصورة. |
| width | Double | عرض الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس ١٠٠٪. |
| height | Double | ارتفاع الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس ١٠٠٪. |
| wrapType | WrapType | يحدد كيفية لف النص حول الصورة. |

### قيمة الإرجاع

عقدة الصورة التي تم إدراجها للتو.

## ملاحظات

يمكنك تغيير حجم الصورة وموقعها وطريقة تحديد الموقع والإعدادات الأخرى باستخدام [`Shape`](../../../aspose.words.drawing/shape/) الكائن الذي تم إرجاعه بواسطة هذه الطريقة.

## أمثلة

يوضح كيفية إدراج صورة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// هناك طريقتان لاستخدام منشئ المستندات لتحديد مصدر الصورة ثم إدراجها كشكل عائم.
// 1 - من ملف في نظام الملفات المحلي:
builder.InsertImage(ImageDir + "Transparent background logo.png", RelativeHorizontalPosition.Margin, 100,
    RelativeVerticalPosition.Margin, 0, 200, 200, WrapType.Square);

// 2 - من عنوان URL:
builder.InsertImage(ImageUrl, RelativeHorizontalPosition.Margin, 100,
    RelativeVerticalPosition.Margin, 250, 200, 200, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFloatingImage.docx");
```

يوضح كيفية إدراج صورة من نظام الملفات المحلي في مستند مع الحفاظ على أبعادها.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تقوم طريقة InsertImage بإنشاء شكل عائم بالصورة المرسلة في بيانات صورته.
//يمكننا تحديد أبعاد الشكل عن طريق تمريرها إلى هذه الطريقة.
Shape imageShape = builder.InsertImage(ImageDir + "Logo.jpg", RelativeHorizontalPosition.Margin, 0,
    RelativeVerticalPosition.Margin, 0, -1, -1, WrapType.Square);

// تمرير القيم السلبية كأبعاد مقصودة سيحدد تلقائيًا
// أبعاد الشكل بناءً على أبعاد صورته.
Assert.AreEqual(300.0d, imageShape.Width);
Assert.AreEqual(300.0d, imageShape.Height);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertImageOriginalSize.docx");
```

يوضح كيفية إدراج صورة من نظام الملفات المحلي في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي ثلاث طرق لإدراج صورة من اسم ملف النظام المحلي.
// 1 - شكل مضمن بحجم افتراضي يعتمد على الأبعاد الأصلية للصورة:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - شكل مضمن بأبعاد مخصصة:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - الشكل العائم مع الأبعاد المخصصة:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## InsertImage(*Stream, [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertimage_7}

يقوم بإدراج صورة من مجرى في الموضع والحجم المحددين.

```csharp
public Shape InsertImage(Stream stream, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | التيار الذي يحتوي على الصورة. |
| horzPos | RelativeHorizontalPosition | يحدد المكان الذي يتم قياس المسافة منه إلى الصورة. |
| left | Double | المسافة بالنقاط من الأصل إلى الجانب الأيسر من الصورة. |
| vertPos | RelativeVerticalPosition | يحدد المكان الذي يتم قياس المسافة منه إلى الصورة. |
| top | Double | المسافة بالنقاط من الأصل إلى الجانب العلوي من الصورة. |
| width | Double | عرض الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس ١٠٠٪. |
| height | Double | ارتفاع الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس ١٠٠٪. |
| wrapType | WrapType | يحدد كيفية لف النص حول الصورة. |

### قيمة الإرجاع

عقدة الصورة التي تم إدراجها للتو.

## ملاحظات

يمكنك تغيير حجم الصورة وموقعها وطريقة تحديد الموقع والإعدادات الأخرى باستخدام [`Shape`](../../../aspose.words.drawing/shape/) الكائن الذي تم إرجاعه بواسطة هذه الطريقة.

## أمثلة

يوضح كيفية إدراج صورة من مجرى إلى مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // فيما يلي ثلاث طرق لإدراج صورة من مجرى.
    // 1 - شكل مضمن بحجم افتراضي يعتمد على الأبعاد الأصلية للصورة:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - شكل مضمن بأبعاد مخصصة:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - الشكل العائم مع الأبعاد المخصصة:
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## InsertImage(*byte[], [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertimage_1}

يقوم بإدراج صورة من مجموعة بايتات في الموضع والحجم المحددين.

```csharp
public Shape InsertImage(byte[] imageBytes, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| imageBytes | Byte[] | مجموعة البايتات التي تحتوي على الصورة. |
| horzPos | RelativeHorizontalPosition | يحدد المكان الذي يتم قياس المسافة منه إلى الصورة. |
| left | Double | المسافة بالنقاط من الأصل إلى الجانب الأيسر من الصورة. |
| vertPos | RelativeVerticalPosition | يحدد المكان الذي يتم قياس المسافة منه إلى الصورة. |
| top | Double | المسافة بالنقاط من الأصل إلى الجانب العلوي من الصورة. |
| width | Double | عرض الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس ١٠٠٪. |
| height | Double | ارتفاع الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس ١٠٠٪. |
| wrapType | WrapType | يحدد كيفية لف النص حول الصورة. |

### قيمة الإرجاع

عقدة الصورة التي تم إدراجها للتو.

## ملاحظات

يمكنك تغيير حجم الصورة وموقعها وطريقة تحديد الموقع والإعدادات الأخرى باستخدام [`Shape`](../../../aspose.words.drawing/shape/) الكائن الذي تم إرجاعه بواسطة هذه الطريقة.

## أمثلة

يوضح كيفية إدراج صورة من مجموعة بايتات في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

byte[] imageByteArray = TestUtil.ImageToByteArray(ImageDir + "Logo.jpg");

// فيما يلي ثلاث طرق لإدراج صورة من مجموعة بايتات.
// 1 - شكل مضمن بحجم افتراضي يعتمد على الأبعاد الأصلية للصورة:
builder.InsertImage(imageByteArray);

builder.InsertBreak(BreakType.PageBreak);

// 2 - شكل مضمن بأبعاد مخصصة:
builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - الشكل العائم مع الأبعاد المخصصة:
builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
