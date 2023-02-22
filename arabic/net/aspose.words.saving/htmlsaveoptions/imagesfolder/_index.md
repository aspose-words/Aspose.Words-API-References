---
title: HtmlSaveOptions.ImagesFolder
second_title: Aspose.Words لمراجع .NET API
description: HtmlSaveOptions ملكية. يحدد المجلد الفعلي حيث يتم حفظ الصور عند تصدير مستند إلى تنسيق HTML. الافتراضي هو عبارة عن سلسلة فارغة.
type: docs
weight: 370
url: /ar/net/aspose.words.saving/htmlsaveoptions/imagesfolder/
---
## HtmlSaveOptions.ImagesFolder property

يحدد المجلد الفعلي حيث يتم حفظ الصور عند تصدير مستند إلى تنسيق HTML. الافتراضي هو عبارة عن سلسلة فارغة.

```csharp
public string ImagesFolder { get; set; }
```

### ملاحظات

عندما تقوم بحفظ ملف[`Document`](../../../aspose.words/document/) بتنسيق HTML ، يحتاج Aspose.Words إلى حفظ جميع الصور المضمنة في المستند كملفات قائمة بذاتها.`ImagesFolder` يسمح لك بتحديد مكان حفظ الصور و[`ImagesFolderAlias`](../imagesfolderalias/) يسمح بتحديد كيفية إنشاء عناوين URI للصورة.

إذا قمت بحفظ مستند في ملف وقمت بتوفير اسم ملف ، Aspose.Words ، بشكل افتراضي ، يحفظ الصور في نفس المجلد حيث يتم حفظ ملف المستند. يستخدم`ImagesFolder` لتجاوز هذا السلوك.

إذا قمت بحفظ مستند في دفق ، فإن Aspose.Words ليس بها مجلد لحفظ الصور ، ولكن لا يزال بحاجة إلى حفظ الصور في مكان ما. في هذه الحالة ، تحتاج إلى تحديد مجلد يمكن الوصول إليه في ملف`ImagesFolder` الخاصية أو توفير تدفقات مخصصة عبر [`ImageSavingCallback`](../imagesavingcallback/) معالج الحدث.

إذا كان المجلد المحدد بواسطة`ImagesFolder` غير موجود ، سيتم إنشاؤه تلقائيًا.

[`ResourceFolder`](../resourcefolder/) هي طريقة أخرى لتحديد مجلد يجب حفظ الصور فيه.

### أمثلة

يوضح كيفية تحديد مجلد لتخزين الصور المرتبطة بعد الحفظ في .html.

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
* مساحة الاسم [Aspose.Words.Saving](../../htmlsaveoptions/)
* المجسم [Aspose.Words](../../../)


