---
title: DocumentBuilder.InsertImage
second_title: Aspose.Words لمراجع .NET API
description: DocumentBuilder طريقة. لإدراج صورة من .NETImage في المستند. تم إدراج الصورة في السطر وبمقياس 100.
type: docs
weight: 350
url: /ar/net/aspose.words/documentbuilder/insertimage/
---
## InsertImage(Image) {#insertimage_3}

لإدراج صورة من .NETImage في المستند. تم إدراج الصورة في السطر وبمقياس 100٪.

```csharp
public Shape InsertImage(Image image)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| image | Image | الصورة المراد إدراجها في المستند. |

### قيمة الإرجاع

عقدة الصورة التي تم إدراجها للتو.

### ملاحظات

يمكنك تغيير حجم الصورة والموقع وطريقة تحديد المواقع والإعدادات الأخرى باستخدام [`Shape`](../../../aspose.words.drawing/shape/) تم إرجاع الكائن بهذه الطريقة.

### أمثلة

يوضح كيفية إدراج صورة من كائن في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

// فيما يلي ثلاث طرق لإدراج صورة من مثيل كائن صورة.
// 1 - شكل مضمن بحجم افتراضي بناءً على أبعاد الصورة الأصلية:
builder.InsertImage(image);

builder.InsertBreak(BreakType.PageBreak);

// 2 - شكل مضمّن بأبعاد مخصصة:
builder.InsertImage(image, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - شكل عائم بأبعاد مخصصة:
builder.InsertImage(image, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)

---

## InsertImage(string) {#insertimage_9}

يقوم بإدراج صورة من ملف أو عنوان URL في المستند. تم إدراج الصورة في السطر وبمقياس 100٪.

```csharp
public Shape InsertImage(string fileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | الملف مع الصورة. يمكن أن يكون أي URI محليًا أو بعيدًا صالحًا. |

### قيمة الإرجاع

عقدة الصورة التي تم إدراجها للتو.

### ملاحظات

سيؤدي هذا التحميل الزائد إلى تنزيل الصورة تلقائيًا قبل إدراجها في document إذا قمت بتحديد URI بعيد.

يمكنك تغيير حجم الصورة والموقع وطريقة تحديد المواقع والإعدادات الأخرى باستخدام [`Shape`](../../../aspose.words.drawing/shape/) تم إرجاع الكائن بهذه الطريقة.

### أمثلة

يوضح كيفية إدراج صورة gif في المستند.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// يمكننا إدراج صورة gif باستخدام مسار أو مصفوفة بايت.
// يعمل فقط إذا تم تحسين DocumentBuilder إلى إصدار Word 2010 أو إصدار أعلى.
// لاحظ أن الوصول إلى بايت الصورة يؤدي إلى تحويل Gif إلى Png.
Shape gifImage = builder.InsertImage(ImageDir + "Graphics Interchange Format.gif");

gifImage = builder.InsertImage(File.ReadAllBytes(ImageDir + "Graphics Interchange Format.gif"));

builder.Document.Save(ArtifactsDir + "InsertGif.docx");
```

يوضح كيفية إدراج شكل مع صورة في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يوجد أدناه موقعان حيث توجد طريقة "InsertShape" الخاصة بمنشئ المستندات
// يمكن أن مصدر الصورة التي سيعرضها الشكل.
// 1 - قم بتمرير اسم ملف نظام ملفات محلي لملف صورة:
builder.Write("Image from local file: ");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.Writeln();

// 2 - قم بتمرير عنوان URL يشير إلى صورة.
builder.Write("Image from a URL: ");
builder.InsertImage(ImageUrl);
builder.Writeln();

doc.Save(ArtifactsDir + "Image.FromUrl.docx");
```

يوضح كيفية إدراج صورة عائمة في وسط الصفحة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل صورة عائمة ستظهر خلف النص المتداخل وقم بمحاذاة مركز الصفحة.
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

// Aspose.Words إدراج صورة SVG في المستند بصيغة PNG بامتداد svgBlip
// الذي يحتوي على تمثيل صورة SVG المتجه الأصلي.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.SvgWithSvgBlip.docx");

// Aspose.Words بإدراج صورة SVG في المستند بصيغة PNG ، تمامًا كما يفعل Microsoft Word للتنسيق القديم.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.Svg.doc");

doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);

