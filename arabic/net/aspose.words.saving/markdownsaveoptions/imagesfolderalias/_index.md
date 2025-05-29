---
title: MarkdownSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية MarkdownSaveOptions ImagesFolderAlias لإدارة عناوين URI للصور في مستنداتك بسهولة. سهّل سير عملك مع هذه الميزة الأساسية!
type: docs
weight: 90
url: /ar/net/aspose.words.saving/markdownsaveoptions/imagesfolderalias/
---
## MarkdownSaveOptions.ImagesFolderAlias property

يحدد اسم المجلد المستخدم لإنشاء عناوين URI للصور المكتوبة في مستند. الافتراضي هو سلسلة فارغة.

```csharp
public string ImagesFolderAlias { get; set; }
```

## ملاحظات

عندما تحفظ[`Document`](../../../aspose.words/document/) فيMarkdown يحتاج Aspose.Words إلى حفظ جميع الصور المضمنة في المستند كملفات مستقلة. [`ImagesFolder`](../imagesfolder/) يسمح لك بتحديد المكان الذي سيتم حفظ الصور فيه و `ImagesFolderAlias` يسمح بتحديد كيفية إنشاء عناوين URI للصور.

لو`ImagesFolderAlias` إذا لم تكن سلسلة فارغة، فإن عنوان URI للصورة الذي تمت كتابته إلى Markdown سيكونImagesFolderAlias + &lt;اسم ملف الصورة&gt;.

لو`ImagesFolderAlias` إذا كانت السلسلة فارغة، فإن عنوان URI للصورة الذي تمت كتابته إلى Markdown سيكون:مجلد الصور + &lt;اسم ملف الصورة&gt;.

لو`ImagesFolderAlias` إذا تم تعيينه على '.' (نقطة)، فسيتم كتابة ملف الصورة name إلى Markdown بدون مسار بغض النظر عن الخيارات الأخرى.

## أمثلة

يوضح كيفية تحديد اسم المجلد المستخدم لإنشاء عناوين URI للصور.

```csharp
DocumentBuilder builder = new DocumentBuilder();

builder.Writeln("Some image below:");
builder.InsertImage(ImageDir + "Logo.jpg");

string imagesFolder = Path.Combine(ArtifactsDir, "ImagesDir");
MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
// استخدم خاصية "ImagesFolder" لتعيين مجلد في نظام الملفات المحلي الذي سيتم تخزين الصور فيه
// سيقوم Aspose.Words بحفظ جميع الصور المرتبطة بالمستند.
saveOptions.ImagesFolder = imagesFolder;
// استخدم خاصية "ImagesFolderAlias" لاستخدام هذا المجلد
// عند إنشاء عناوين URI للصور بدلاً من اسم مجلد الصور.
saveOptions.ImagesFolderAlias = "http://example.com/images";

builder.Document.Save(ArtifactsDir + "MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

### أنظر أيضا

* class [MarkdownSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
