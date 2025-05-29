---
title: HtmlSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية HtmlSaveOptions ImagesFolderAlias لإدارة عناوين URI للصور بسهولة في مستندات HTML. بسّط سير عملك مع هذه الميزة الأساسية!
type: docs
weight: 370
url: /ar/net/aspose.words.saving/htmlsaveoptions/imagesfolderalias/
---
## HtmlSaveOptions.ImagesFolderAlias property

يحدد اسم المجلد المستخدم لإنشاء عناوين URI للصور المكتوبة في مستند HTML. الافتراضي هو سلسلة فارغة.

```csharp
public string ImagesFolderAlias { get; set; }
```

## ملاحظات

عندما تحفظ[`Document`](../../../aspose.words/document/) في تنسيق HTML، يحتاج Aspose.Words إلى حفظ جميع الصور المضمنة في المستند كملفات مستقلة.[`ImagesFolder`](../imagesfolder/) يسمح لك بتحديد المكان الذي سيتم حفظ الصور فيه و`ImagesFolderAlias` يسمح لك بتحديد كيفية إنشاء عناوين URI للصور.

لو`ImagesFolderAlias` إذا لم تكن سلسلة فارغة، فإن عنوان URI للصورة الذي تمت كتابته إلى HTML سيكونImagesFolderAlias + &lt;اسم ملف الصورة&gt;.

لو`ImagesFolderAlias`إذا كانت السلسلة فارغة، فإن عنوان URI للصورة الذي تمت كتابته إلى HTML سيكون x000d_مجلد الصور + &lt;اسم ملف الصورة&gt;.

لو`ImagesFolderAlias` إذا تم تعيينه على '.' (نقطة)، فسيتم كتابة ملف الصورة name إلى HTML بدون مسار بغض النظر عن الخيارات الأخرى.

الطريقة البديلة لتحديد اسم المجلد لإنشاء URIs للصورة هي استخدام[`ResourceFolderAlias`](../resourcefolderalias/).

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
