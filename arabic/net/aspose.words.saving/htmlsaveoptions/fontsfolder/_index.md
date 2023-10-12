---
title: HtmlSaveOptions.FontsFolder
second_title: Aspose.Words لمراجع .NET API
description: HtmlSaveOptions ملكية. يحدد المجلد الفعلي حيث يتم حفظ الخطوط عند تصدير مستند إلى HTML. الافتراضي هو سلسلة فارغة.
type: docs
weight: 310
url: /ar/net/aspose.words.saving/htmlsaveoptions/fontsfolder/
---
## HtmlSaveOptions.FontsFolder property

يحدد المجلد الفعلي حيث يتم حفظ الخطوط عند تصدير مستند إلى HTML. الافتراضي هو سلسلة فارغة.

```csharp
public string FontsFolder { get; set; }
```

### ملاحظات

عندما تقوم بحفظ أ[`Document`](../../../aspose.words/document/) بتنسيق HTML و[`ExportFontResources`](../exportfontresources/) تم ضبط على`حقيقي` ، يحتاج Aspose.Words إلى حفظ الخطوط المستخدمة في المستند كملفات مستقلة. `FontsFolder` يسمح لك بتحديد مكان حفظ الخطوط و [`FontsFolderAlias`](../fontsfolderalias/) يسمح بتحديد كيفية إنشاء عناوين URI للخط.

إذا قمت بحفظ مستند في ملف وقمت بتوفير اسم ملف، فإن Aspose.Words، افتراضيًا، يحفظ الخطوط في نفس المجلد حيث تم حفظ ملف المستند. يستخدم`FontsFolder` لتجاوز هذا السلوك.

إذا قمت بحفظ مستند في دفق، فلن يحتوي Aspose.Words على مجلد لحفظ الخطوط، ولكنه لا يزال بحاجة إلى حفظ الخطوط في مكان ما. في هذه الحالة، تحتاج إلى تحديد مجلد يمكن الوصول إليه في ملف`FontsFolder` الملكية أو تقديم تدفقات مخصصة عبر the[`FontSavingCallback`](../fontsavingcallback/) معالج الحدث.

إذا كان المجلد المحدد بواسطة`FontsFolder` غير موجود، سيتم إنشاؤه تلقائيًا.

[`ResourceFolder`](../resourcefolder/) هي طريقة أخرى لتحديد المجلد الذي يجب حفظ الخطوط فيه.

### أمثلة

يوضح كيفية تعيين المجلدات والأسماء المستعارة للمجلدات للموارد المحفوظة خارجيًا والتي سيقوم Aspose.Words بإنشائها عند حفظ مستند إلى HTML.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlSaveOptions options = new HtmlSaveOptions
{
    CssStyleSheetType = CssStyleSheetType.External,
    ExportFontResources = true,
    ImageResolution = 72,
    FontResourcesSubsettingSizeThreshold = 0,
    FontsFolder = ArtifactsDir + "Fonts",
    ImagesFolder = ArtifactsDir + "Images",
    ResourceFolder = ArtifactsDir + "Resources",
    FontsFolderAlias = "http://example.com/fonts"،
    ImagesFolderAlias = "http://example.com/images"،
    ResourceFolderAlias = "http://example.com/resources"،
    ExportOriginalUrlForLinkedImages = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FolderAlias.html", options);
```

### أنظر أيضا

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../htmlsaveoptions/)
* المجسم [Aspose.Words](../../../)


