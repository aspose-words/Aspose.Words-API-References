---
title: MarkdownSaveOptions.ImagesFolder
linktitle: ImagesFolder
articleTitle: ImagesFolder
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية MarkdownSaveOptions ImagesFolder على تعزيز تصدير المستندات الخاصة بك عن طريق تحديد المجلد المثالي لحفظ الصور بتنسيق Markdown.
type: docs
weight: 80
url: /ar/net/aspose.words.saving/markdownsaveoptions/imagesfolder/
---
## MarkdownSaveOptions.ImagesFolder property

يحدد المجلد الفعلي الذي يتم حفظ الصور فيه عند تصدير مستند إلى Markdown التنسيق الافتراضي هو سلسلة فارغة.

```csharp
public string ImagesFolder { get; set; }
```

## ملاحظات

عندما تحفظ[`Document`](../../../aspose.words/document/) فيMarkdownيحتاج Aspose.Words إلى حفظ جميع الصور المضمنة في المستند كملفات مستقلة. `ImagesFolder` يسمح لك بتحديد المكان الذي سيتم حفظ الصور فيه.

إذا حفظت مستندًا في ملف وأدخلت اسمًا للملف، فسيحفظ Aspose.Words الصور افتراضيًا في نفس المجلد الذي حُفظ فيه ملف المستند. استخدم`ImagesFolder` لتجاوز هذا السلوك.

إذا حفظت مستندًا في مسار، فلن يحتوي Aspose.Words على مجلد لحفظ الصور، ولكنه سيحتاج إلى حفظها في مكان ما. في هذه الحالة، ستحتاج إلى تحديد مجلد يمكن الوصول إليه في`ImagesFolder` الملكية.

إذا كان المجلد المحدد بواسطة`ImagesFolder` غير موجود، سيتم إنشاؤه تلقائيًا.

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
