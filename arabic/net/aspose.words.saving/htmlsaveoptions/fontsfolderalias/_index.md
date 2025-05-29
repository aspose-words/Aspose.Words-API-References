---
title: HtmlSaveOptions.FontsFolderAlias
linktitle: FontsFolderAlias
articleTitle: FontsFolderAlias
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية HtmlSaveOptions FontsFolderAlias لتخصيص عناوين URI للخطوط في مستندات HTML. حسّن تصميم موقعك الإلكتروني بسهولة!
type: docs
weight: 320
url: /ar/net/aspose.words.saving/htmlsaveoptions/fontsfolderalias/
---
## HtmlSaveOptions.FontsFolderAlias property

يحدد اسم المجلد المستخدم لإنشاء عناوين URI للخطوط المكتوبة في مستند HTML. الافتراضي هو سلسلة فارغة.

```csharp
public string FontsFolderAlias { get; set; }
```

## ملاحظات

عندما تحفظ[`Document`](../../../aspose.words/document/) بتنسيق HTML و[`ExportFontResources`](../exportfontresources/) تم تعيين على`حقيقي` ، يحتاج Aspose.Words إلى حفظ الخطوط المستخدمة في المستند كملفات مستقلة. [`FontsFolder`](../fontsfolder/) يسمح لك بتحديد المكان الذي سيتم حفظ الخطوط فيه و `FontsFolderAlias` يسمح بتحديد كيفية إنشاء عناوين URI للخطوط.

لو`FontsFolderAlias` إذا لم تكن سلسلة فارغة، فسيكون عنوان الخط URI المكتوب إلى HTMLFontsFolderAlias + &lt;اسم ملف الخط&gt;.

لو`FontsFolderAlias` إذا كانت السلسلة فارغة، فسيكون عنوان الخط URI المكتوب إلى HTML هومجلد الخطوط + &lt;اسم ملف الخط&gt;.

لو`FontsFolderAlias`إذا تم تعيينه على '.' (نقطة)، فسيتم كتابة ملف الخط name إلى HTML بدون مسار بغض النظر عن الخيارات الأخرى.

الطريقة البديلة لتحديد اسم المجلد لإنشاء الخط URIs هي استخدام[`ResourceFolderAlias`](../resourcefolderalias/).

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
