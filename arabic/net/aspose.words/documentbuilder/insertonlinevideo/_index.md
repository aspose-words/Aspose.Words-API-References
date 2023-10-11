---
title: DocumentBuilder.InsertOnlineVideo
second_title: Aspose.Words لمراجع .NET API
description: DocumentBuilder طريقة. إدراج كائن فيديو عبر الإنترنت في المستند وتغيير حجمه إلى الحجم المحدد.
type: docs
weight: 420
url: /ar/net/aspose.words/documentbuilder/insertonlinevideo/
---
## InsertOnlineVideo(string, double, double) {#insertonlinevideo_1}

إدراج كائن فيديو عبر الإنترنت في المستند وتغيير حجمه إلى الحجم المحدد.

```csharp
public Shape InsertOnlineVideo(string videoUrl, double width, double height)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| videoUrl | String | عنوان URL للفيديو. |
| width | Double | عرض الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس 100%. |
| height | Double | ارتفاع الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس 100%. |

### قيمة الإرجاع

عقدة الصورة التي تم إدراجها للتو.

### ملاحظات

يمكنك تغيير حجم الصورة والموقع وطريقة تحديد الموضع والإعدادات الأخرى باستخدام [`Shape`](../../../aspose.words.drawing/shape/) الكائن الذي تم إرجاعه بهذه الطريقة.

يتم دعم إدراج الفيديو عبر الإنترنت من الموارد التالية:

* https://www.youtube.com/
* https://vimeo.com/

إذا لم يتم عرض الفيديو الخاص بك على الإنترنت بشكل صحيح، فاستخدم`InsertOnlineVideo`، والذي يقبل كود html المضمن المخصص.

يمكن أن يختلف رمز تضمين الفيديو بين مقدمي الخدمة، لذا استشر المزود الذي تختاره للحصول على التفاصيل.

### أمثلة

يوضح كيفية إدراج مقطع فيديو عبر الإنترنت في مستند باستخدام عنوان URL.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOnlineVideo("https://youtu.be/t_1LYZ102RA"، 360، 270);

// يمكننا مشاهدة الفيديو من برنامج Microsoft Word بالضغط على الشكل.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertVideoWithUrl.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)

---

## InsertOnlineVideo(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertonlinevideo}

إدراج كائن فيديو عبر الإنترنت في المستند وتغيير حجمه إلى الحجم المحدد.

```csharp
public Shape InsertOnlineVideo(string videoUrl, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| videoUrl | String | عنوان URL للفيديو. |
| horzPos | RelativeHorizontalPosition | يحدد المكان الذي يتم منه قياس المسافة إلى الصورة. |
| left | Double | المسافة بالنقاط من الأصل إلى الجانب الأيسر من الصورة. |
| vertPos | RelativeVerticalPosition | يحدد المكان الذي يتم قياس المسافة منه إلى الصورة. |
| top | Double | المسافة بالنقاط من الأصل إلى الجانب العلوي من الصورة. |
| width | Double | عرض الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس 100%. |
| height | Double | ارتفاع الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس 100%. |
| wrapType | WrapType | يحدد كيفية التفاف النص حول الصورة. |

### قيمة الإرجاع

عقدة الصورة التي تم إدراجها للتو.

### ملاحظات

يمكنك تغيير حجم الصورة والموقع وطريقة تحديد الموضع والإعدادات الأخرى باستخدام [`Shape`](../../../aspose.words.drawing/shape/) الكائن الذي تم إرجاعه بهذه الطريقة.

يتم دعم إدراج الفيديو عبر الإنترنت من الموارد التالية:

* https://www.youtube.com/
* https://vimeo.com/

إذا لم يتم عرض الفيديو الخاص بك على الإنترنت بشكل صحيح، فاستخدم`InsertOnlineVideo`، والذي يقبل كود html المضمن المخصص.

يمكن أن يختلف رمز تضمين الفيديو بين مقدمي الخدمة، لذا استشر المزود الذي تختاره للحصول على التفاصيل.

### أمثلة

يوضح كيفية إدراج مقطع فيديو عبر الإنترنت في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";

// أدخل شكلاً يقوم بتشغيل مقطع فيديو من الويب عند النقر عليه في Microsoft Word.
// سيحتوي هذا الشكل المستطيل على صورة بناءً على الإطار الأول للفيديو المرتبط
// وموجه مرئي "زر التشغيل". الفيديو لديه نسبة عرض إلى ارتفاع 16:9.
// سنقوم بضبط حجم الشكل على تلك النسبة، حتى لا تظهر الصورة ممتدة.
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
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)

