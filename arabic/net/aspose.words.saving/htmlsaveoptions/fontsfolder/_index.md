---
title: HtmlSaveOptions.FontsFolder
linktitle: FontsFolder
articleTitle: FontsFolder
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية HtmlSaveOptions FontsFolder لإدارة تخزين الخطوط بسهولة لصادرات HTML، وتحسين عرض المستندات وإمكانية الوصول إليها.
type: docs
weight: 310
url: /ar/net/aspose.words.saving/htmlsaveoptions/fontsfolder/
---
## HtmlSaveOptions.FontsFolder property

يحدد المجلد الفعلي الذي يتم حفظ الخطوط فيه عند تصدير مستند إلى HTML. الافتراضي هو سلسلة فارغة.

```csharp
public string FontsFolder { get; set; }
```

## ملاحظات

عندما تحفظ[`Document`](../../../aspose.words/document/) بتنسيق HTML و[`ExportFontResources`](../exportfontresources/) تم تعيين على`حقيقي` ، يحتاج Aspose.Words إلى حفظ الخطوط المستخدمة في المستند كملفات مستقلة. `FontsFolder` يسمح لك بتحديد المكان الذي سيتم حفظ الخطوط فيه و [`FontsFolderAlias`](../fontsfolderalias/) يسمح بتحديد كيفية إنشاء عناوين URI للخطوط.

إذا حفظت مستندًا في ملف وأدخلت اسمًا للملف، فسيحفظ Aspose.Words افتراضيًا خطوط x000d_ في نفس المجلد الذي حفظ فيه ملف المستند. استخدم`FontsFolder` لتجاوز هذا السلوك.

إذا حفظت مستندًا في مسار، فلن يحتوي Aspose.Words على مجلد لحفظ الخطوط، ، ولكنه سيحتاج إلى حفظها في مكان ما. في هذه الحالة، ستحتاج إلى تحديد مجلد يسهل الوصول إليه في`FontsFolder` الخاصية أو توفير تدفقات مخصصة عبر [`FontSavingCallback`](../fontsavingcallback/) معالج الحدث.

إذا تم تحديد المجلد بواسطة`FontsFolder` إذا لم يكن موجودًا، فسيتم إنشاؤه تلقائيًا.

[`ResourceFolder`](../resourcefolder/) هناك طريقة أخرى لتحديد المجلد الذي يجب حفظ الخطوط فيه.

## أمثلة

يوضح كيفية تعيين المجلدات وأسماء المجلدات للموارد المحفوظة خارجيًا والتي سيقوم Aspose.Words بإنشائها عند حفظ مستند بتنسيق HTML.

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
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
