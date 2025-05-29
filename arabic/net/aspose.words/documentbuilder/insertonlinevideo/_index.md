---
title: DocumentBuilder.InsertOnlineVideo
linktitle: InsertOnlineVideo
articleTitle: InsertOnlineVideo
second_title: Aspose.Words لـ .NET
description: قم بإضافة مقاطع الفيديو عبر الإنترنت وتوسيع نطاقها بسهولة في مستنداتك باستخدام طريقة InsertOnlineVideo من DocumentBuilder لتعزيز المشاركة والإبداع.
type: docs
weight: 440
url: /ar/net/aspose.words/documentbuilder/insertonlinevideo/
---
## InsertOnlineVideo(*string, [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertonlinevideo}

يقوم بإدراج كائن فيديو عبر الإنترنت في المستند ويقوم بتغيير حجمه إلى الحجم المحدد.

```csharp
public Shape InsertOnlineVideo(string videoUrl, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| videoUrl | String | عنوان URL للفيديو. |
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

يتم دعم إدراج الفيديو عبر الإنترنت من الموارد التالية:

* https://www.youtube.com/
* https://vimeo.com/

إذا لم يتم عرض مقطع الفيديو الخاص بك عبر الإنترنت بشكل صحيح، فاستخدم`InsertOnlineVideo`، والذي يقبل كود HTML المضمن المخصص.

قد يختلف كود تضمين الفيديو بين مقدمي الخدمة، لذا استشر مقدم الخدمة المناسب لك للحصول على التفاصيل.

## أمثلة

يوضح كيفية إدراج مقطع فيديو عبر الإنترنت في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";

// إدراج شكل يقوم بتشغيل مقطع فيديو من الويب عند النقر فوقه في Microsoft Word.
// سيحتوي هذا الشكل المستطيل على صورة بناءً على الإطار الأول من الفيديو المرتبط
// وإشارة مرئية لزر التشغيل. نسبة عرض الفيديو إلى ارتفاعه 16:9.
// سوف نقوم بضبط حجم الشكل على هذه النسبة، حتى لا تظهر الصورة ممتدة.
builder.InsertOnlineVideo(videoUrl, RelativeHorizontalPosition.LeftMargin, 0,
    RelativeVerticalPosition.TopMargin, 0, 320, 180, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOnlineVideo.docx");
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

## InsertOnlineVideo(*string, string, byte[], double, double*) {#insertonlinevideo_3}

يقوم بإدراج كائن فيديو عبر الإنترنت في المستند ويقوم بتغيير حجمه إلى الحجم المحدد.

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    double width, double height)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| videoUrl | String | عنوان URL للفيديو. |
| videoEmbedCode | String | كود التضمين للفيديو. |
| thumbnailImageBytes | Byte[] | بايتات الصورة المصغرة. |
| width | Double | عرض الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس ١٠٠٪. |
| height | Double | ارتفاع الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس ١٠٠٪. |

### قيمة الإرجاع

عقدة الصورة التي تم إدراجها للتو.

## ملاحظات

يمكنك تغيير حجم الصورة وموقعها وطريقة تحديد الموقع والإعدادات الأخرى باستخدام [`Shape`](../../../aspose.words.drawing/shape/) الكائن الذي تم إرجاعه بواسطة هذه الطريقة.

## أمثلة

يوضح كيفية إدراج مقطع فيديو عبر الإنترنت في مستند باستخدام صورة مصغرة مخصصة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";
string videoEmbedCode =
    "<iframe src=\"https://player.vimeo.com/video/52477838\" العرض=\"640\" الارتفاع=\"360\" حدود الإطار=\"0\" " +
    "title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

byte[] thumbnailImageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(thumbnailImageBytes))
{
    using (Image image = Image.FromStream(stream))
    {
        // فيما يلي طريقتان لإنشاء شكل باستخدام صورة مصغرة مخصصة، والتي ترتبط بمقطع فيديو عبر الإنترنت
        //هذا ما سيتم تشغيله عندما نضغط على الشكل في Microsoft Word.
        // 1 - إدراج شكل مضمن في مؤشر إدراج عقدة المنشئ:
        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image.Width, image.Height);

        builder.InsertBreak(BreakType.PageBreak);

        // 2 - إدراج شكل عائم:
        double left = builder.PageSetup.RightMargin - image.Width;
        double top = builder.PageSetup.BottomMargin - image.Height;

        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes,
            RelativeHorizontalPosition.RightMargin, left, RelativeVerticalPosition.BottomMargin, top,
            image.Width, image.Height, WrapType.Square);
    }
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## InsertOnlineVideo(*string, string, byte[], [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertonlinevideo_2}

يقوم بإدراج كائن فيديو عبر الإنترنت في المستند ويقوم بتغيير حجمه إلى الحجم المحدد.

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    RelativeHorizontalPosition horzPos, double left, RelativeVerticalPosition vertPos, double top, 
    double width, double height, WrapType wrapType)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| videoUrl | String | عنوان URL للفيديو. |
| videoEmbedCode | String | كود التضمين للفيديو. |
| thumbnailImageBytes | Byte[] | بايتات الصورة المصغرة. |
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

يوضح كيفية إدراج مقطع فيديو عبر الإنترنت في مستند باستخدام صورة مصغرة مخصصة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";
string videoEmbedCode =
    "<iframe src=\"https://player.vimeo.com/video/52477838\" العرض=\"640\" الارتفاع=\"360\" حدود الإطار=\"0\" " +
    "title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

byte[] thumbnailImageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(thumbnailImageBytes))
{
    using (Image image = Image.FromStream(stream))
    {
        // فيما يلي طريقتان لإنشاء شكل باستخدام صورة مصغرة مخصصة، والتي ترتبط بمقطع فيديو عبر الإنترنت
        //هذا ما سيتم تشغيله عندما نضغط على الشكل في Microsoft Word.
        // 1 - إدراج شكل مضمن في مؤشر إدراج عقدة المنشئ:
        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image.Width, image.Height);

        builder.InsertBreak(BreakType.PageBreak);

        // 2 - إدراج شكل عائم:
        double left = builder.PageSetup.RightMargin - image.Width;
        double top = builder.PageSetup.BottomMargin - image.Height;

        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes,
            RelativeHorizontalPosition.RightMargin, left, RelativeVerticalPosition.BottomMargin, top,
            image.Width, image.Height, WrapType.Square);
    }
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
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

## InsertOnlineVideo(*string, double, double*) {#insertonlinevideo_1}

يقوم بإدراج كائن فيديو عبر الإنترنت في المستند ويقوم بتغيير حجمه إلى الحجم المحدد.

```csharp
public Shape InsertOnlineVideo(string videoUrl, double width, double height)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| videoUrl | String | عنوان URL للفيديو. |
| width | Double | عرض الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس ١٠٠٪. |
| height | Double | ارتفاع الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس ١٠٠٪. |

### قيمة الإرجاع

عقدة الصورة التي تم إدراجها للتو.

## ملاحظات

يمكنك تغيير حجم الصورة وموقعها وطريقة تحديد الموقع والإعدادات الأخرى باستخدام [`Shape`](../../../aspose.words.drawing/shape/) الكائن الذي تم إرجاعه بواسطة هذه الطريقة.

يتم دعم إدراج الفيديو عبر الإنترنت من الموارد التالية:

* https://www.youtube.com/
* https://vimeo.com/

إذا لم يتم عرض مقطع الفيديو الخاص بك عبر الإنترنت بشكل صحيح، فاستخدم`InsertOnlineVideo`، والذي يقبل كود HTML المضمن المخصص.

قد يختلف كود تضمين الفيديو بين مقدمي الخدمة، لذا استشر مقدم الخدمة المناسب لك للحصول على التفاصيل.

## أمثلة

يوضح كيفية إدراج مقطع فيديو عبر الإنترنت في مستند باستخدام عنوان URL.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOnlineVideo("https://youtu.be/g1N9ke8Prmk"، 360، 270);

//يمكننا مشاهدة الفيديو من Microsoft Word بالضغط على الشكل.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertVideoWithUrl.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