---

## InsertOnlineVideo(string, string, byte[], double, double) {#insertonlinevideo_3}

إدراج كائن فيديو عبر الإنترنت في المستند وتغيير حجمه إلى الحجم المحدد.

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    double width, double height)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| videoUrl | String | عنوان URL للفيديو. |
| videoEmbedCode | String | كود التضمين للفيديو. |
| thumbnailImageBytes | Byte[] | بايت الصورة المصغرة. |
| width | Double | عرض الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس 100%. |
| height | Double | ارتفاع الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس 100%. |

### قيمة الإرجاع

عقدة الصورة التي تم إدراجها للتو.

### ملاحظات

يمكنك تغيير حجم الصورة والموقع وطريقة تحديد الموضع والإعدادات الأخرى باستخدام [`Shape`](../../../aspose.words.drawing/shape/) الكائن الذي تم إرجاعه بهذه الطريقة.

### أمثلة

يوضح كيفية إدراج مقطع فيديو عبر الإنترنت في مستند باستخدام صورة مصغرة مخصصة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";
string videoEmbedCode =
    "<iframe src=\"https://player.vimeo.com/video/52477838\" width=\"640\" height=\"360\"frameborder=\"0\" " +
    "title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

byte[] thumbnailImageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(thumbnailImageBytes))
{
    using (Image image = Image.FromStream(stream))
    {
        // فيما يلي طريقتان لإنشاء شكل باستخدام صورة مصغرة مخصصة ترتبط بمقطع فيديو عبر الإنترنت
        // الذي سيتم تشغيله عندما ننقر على الشكل في Microsoft Word.
        // 1 - إدراج شكل سطري عند مؤشر إدراج عقدة المنشئ:
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
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)

---

## InsertOnlineVideo(string, string, byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertonlinevideo_2}

إدراج كائن فيديو عبر الإنترنت في المستند وتغيير حجمه إلى الحجم المحدد.

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    RelativeHorizontalPosition horzPos, double left, RelativeVerticalPosition vertPos, double top, 
    double width, double height, WrapType wrapType)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| videoUrl | String | عنوان URL للفيديو. |
| videoEmbedCode | String | كود التضمين للفيديو. |
| thumbnailImageBytes | Byte[] | بايت الصورة المصغرة. |
| horzPos | RelativeHorizontalPosition | يحدد المكان الذي يتم منه قياس المسافة إلى الصورة. |
| left | Double | المسافة بالنقاط من الأصل إلى الجانب الأيسر من الصورة. |
| vertPos | RelativeVerticalPosition | يحدد المكان الذي يتم قياس المسافة منه إلى الصورة. |
| top | Double | المسافة بالنقاط من الأصل إلى الجانب العلوي من الصورة. |
| width | Double | عرض الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس 100%. |
| height | Double | ارتفاع الصورة بالنقاط. يمكن أن تكون قيمة سالبة أو صفرية لطلب مقياس 100%. |
| wrapType | WrapType | يحدد كيفية التفاف النص حول الصورة. |

### قيمة الإرجاع

عقدة الصورة التي تم إدراجها للتو.

### ملاحظات

يمكنك تغيير حجم الصورة والموقع وطريقة تحديد الموضع والإعدادات الأخرى باستخدام [`Shape`](../../../aspose.words.drawing/shape/) الكائن الذي تم إرجاعه بهذه الطريقة.

### أمثلة

يوضح كيفية إدراج مقطع فيديو عبر الإنترنت في مستند باستخدام صورة مصغرة مخصصة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";
string videoEmbedCode =
    "<iframe src=\"https://player.vimeo.com/video/52477838\" width=\"640\" height=\"360\"frameborder=\"0\" " +
    "title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

byte[] thumbnailImageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(thumbnailImageBytes))
{
    using (Image image = Image.FromStream(stream))
    {
        // فيما يلي طريقتان لإنشاء شكل باستخدام صورة مصغرة مخصصة ترتبط بمقطع فيديو عبر الإنترنت
        // الذي سيتم تشغيله عندما ننقر على الشكل في Microsoft Word.
        // 1 - إدراج شكل سطري عند مؤشر إدراج عقدة المنشئ:
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
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)


