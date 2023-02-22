---
title: HtmlSaveOptions.ImageResolution
second_title: Aspose.Words لمراجع .NET API
description: HtmlSaveOptions ملكية. يحدد دقة الإخراج للصور عند التصدير إلى HTML أو MHTML أو EPUB. الافتراضي هو96 نقطة في البوصة .
type: docs
weight: 350
url: /ar/net/aspose.words.saving/htmlsaveoptions/imageresolution/
---
## HtmlSaveOptions.ImageResolution property

يحدد دقة الإخراج للصور عند التصدير إلى HTML أو MHTML أو EPUB. الافتراضي هو`96 نقطة في البوصة` .

```csharp
public int ImageResolution { get; set; }
```

### ملاحظات

هذه الخاصية تؤثر على الصور النقطية عندما[`ScaleImageToShapeSize`](../scaleimagetoshapesize/) هو`حقيقي` وتأثيرات ملفات التعريف التي تم تصديرها كصور نقطية. تتطلب بعض خصائص الصورة مثل cropping أو التدوير حفظ الصور المحولة وفي هذه الحالة يتم إنشاء الصور المحولة بدقة الوضوح المحددة.

### أمثلة

يوضح كيفية تعيين المجلدات والأسماء المستعارة للمجلدات للموارد المحفوظة خارجيًا والتي ستنشئها Aspose.Words عند حفظ مستند إلى HTML.

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
    FontsFolderAlias = "http://example.com/fonts "،
    ImagesFolderAlias = "http://example.com/images "،
    ResourceFolderAlias = "http://example.com/resources "،
    ExportOriginalUrlForLinkedImages = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FolderAlias.html", options);
```

### أنظر أيضا

* property [ScaleImageToShapeSize](../scaleimagetoshapesize/)
* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../htmlsaveoptions/)
* المجسم [Aspose.Words](../../../)


