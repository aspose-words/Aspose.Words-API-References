---
title: HtmlSaveOptions.FontsFolderAlias
linktitle: FontsFolderAlias
articleTitle: FontsFolderAlias
second_title: Aspose.Words لـ .NET
description: HtmlSaveOptions FontsFolderAlias ملكية. يحدد اسم المجلد المستخدم لإنشاء معرفات URI للخط المكتوب في مستند HTML. الافتراضي هو سلسلة فارغة في C#.
type: docs
weight: 320
url: /ar/net/aspose.words.saving/htmlsaveoptions/fontsfolderalias/
---
## HtmlSaveOptions.FontsFolderAlias property

يحدد اسم المجلد المستخدم لإنشاء معرفات URI للخط المكتوب في مستند HTML. الافتراضي هو سلسلة فارغة.

```csharp
public string FontsFolderAlias { get; set; }
```

## ملاحظات

عندما تقوم بحفظ أ[`Document`](../../../aspose.words/document/) بتنسيق HTML و[`ExportFontResources`](../exportfontresources/) تم ضبط على`حقيقي` ، يحتاج Aspose.Words إلى حفظ الخطوط المستخدمة في المستند كملفات مستقلة. [`FontsFolder`](../fontsfolder/) يسمح لك بتحديد مكان حفظ الخطوط و `FontsFolderAlias` يسمح بتحديد كيفية إنشاء عناوين URI للخط.

لو`FontsFolderAlias` ليست سلسلة فارغة، فإن الخط URI المكتوب إلى HTML سيكونFontsFolderAlias + &lt;اسم ملف الخط&gt;.

لو`FontsFolderAlias` عبارة عن سلسلة فارغة، فسيكون عنوان URI للخط المكتوب إلى HTMLFontsFolder + &lt;اسم ملف الخط&gt;.

لو`FontsFolderAlias`تم ضبطه على "." (نقطة)، فسيتم كتابة اسم ملف الخط إلى HTML بدون مسار بغض النظر عن الخيارات الأخرى.

طريقة بديلة لتحديد اسم المجلد لإنشاء الخط URIs هي الاستخدام[`ResourceFolderAlias`](../resourcefolderalias/).

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
