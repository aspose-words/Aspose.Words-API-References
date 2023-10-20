---
title: HtmlSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words لـ .NET
description: HtmlSaveOptions ImagesFolderAlias ملكية. يحدد اسم المجلد المستخدم لإنشاء معرفات URI للصور المكتوبة في مستند HTML. الافتراضي هو سلسلة فارغة في C#.
type: docs
weight: 370
url: /ar/net/aspose.words.saving/htmlsaveoptions/imagesfolderalias/
---
## HtmlSaveOptions.ImagesFolderAlias property

يحدد اسم المجلد المستخدم لإنشاء معرفات URI للصور المكتوبة في مستند HTML. الافتراضي هو سلسلة فارغة.

```csharp
public string ImagesFolderAlias { get; set; }
```

## ملاحظات

عندما تقوم بحفظ أ[`Document`](../../../aspose.words/document/) بتنسيق HTML، يحتاج Aspose.Words إلى حفظ كافة الصور المضمنة في المستند كملفات مستقلة.[`ImagesFolder`](../imagesfolder/) يسمح لك بتحديد مكان حفظ الصور و`ImagesFolderAlias` يسمح بتحديد كيفية إنشاء معرفات URI للصورة.

لو`ImagesFolderAlias` ليست سلسلة فارغة، فإن URI للصورة المكتوب إلى HTML سيكونImagesFolderAlias + &lt;اسم ملف الصورة&gt;.

لو`ImagesFolderAlias` إذا كانت سلسلة فارغة، فسيكون URI للصورة المكتوبة إلى HTMLImagesFolder + &lt;اسم ملف الصورة&gt;.

لو`ImagesFolderAlias`تم ضبطه على "." (نقطة)، فسيتم كتابة اسم ملف الصورة إلى HTML بدون مسار بغض النظر عن الخيارات الأخرى.

طريقة بديلة لتحديد اسم المجلد لإنشاء صورة URIs هي الاستخدام[`ResourceFolderAlias`](../resourcefolderalias/).

## أمثلة

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
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
