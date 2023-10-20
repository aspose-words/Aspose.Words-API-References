---
title: HtmlSaveOptions.ResourceFolderAlias
linktitle: ResourceFolderAlias
articleTitle: ResourceFolderAlias
second_title: Aspose.Words لـ .NET
description: HtmlSaveOptions ResourceFolderAlias ملكية. يحدد اسم المجلد المستخدم لإنشاء URIs لجميع الموارد المكتوبة في مستند HTML. الافتراضي هو سلسلة فارغة في C#.
type: docs
weight: 430
url: /ar/net/aspose.words.saving/htmlsaveoptions/resourcefolderalias/
---
## HtmlSaveOptions.ResourceFolderAlias property

يحدد اسم المجلد المستخدم لإنشاء URIs لجميع الموارد المكتوبة في مستند HTML. الافتراضي هو سلسلة فارغة.

```csharp
public string ResourceFolderAlias { get; set; }
```

## ملاحظات

`ResourceFolderAlias` هي أبسط طريقة لتحديد كيفية إنشاء معرفات URI لجميع ملفات الموارد. يمكن تحديد نفس المعلومات للصور والخطوط بشكل منفصل عبر[`ImagesFolderAlias`](../imagesfolderalias/) و[`FontsFolderAlias`](../fontsfolderalias/) الخصائص، على التوالي. ومع ذلك، لا توجد خاصية فردية لـ CSS.

`ResourceFolderAlias` لديه أولوية أقل من[`FontsFolderAlias`](../fontsfolderalias/) و[`ImagesFolderAlias`](../imagesfolderalias/) . على سبيل المثال، إذا كان كلاهما`ResourceFolderAlias` و[`FontsFolderAlias`](../fontsfolderalias/) تم تحديد عناوين URL الخاصة بالخطوط باستخدام [`FontsFolderAlias`](../fontsfolderalias/) ، بينما سيتم إنشاء معرفات URI للصور وCSS باستخدام `ResourceFolderAlias`.

لو`ResourceFolderAlias` فارغة،[`ResourceFolder`](../resourcefolder/)سيتم استخدام قيمة الخاصية لإنشاء معرفات URI للمورد.

لو`ResourceFolderAlias` تم ضبطه على "." (نقطة)، ستحتوي معرفات الموارد المنتظمة (URI) للمورد على أسماء الملفات فقط، بدون أي مسار.

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
