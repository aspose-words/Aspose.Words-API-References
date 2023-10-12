---
title: HtmlSaveOptions.ImagesFolder
second_title: Aspose.Words لمراجع .NET API
description: HtmlSaveOptions ملكية. يحدد المجلد الفعلي حيث يتم حفظ الصور عند تصدير مستند إلى تنسيق HTML. الافتراضي هو سلسلة فارغة.
type: docs
weight: 360
url: /ar/net/aspose.words.saving/htmlsaveoptions/imagesfolder/
---
## HtmlSaveOptions.ImagesFolder property

يحدد المجلد الفعلي حيث يتم حفظ الصور عند تصدير مستند إلى تنسيق HTML. الافتراضي هو سلسلة فارغة.

```csharp
public string ImagesFolder { get; set; }
```

### ملاحظات

عندما تقوم بحفظ أ[`Document`](../../../aspose.words/document/) بتنسيق HTML، يحتاج Aspose.Words إلى حفظ كافة الصور المضمنة في المستند كملفات مستقلة.`ImagesFolder` يسمح لك بتحديد مكان حفظ الصور و[`ImagesFolderAlias`](../imagesfolderalias/) يسمح بتحديد كيفية إنشاء معرفات URI للصورة.

إذا قمت بحفظ مستند في ملف وقمت بتوفير اسم ملف، فسيقوم Aspose.Words، افتراضيًا، بحفظ الصور في نفس المجلد حيث تم حفظ ملف المستند. يستخدم`ImagesFolder` لتجاوز هذا السلوك.

إذا قمت بحفظ مستند في دفق، فلن يحتوي Aspose.Words على مجلد لحفظ الصور، ولكنه لا يزال بحاجة إلى حفظ الصور في مكان ما. في هذه الحالة، تحتاج إلى تحديد مجلد يمكن الوصول إليه في ملف`ImagesFolder` الملكية أو تقديم تدفقات مخصصة عبر the[`ImageSavingCallback`](../imagesavingcallback/) معالج الحدث.

إذا كان المجلد المحدد بواسطة`ImagesFolder` غير موجود، سيتم إنشاؤه تلقائيًا.

[`ResourceFolder`](../resourcefolder/) هي طريقة أخرى لتحديد المجلد الذي يجب حفظ الصور فيه.

### أمثلة

يوضح كيفية تحديد المجلد لتخزين الصور المرتبطة بعد حفظها في .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// قم بتعيين خيار لتصدير حقول النموذج كنص عادي بدلاً من عناصر إدخال HTML.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

### أنظر أيضا

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../htmlsaveoptions/)
* المجسم [Aspose.Words](../../../)