// Aspose.Words إدراج صورة SVG في المستند كملف تعريف EMF للحفاظ على الصورة في تمثيل متجه.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.Emf.docx");
```

يوضح كيفية إدراج صورة من نظام الملفات المحلي في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي ثلاث طرق لإدراج صورة من اسم ملف نظام محلي.
// 1 - شكل مضمن بحجم افتراضي بناءً على أبعاد الصورة الأصلية:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - شكل مضمّن بأبعاد مخصصة:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - شكل عائم بأبعاد مخصصة:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)

---

## InsertImage(Stream) {#insertimage_6}

لإدراج صورة من دفق في المستند. تم إدراج الصورة في السطر وبمقياس 100٪.

```csharp
public Shape InsertImage(Stream stream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | الدفق الذي يحتوي على الصورة. |

### قيمة الإرجاع

عقدة الصورة التي تم إدراجها للتو.

### ملاحظات

يمكنك تغيير حجم الصورة والموقع وطريقة تحديد المواقع والإعدادات الأخرى باستخدام [`Shape`](../../../aspose.words.drawing/shape/) تم إرجاع الكائن بهذه الطريقة.

### أمثلة

يوضح كيفية إدراج شكل مع صورة من تدفق إلى مستند.

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

يوضح كيفية إدراج صورة من دفق في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // فيما يلي ثلاث طرق لإدراج صورة من التدفق.
    // 1 - شكل مضمن بحجم افتراضي بناءً على أبعاد الصورة الأصلية:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - شكل مضمّن بأبعاد مخصصة:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - شكل عائم بأبعاد مخصصة:
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)

---

## InsertImage(byte[]) {#insertimage}

لإدراج صورة من مصفوفة بايت في المستند. تم إدراج الصورة في السطر وبمقياس 100٪.

```csharp
public Shape InsertImage(byte[] imageBytes)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| imageBytes | Byte[] | مصفوفة البايت التي تحتوي على الصورة. |

### قيمة الإرجاع

عقدة الصورة التي تم إدراجها للتو.

### ملاحظات

يمكنك تغيير حجم الصورة والموقع وطريقة تحديد المواقع والإعدادات الأخرى باستخدام [`Shape`](../../../aspose.words.drawing/shape/) تم إرجاع الكائن بهذه الطريقة.

### أمثلة

يوضح كيفية إدراج صورة من مصفوفة بايت في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

using (MemoryStream ms = new MemoryStream())
{
    image.Save(ms, ImageFormat.Png);
    byte[] imageByteArray = ms.ToArray();

    // فيما يلي ثلاث طرق لإدراج صورة من مصفوفة بايت.
    // 1 - شكل مضمن بحجم افتراضي بناءً على أبعاد الصورة الأصلية:
    builder.InsertImage(imageByteArray);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - شكل مضمّن بأبعاد مخصصة:
    builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - شكل عائم بأبعاد مخصصة:
    builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin, 
    100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

يوضح كيفية إدراج صورة من مصفوفة بايت في مستند (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// سيؤدي فك تشفير الصورة إلى تحويلها إلى تنسيق .png.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    using (SKImage image = SKImage.FromBitmap(bitmap))
    {
        using (SKData data = image.Encode())
        {
            byte[] imageByteArray = data.ToArray();

            // فيما يلي ثلاث طرق لإدراج صورة من مصفوفة بايت.
            // 1 - شكل مضمن بحجم افتراضي بناءً على أبعاد الصورة الأصلية:
            builder.InsertImage(imageByteArray);

            builder.InsertBreak(BreakType.PageBreak);

            // 2 - شكل مضمّن بأبعاد مخصصة:
            builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

            builder.InsertBreak(BreakType.PageBreak);

            // 3 - شكل عائم بأبعاد مخصصة:
            builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
                100, 200, 100, WrapType.Square);
        }
    }
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArrayNetStandard2.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)

---

## InsertImage(Image, double, double) {#insertimage_5}

إدراج صورة مضمنة من .NETImage في المستند وقياسه إلى الحجم المحدد.

```csharp
public Shape InsertImage(Image image, double width, double height)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| image | Image | الصورة المراد إدراجها في المستند. |
| width | Double | عرض الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس بنسبة 100٪. |
| height | Double | ارتفاع الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس بنسبة 100٪. |

