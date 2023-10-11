---
title: MarkdownSaveOptions.ImagesFolderAlias
second_title: Aspose.Words لمراجع .NET API
description: MarkdownSaveOptions ملكية. يحدد اسم المجلد المستخدم لإنشاء معرفات URI للصور المكتوبة في المستند. الافتراضي هو سلسلة فارغة.
type: docs
weight: 50
url: /ar/net/aspose.words.saving/markdownsaveoptions/imagesfolderalias/
---
## MarkdownSaveOptions.ImagesFolderAlias property

يحدد اسم المجلد المستخدم لإنشاء معرفات URI للصور المكتوبة في المستند. الافتراضي هو سلسلة فارغة.

```csharp
public string ImagesFolderAlias { get; set; }
```

### ملاحظات

عندما تقوم بحفظ أ[`Document`](../../../aspose.words/document/) فيMarkdown التنسيق، يحتاج Aspose.Words إلى حفظ جميع الصور المضمنة في المستند كملفات مستقلة. [`ImagesFolder`](../imagesfolder/) يسمح لك بتحديد مكان حفظ الصور و `ImagesFolderAlias` يسمح بتحديد كيفية إنشاء معرفات URI للصورة.

لو`ImagesFolderAlias` ليست سلسلة فارغة، فسيكون عنوان URI للصورة المكتوب إلى MarkdownImagesFolderAlias + &lt;اسم ملف الصورة&gt;.

لو`ImagesFolderAlias` عبارة عن سلسلة فارغة، فسيكون عنوان URI للصورة المكتوب إلى MarkdownImagesFolder + &lt;اسم ملف الصورة&gt;.

لو`ImagesFolderAlias`تم ضبطه على "." (نقطة)، فسيتم كتابة ملف الصورة name إلى Markdown بدون مسار بغض النظر عن الخيارات الأخرى.

### أمثلة

يوضح كيفية تحديد اسم المجلد المستخدم لإنشاء معرفات URI للصورة.

```csharp
DocumentBuilder builder = new DocumentBuilder();

builder.Writeln("Some image below:");
Image image = Image.FromFile(ImageDir + "Logo.jpg");
builder.InsertImage(image);

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
// استخدم خاصية "ImagesFolder" لتعيين مجلد في نظام الملفات المحلي الذي
// Aspose.Words سيحفظ جميع الصور المرتبطة بالمستند.
saveOptions.ImagesFolder = ArtifactsDir + "ImagesDir/";
// استخدم خاصية "ImagesFolderAlias" لاستخدام هذا المجلد
// عند إنشاء معرفات URI للصورة بدلاً من اسم مجلد الصور.
saveOptions.ImagesFolderAlias = "http://example.com/images";

builder.Document.Save(ArtifactsDir + "MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

يوضح كيفية تحديد اسم المجلد المستخدم لإنشاء معرفات URI للصورة (.NetStandard 2.0).

```csharp
DocumentBuilder builder = new DocumentBuilder();

builder.Writeln("Some image below:");
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
    builder.InsertImage(bitmap);

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
// استخدم خاصية "ImagesFolder" لتعيين مجلد في نظام الملفات المحلي الذي
// Aspose.Words سيحفظ جميع الصور المرتبطة بالمستند.
saveOptions.ImagesFolder = ArtifactsDir + "ImagesDir/";
// استخدم خاصية "ImagesFolderAlias" لاستخدام هذا المجلد
// عند إنشاء معرفات URI للصورة بدلاً من اسم مجلد الصور.
saveOptions.ImagesFolderAlias = "http://example.com/images";

builder.Document.Save(ArtifactsDir + "MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

### أنظر أيضا

* class [MarkdownSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../markdownsaveoptions/)
* المجسم [Aspose.Words](../../../)


