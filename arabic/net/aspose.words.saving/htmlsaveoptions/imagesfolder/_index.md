---
title: HtmlSaveOptions.ImagesFolder
linktitle: ImagesFolder
articleTitle: ImagesFolder
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية HtmlSaveOptions ImagesFolder. حدّد بسهولة مجلد حفظ الصور عند تصدير المستندات إلى HTML. بسّط سير عملك اليوم!
type: docs
weight: 360
url: /ar/net/aspose.words.saving/htmlsaveoptions/imagesfolder/
---
## HtmlSaveOptions.ImagesFolder property

يحدد المجلد الفعلي الذي يتم حفظ الصور فيه عند تصدير مستند إلى تنسيق HTML. الافتراضي هو سلسلة فارغة.

```csharp
public string ImagesFolder { get; set; }
```

## ملاحظات

عندما تحفظ[`Document`](../../../aspose.words/document/) في تنسيق HTML، يحتاج Aspose.Words إلى حفظ جميع الصور المضمنة في المستند كملفات مستقلة.`ImagesFolder` يسمح لك بتحديد المكان الذي سيتم حفظ الصور فيه و[`ImagesFolderAlias`](../imagesfolderalias/) يسمح لك بتحديد كيفية إنشاء عناوين URI للصور.

إذا حفظت مستندًا في ملف وأدخلت اسمًا للملف، فسيحفظ Aspose.Words افتراضيًا صور x000d_ في نفس المجلد الذي حُفظ فيه ملف المستند. استخدم`ImagesFolder` لتجاوز هذا السلوك.

إذا حفظت مستندًا في مسار، فلن يحتوي Aspose.Words على مجلد لحفظ الصور، ، ولكنه سيحتاج إلى حفظ الصور في مكان ما. في هذه الحالة، ستحتاج إلى تحديد مجلد يسهل الوصول إليه في`ImagesFolder` الخاصية أو توفير تدفقات مخصصة عبر [`ImageSavingCallback`](../imagesavingcallback/) معالج الحدث.

إذا تم تحديد المجلد بواسطة`ImagesFolder` إذا لم يكن موجودًا، فسيتم إنشاؤه تلقائيًا.

[`ResourceFolder`](../resourcefolder/) هناك طريقة أخرى لتحديد المجلد الذي يجب حفظ الصور فيه.

## أمثلة

يوضح كيفية تحديد المجلد لتخزين الصور المرتبطة بعد حفظها في .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// تعيين خيار لتصدير حقول النموذج كنص عادي بدلاً من عناصر إدخال HTML.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

### أنظر أيضا

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
