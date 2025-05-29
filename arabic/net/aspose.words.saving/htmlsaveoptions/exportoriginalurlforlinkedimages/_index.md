---
title: HtmlSaveOptions.ExportOriginalUrlForLinkedImages
linktitle: ExportOriginalUrlForLinkedImages
articleTitle: ExportOriginalUrlForLinkedImages
second_title: Aspose.Words لـ .NET
description: اكتشف ميزة ExportOriginalUrlForLinkedImages في HtmlSaveOptions، التي تتيح لك استخدام عناوين URL الأصلية للصور المرتبطة. حسّن من سلامة مستندك!
type: docs
weight: 200
url: /ar/net/aspose.words.saving/htmlsaveoptions/exportoriginalurlforlinkedimages/
---
## HtmlSaveOptions.ExportOriginalUrlForLinkedImages property

يحدد ما إذا كان يجب استخدام عنوان URL الأصلي كعنوان URL للصور المرتبطة. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool ExportOriginalUrlForLinkedImages { get; set; }
```

## ملاحظات

إذا تم تعيين القيمة على`حقيقي`[`SourceFullName`](../../../aspose.words.drawing/imagedata/sourcefullname/) يتم استخدام القيمة كعنوان URL للصور المرتبطة ولا يتم تحميل الصور المرتبطة إلى مجلد المستند أو[`ImagesFolder`](../imagesfolder/).

إذا تم تعيين القيمة على`خطأ شنيع`يتم تحميل الصور المرتبطة إلى مجلد المستند أو[`ImagesFolder`](../imagesfolder/) ويتم إنشاء عنوان URL لكل صورة مرتبطة اعتمادًا على مجلد المستند،[`ImagesFolder`](../imagesfolder/) و[`ImagesFolderAlias`](../imagesfolderalias/) ملكيات.

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
