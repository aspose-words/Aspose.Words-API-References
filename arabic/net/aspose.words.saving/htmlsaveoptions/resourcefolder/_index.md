---
title: HtmlSaveOptions.ResourceFolder
linktitle: ResourceFolder
articleTitle: ResourceFolder
second_title: Aspose.Words لـ .NET
description: HtmlSaveOptions ResourceFolder ملكية. يحدد مجلدًا فعليًا حيث يتم حفظ جميع الموارد مثل الصور والخطوط وCSS الخارجية عند تصدير document إلى HTML. الافتراضي هو سلسلة فارغة في C#.
type: docs
weight: 420
url: /ar/net/aspose.words.saving/htmlsaveoptions/resourcefolder/
---
## HtmlSaveOptions.ResourceFolder property

يحدد مجلدًا فعليًا حيث يتم حفظ جميع الموارد مثل الصور والخطوط وCSS الخارجية عند تصدير document إلى HTML. الافتراضي هو سلسلة فارغة.

```csharp
public string ResourceFolder { get; set; }
```

## ملاحظات

`ResourceFolder` هي أبسط طريقة لتحديد المجلد الذي يجب كتابة جميع الموارد فيه. هناك طريقة أخرى وهي استخدام الخصائص الفردية[`FontsFolder`](../fontsfolder/) ,[`ImagesFolder`](../imagesfolder/) و[`CssStyleSheetFileName`](../cssstylesheetfilename/).

`ResourceFolder` له أولوية أقل من المجلدات المحددة عبر[`FontsFolder`](../fontsfolder/)[`ImagesFolder`](../imagesfolder/) ، و[`CssStyleSheetFileName`](../cssstylesheetfilename/) . على سبيل المثال، إذا كان كلا `ResourceFolder` و[`FontsFolder`](../fontsfolder/)تم تحديد الخطوط، وسيتم حفظها إلى[`FontsFolder`](../fontsfolder/) ، بينما سيتم حفظ الصور وCSS في`ResourceFolder`.

إذا كان المجلد المحدد بواسطة`ResourceFolder` غير موجود، سيتم إنشاؤه تلقائيًا.

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
