---
title: HtmlSaveOptions.ExportOriginalUrlForLinkedImages
second_title: Aspose.Words لمراجع .NET API
description: HtmlSaveOptions ملكية. يحدد ما إذا كان يجب استخدام عنوان URL الأصلي كعنوان URL للصور المرتبطة. القيمة الافتراضية هيخطأ شنيع .
type: docs
weight: 200
url: /ar/net/aspose.words.saving/htmlsaveoptions/exportoriginalurlforlinkedimages/
---
## HtmlSaveOptions.ExportOriginalUrlForLinkedImages property

يحدد ما إذا كان يجب استخدام عنوان URL الأصلي كعنوان URL للصور المرتبطة. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool ExportOriginalUrlForLinkedImages { get; set; }
```

### ملاحظات

إذا تم ضبط القيمة على`حقيقي`[`SourceFullName`](../../../aspose.words.drawing/imagedata/sourcefullname/) يتم استخدام القيمة حيث لا يتم تحميل عنوان URL للصور المرتبطة والصور المرتبطة في مجلد المستند أو[`ImagesFolder`](../imagesfolder/).

إذا تم ضبط القيمة على`خطأ شنيع`يتم تحميل الصور المرتبطة في مجلد المستند أو[`ImagesFolder`](../imagesfolder/) ويتم إنشاء عنوان URL لكل صورة مرتبطة اعتمادًا على في مجلد المستند،[`ImagesFolder`](../imagesfolder/) و[`ImagesFolderAlias`](../imagesfolderalias/) ملكيات.

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


