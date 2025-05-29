---
title: HtmlSaveOptions.ResourceFolder
linktitle: ResourceFolder
articleTitle: ResourceFolder
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية HtmlSaveOptions ResourceFolder لتصدير المستندات على النحو الأمثل. أدر الصور والخطوط وCSS بسهولة في مجلد مخصص.
type: docs
weight: 440
url: /ar/net/aspose.words.saving/htmlsaveoptions/resourcefolder/
---
## HtmlSaveOptions.ResourceFolder property

يُحدد مجلدًا فعليًا تُحفظ فيه جميع الموارد، مثل الصور والخطوط وCSS الخارجية، عند تصدير document إلى HTML. القيمة الافتراضية هي سلسلة فارغة.

```csharp
public string ResourceFolder { get; set; }
```

## ملاحظات

`ResourceFolder` هي أبسط طريقة لتحديد مجلد يجب كتابة جميع الموارد فيه. طريقة أخرى هي استخدام خصائص فردية[`FontsFolder`](../fontsfolder/) ،[`ImagesFolder`](../imagesfolder/) ، و[`CssStyleSheetFileName`](../cssstylesheetfilename/).

`ResourceFolder` لها أولوية أقل من المجلدات المحددة عبر[`FontsFolder`](../fontsfolder/) ، [`ImagesFolder`](../imagesfolder/) ، و[`CssStyleSheetFileName`](../cssstylesheetfilename/) على سبيل المثال، إذا كان both `ResourceFolder` و[`FontsFolder`](../fontsfolder/)إذا تم تحديد الخطوط، فسيتم حفظها إلى[`FontsFolder`](../fontsfolder/) ، بينما سيتم حفظ الصور وCSS في`ResourceFolder`.

إذا تم تحديد المجلد بواسطة`ResourceFolder` غير موجود، سيتم إنشاؤه تلقائيًا.

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
