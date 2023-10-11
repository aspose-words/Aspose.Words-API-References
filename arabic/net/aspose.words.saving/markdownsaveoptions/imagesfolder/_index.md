---
title: MarkdownSaveOptions.ImagesFolder
second_title: Aspose.Words لمراجع .NET API
description: MarkdownSaveOptions ملكية. يحدد المجلد الفعلي حيث يتم حفظ الصور عند تصدير مستند إلى Markdown شكل. الافتراضي هو سلسلة فارغة.
type: docs
weight: 40
url: /ar/net/aspose.words.saving/markdownsaveoptions/imagesfolder/
---
## MarkdownSaveOptions.ImagesFolder property

يحدد المجلد الفعلي حيث يتم حفظ الصور عند تصدير مستند إلى Markdown شكل. الافتراضي هو سلسلة فارغة.

```csharp
public string ImagesFolder { get; set; }
```

### ملاحظات

عندما تقوم بحفظ ملف[`Document`](../../../aspose.words/document/) فيMarkdownالتنسيق، يحتاج Aspose.Words إلى حفظ جميع الصور المضمنة في المستند كملفات مستقلة. `ImagesFolder` يسمح لك بتحديد مكان حفظ الصور.

إذا قمت بحفظ مستند في ملف وقمت بتوفير اسم ملف، فإن Aspose.Words، بشكل افتراضي، يحفظ الصور في نفس المجلد الذي تم حفظ ملف المستند فيه. يستخدم`ImagesFolder` لتجاوز هذا السلوك.

إذا قمت بحفظ مستند في دفق، فلن يحتوي Aspose.Words على مجلد لحفظ الصور، ولكنه لا يزال بحاجة إلى حفظ الصور في مكان ما. في هذه الحالة، تحتاج إلى تحديد مجلد يمكن الوصول إليه في ملف`ImagesFolder` الملكية.

إذا كان المجلد المحدد بواسطة`ImagesFolder` غير موجود، سيتم إنشاؤه تلقائيًا.

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


