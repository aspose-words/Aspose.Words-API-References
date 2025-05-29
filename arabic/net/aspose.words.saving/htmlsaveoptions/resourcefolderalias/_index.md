---
title: HtmlSaveOptions.ResourceFolderAlias
linktitle: ResourceFolderAlias
articleTitle: ResourceFolderAlias
second_title: Aspose.Words لـ .NET
description: قم بتحسين مستندات HTML الخاصة بك باستخدام خاصية HtmlSaveOptions ResourceFolderAlias، وتحديد أسماء المجلدات لبناء URI فعال للموارد.
type: docs
weight: 450
url: /ar/net/aspose.words.saving/htmlsaveoptions/resourcefolderalias/
---
## HtmlSaveOptions.ResourceFolderAlias property

يحدد اسم المجلد المستخدم لإنشاء عناوين URI لجميع الموارد المكتوبة في مستند HTML. الافتراضي هو سلسلة فارغة.

```csharp
public string ResourceFolderAlias { get; set; }
```

## ملاحظات

`ResourceFolderAlias` هذه هي أبسط طريقة لتحديد كيفية إنشاء عناوين URI لجميع ملفات الموارد. يمكن تحديد المعلومات نفسها للصور والخطوط بشكل منفصل عبر[`ImagesFolderAlias`](../imagesfolderalias/) و[`FontsFolderAlias`](../fontsfolderalias/) الخصائص، على التوالي. ومع ذلك، لا توجد خاصية فردية لـ CSS.

`ResourceFolderAlias` لها أولوية أقل من[`FontsFolderAlias`](../fontsfolderalias/) و[`ImagesFolderAlias`](../imagesfolderalias/) . على سبيل المثال، إذا كان كلاهما`ResourceFolderAlias` و[`FontsFolderAlias`](../fontsfolderalias/) إذا تم تحديدها، فسيتم إنشاء عناوين URI للخطوط باستخدام [`FontsFolderAlias`](../fontsfolderalias/)، بينما سيتم إنشاء عناوين URI للصور وCSS باستخدام `ResourceFolderAlias`.

لو`ResourceFolderAlias` فارغ،[`ResourceFolder`](../resourcefolder/) سيتم استخدام قيمة الخاصية لإنشاء عناوين URI للموارد.

لو`ResourceFolderAlias` إذا تم تعيينه على '.' (نقطة)، فإن عناوين URI للموارد ستحتوي على أسماء الملفات فقط، بدون أي مسار.

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