### قيمة الإرجاع

عقدة الصورة التي تم إدراجها للتو.

### ملاحظات

يمكنك تغيير حجم الصورة والموقع وطريقة تحديد المواقع والإعدادات الأخرى باستخدام [`Shape`](../../../aspose.words.drawing/shape/) تم إرجاع الكائن بهذه الطريقة.

### أمثلة

يوضح كيفية إدراج صورة من كائن في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

// فيما يلي ثلاث طرق لإدراج صورة من مثيل كائن صورة.
// 1 - شكل مضمن بحجم افتراضي بناءً على أبعاد الصورة الأصلية:
builder.InsertImage(image);

builder.InsertBreak(BreakType.PageBreak);

// 2 - شكل مضمّن بأبعاد مخصصة:
builder.InsertImage(image, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - شكل عائم بأبعاد مخصصة:
builder.InsertImage(image, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

يوضح كيفية إدراج صورة من كائن في مستند (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// سيؤدي فك تشفير الصورة إلى تحويلها إلى تنسيق .png.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    // فيما يلي ثلاث طرق لإدراج صورة من مثيل كائن صورة.
    // 1 - شكل مضمن بحجم افتراضي بناءً على أبعاد الصورة الأصلية:
    builder.InsertImage(bitmap);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - شكل مضمّن بأبعاد مخصصة:
    builder.InsertImage(bitmap, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - شكل عائم بأبعاد مخصصة:
    builder.InsertImage(bitmap, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObjectNetStandard2.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)

---

## InsertImage(string, double, double) {#insertimage_11}

إدراج صورة مضمنة من ملف أو عنوان URL في المستند وقياسها إلى الحجم المحدد.

```csharp
public Shape InsertImage(string fileName, double width, double height)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | الملف الذي يحتوي على الصورة. |
| width | Double | عرض الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس بنسبة 100٪. |
| height | Double | ارتفاع الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس بنسبة 100٪. |

### قيمة الإرجاع

عقدة الصورة التي تم إدراجها للتو.

### ملاحظات

يمكنك تغيير حجم الصورة والموقع وطريقة تحديد المواقع والإعدادات الأخرى باستخدام [`Shape`](../../../aspose.words.drawing/shape/) تم إرجاع الكائن بهذه الطريقة.

### أمثلة

يوضح كيفية إدراج صورة من نظام الملفات المحلي في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي ثلاث طرق لإدراج صورة من اسم ملف نظام محلي.
// 1 - شكل مضمن بحجم افتراضي بناءً على أبعاد الصورة الأصلية:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - شكل مضمّن بأبعاد مخصصة:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - شكل عائم بأبعاد مخصصة:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)

---

## InsertImage(Stream, double, double) {#insertimage_8}

إدراج صورة مضمنة من دفق في المستند وقياسها إلى الحجم المحدد .

```csharp
public Shape InsertImage(Stream stream, double width, double height)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | الدفق الذي يحتوي على الصورة. |
| width | Double | عرض الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس بنسبة 100٪. |
| height | Double | ارتفاع الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس بنسبة 100٪. |

### قيمة الإرجاع

عقدة الصورة التي تم إدراجها للتو.

### ملاحظات

يمكنك تغيير حجم الصورة والموقع وطريقة تحديد المواقع والإعدادات الأخرى باستخدام [`Shape`](../../../aspose.words.drawing/shape/) تم إرجاع الكائن بهذه الطريقة.

### أمثلة

يوضح كيفية إدراج صورة من دفق في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // فيما يلي ثلاث طرق لإدراج صورة من التدفق.
    // 1 - شكل مضمن بحجم افتراضي بناءً على أبعاد الصورة الأصلية:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - شكل مضمّن بأبعاد مخصصة:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - شكل عائم بأبعاد مخصصة:
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)

---

## InsertImage(byte[], double, double) {#insertimage_2}

إدراج صورة مضمنة من مصفوفة بايت في المستند وقياسها إلى الحجم المحدد.

```csharp
public Shape InsertImage(byte[] imageBytes, double width, double height)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| imageBytes | Byte[] | مصفوفة البايت التي تحتوي على الصورة. |
| width | Double | عرض الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس بنسبة 100٪. |
| height | Double | ارتفاع الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس بنسبة 100٪. |

### قيمة الإرجاع

عقدة الصورة التي تم إدراجها للتو.

### ملاحظات

يمكنك تغيير حجم الصورة والموقع وطريقة تحديد المواقع والإعدادات الأخرى باستخدام [`Shape`](../../../aspose.words.drawing/shape/) تم إرجاع الكائن بهذه الطريقة.

### أمثلة

يوضح كيفية إدراج صورة من مصفوفة بايت في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

using (MemoryStream ms = new MemoryStream())
{
    image.Save(ms, ImageFormat.Png);
    byte[] imageByteArray = ms.ToArray();

    // فيما يلي ثلاث طرق لإدراج صورة من مصفوفة بايت.
    // 1 - شكل مضمن بحجم افتراضي بناءً على أبعاد الصورة الأصلية:
    builder.InsertImage(imageByteArray);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - شكل مضمّن بأبعاد مخصصة:
    builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - شكل عائم بأبعاد مخصصة:
    builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin, 
    100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

يوضح كيفية إدراج صورة من مصفوفة بايت في مستند (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// سيؤدي فك تشفير الصورة إلى تحويلها إلى تنسيق .png.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    using (SKImage image = SKImage.FromBitmap(bitmap))
    {
        using (SKData data = image.Encode())
        {
            byte[] imageByteArray = data.ToArray();

            // فيما يلي ثلاث طرق لإدراج صورة من مصفوفة بايت.
            // 1 - شكل مضمن بحجم افتراضي بناءً على أبعاد الصورة الأصلية:
            builder.InsertImage(imageByteArray);

            builder.InsertBreak(BreakType.PageBreak);

            // 2 - شكل مضمّن بأبعاد مخصصة:
            builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

            builder.InsertBreak(BreakType.PageBreak);

            // 3 - شكل عائم بأبعاد مخصصة:
            builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
                100, 200, 100, WrapType.Square);
        }
    }
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArrayNetStandard2.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)

---

## InsertImage(Image, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertimage_4}

لإدراج صورة من .NETImage كائن في الموضع والحجم المحددين .

```csharp
public Shape InsertImage(Image image, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| image | Image | الصورة المراد إدراجها في المستند. |
| horzPos | RelativeHorizontalPosition | يحدد مكان قياس المسافة إلى الصورة. |
| left | Double | المسافة بالنقاط من نقطة الأصل إلى الجانب الأيسر من الصورة. |
| vertPos | RelativeVerticalPosition | يحدد المكان الذي تم قياس المسافة منه إلى الصورة. |
| top | Double | المسافة بالنقاط من نقطة الأصل إلى الجانب العلوي للصورة. |
| width | Double | عرض الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس بنسبة 100٪. |
| height | Double | ارتفاع الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس بنسبة 100٪. |
| wrapType | WrapType | يحدد كيفية التفاف النص حول الصورة. |

### قيمة الإرجاع

عقدة الصورة التي تم إدراجها للتو.

### ملاحظات

يمكنك تغيير حجم الصورة والموقع وطريقة تحديد المواقع والإعدادات الأخرى باستخدام [`Shape`](../../../aspose.words.drawing/shape/) تم إرجاع الكائن بهذه الطريقة.

### أمثلة

يوضح كيفية إدراج صورة من كائن في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

// فيما يلي ثلاث طرق لإدراج صورة من مثيل كائن صورة.
// 1 - شكل مضمن بحجم افتراضي بناءً على أبعاد الصورة الأصلية:
builder.InsertImage(image);

builder.InsertBreak(BreakType.PageBreak);

// 2 - شكل مضمّن بأبعاد مخصصة:
builder.InsertImage(image, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - شكل عائم بأبعاد مخصصة:
builder.InsertImage(image, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

يوضح كيفية إدراج صورة من كائن في مستند (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// سيؤدي فك تشفير الصورة إلى تحويلها إلى تنسيق .png.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    // فيما يلي ثلاث طرق لإدراج صورة من مثيل كائن صورة.
    // 1 - شكل مضمن بحجم افتراضي بناءً على أبعاد الصورة الأصلية:
    builder.InsertImage(bitmap);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - شكل مضمّن بأبعاد مخصصة:
    builder.InsertImage(bitmap, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - شكل عائم بأبعاد مخصصة:
    builder.InsertImage(bitmap, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObjectNetStandard2.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)

---

## InsertImage(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertimage_10}

إدراج صورة من ملف أو عنوان URL في الموضع والحجم المحددين.

```csharp
public Shape InsertImage(string fileName, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | الملف الذي يحتوي على الصورة. |
| horzPos | RelativeHorizontalPosition | يحدد مكان قياس المسافة إلى الصورة. |
| left | Double | المسافة بالنقاط من نقطة الأصل إلى الجانب الأيسر من الصورة. |
| vertPos | RelativeVerticalPosition | يحدد المكان الذي تم قياس المسافة منه إلى الصورة. |
| top | Double | المسافة بالنقاط من نقطة الأصل إلى الجانب العلوي للصورة. |
| width | Double | عرض الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس بنسبة 100٪. |
| height | Double | ارتفاع الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس بنسبة 100٪. |
| wrapType | WrapType | يحدد كيفية التفاف النص حول الصورة. |

### قيمة الإرجاع

عقدة الصورة التي تم إدراجها للتو.

### ملاحظات

يمكنك تغيير حجم الصورة والموقع وطريقة تحديد المواقع والإعدادات الأخرى باستخدام [`Shape`](../../../aspose.words.drawing/shape/) تم إرجاع الكائن بهذه الطريقة.

### أمثلة

يوضح كيفية إدراج صورة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// هناك طريقتان لاستخدام منشئ المستندات لمصدر صورة ثم إدراجها كشكل عائم.
// 1 - من ملف في نظام الملفات المحلي:
builder.InsertImage(ImageDir + "Transparent background logo.png", RelativeHorizontalPosition.Margin, 100,
    RelativeVerticalPosition.Margin, 0, 200, 200, WrapType.Square);

// 2 - من عنوان URL:
builder.InsertImage(ImageUrl, RelativeHorizontalPosition.Margin, 100,
    RelativeVerticalPosition.Margin, 250, 200, 200, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFloatingImage.docx");
```

يوضح كيفية إدراج صورة من نظام الملفات المحلي في مستند مع الاحتفاظ بأبعادها.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تقوم طريقة InsertImage بإنشاء شكل عائم مع الصورة التي تم تمريرها في بيانات الصورة الخاصة بها.
// يمكننا تحديد أبعاد الشكل ويمكن تمريرها إلى هذه الطريقة.
Shape imageShape = builder.InsertImage(ImageDir + "Logo.jpg", RelativeHorizontalPosition.Margin, 0,
    RelativeVerticalPosition.Margin, 0, -1, -1, WrapType.Square);

// تمرير القيم السالبة كما سيتم تحديد الأبعاد المقصودة تلقائيًا
// أبعاد الشكل بناءً على أبعاد صورته.
Assert.AreEqual(300.0d, imageShape.Width);
Assert.AreEqual(300.0d, imageShape.Height);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertImageOriginalSize.docx");
```

يوضح كيفية إدراج صورة من نظام الملفات المحلي في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي ثلاث طرق لإدراج صورة من اسم ملف نظام محلي.
// 1 - شكل مضمن بحجم افتراضي بناءً على أبعاد الصورة الأصلية:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - شكل مضمّن بأبعاد مخصصة:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - شكل عائم بأبعاد مخصصة:
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
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)

---

## InsertImage(Stream, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertimage_7}

لإدراج صورة من تيار في الموضع والحجم المحددين.

```csharp
public Shape InsertImage(Stream stream, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | الدفق الذي يحتوي على الصورة. |
| horzPos | RelativeHorizontalPosition | يحدد مكان قياس المسافة إلى الصورة. |
| left | Double | المسافة بالنقاط من نقطة الأصل إلى الجانب الأيسر من الصورة. |
| vertPos | RelativeVerticalPosition | يحدد المكان الذي تم قياس المسافة منه إلى الصورة. |
| top | Double | المسافة بالنقاط من نقطة الأصل إلى الجانب العلوي للصورة. |
| width | Double | عرض الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس بنسبة 100٪. |
| height | Double | ارتفاع الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس بنسبة 100٪. |
| wrapType | WrapType | يحدد كيفية التفاف النص حول الصورة. |

### قيمة الإرجاع

عقدة الصورة التي تم إدراجها للتو.

### ملاحظات

يمكنك تغيير حجم الصورة والموقع وطريقة تحديد المواقع والإعدادات الأخرى باستخدام [`Shape`](../../../aspose.words.drawing/shape/) تم إرجاع الكائن بهذه الطريقة.

### أمثلة

يوضح كيفية إدراج صورة من دفق في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // فيما يلي ثلاث طرق لإدراج صورة من التدفق.
    // 1 - شكل مضمن بحجم افتراضي بناءً على أبعاد الصورة الأصلية:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - شكل مضمّن بأبعاد مخصصة:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - شكل عائم بأبعاد مخصصة:
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
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)

---

## InsertImage(byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertimage_1}

إدراج صورة من مصفوفة بايت في الموضع والحجم المحددين.

```csharp
public Shape InsertImage(byte[] imageBytes, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| imageBytes | Byte[] | مصفوفة البايت التي تحتوي على الصورة. |
| horzPos | RelativeHorizontalPosition | يحدد مكان قياس المسافة إلى الصورة. |
| left | Double | المسافة بالنقاط من نقطة الأصل إلى الجانب الأيسر من الصورة. |
| vertPos | RelativeVerticalPosition | يحدد المكان الذي تم قياس المسافة منه إلى الصورة. |
| top | Double | المسافة بالنقاط من نقطة الأصل إلى الجانب العلوي للصورة. |
| width | Double | عرض الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس بنسبة 100٪. |
| height | Double | ارتفاع الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس بنسبة 100٪. |
| wrapType | WrapType | يحدد كيفية التفاف النص حول الصورة. |

### قيمة الإرجاع

عقدة الصورة التي تم إدراجها للتو.

### ملاحظات

يمكنك تغيير حجم الصورة والموقع وطريقة تحديد المواقع والإعدادات الأخرى باستخدام [`Shape`](../../../aspose.words.drawing/shape/) تم إرجاع الكائن بهذه الطريقة.

### أمثلة

يوضح كيفية إدراج صورة من مصفوفة بايت في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

using (MemoryStream ms = new MemoryStream())
{
    image.Save(ms, ImageFormat.Png);
    byte[] imageByteArray = ms.ToArray();

    // فيما يلي ثلاث طرق لإدراج صورة من مصفوفة بايت.
    // 1 - شكل مضمن بحجم افتراضي بناءً على أبعاد الصورة الأصلية:
    builder.InsertImage(imageByteArray);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - شكل مضمّن بأبعاد مخصصة:
    builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - شكل عائم بأبعاد مخصصة:
    builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin, 
    100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

يوضح كيفية إدراج صورة من مصفوفة بايت في مستند (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// سيؤدي فك تشفير الصورة إلى تحويلها إلى تنسيق .png.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    using (SKImage image = SKImage.FromBitmap(bitmap))
    {
        using (SKData data = image.Encode())
        {
            byte[] imageByteArray = data.ToArray();

            // فيما يلي ثلاث طرق لإدراج صورة من مصفوفة بايت.
            // 1 - شكل مضمن بحجم افتراضي بناءً على أبعاد الصورة الأصلية:
            builder.InsertImage(imageByteArray);

            builder.InsertBreak(BreakType.PageBreak);

            // 2 - شكل مضمّن بأبعاد مخصصة:
            builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

            builder.InsertBreak(BreakType.PageBreak);

            // 3 - شكل عائم بأبعاد مخصصة:
            builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
                100, 200, 100, WrapType.Square);
        }
    }
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArrayNetStandard2.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)


