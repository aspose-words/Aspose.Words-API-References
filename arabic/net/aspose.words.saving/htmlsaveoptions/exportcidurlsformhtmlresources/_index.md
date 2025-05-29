---
title: HtmlSaveOptions.ExportCidUrlsForMhtmlResources
linktitle: ExportCidUrlsForMhtmlResources
articleTitle: ExportCidUrlsForMhtmlResources
second_title: Aspose.Words لـ .NET
description: اكتشف كيف يُحسّن ExportCidUrlsForMhtmlResources من HtmlSaveOptions مستندات MHTML من خلال تفعيل عناوين URL الخاصة بـ CID للصور والخطوط وCSS. افتراضيًا، خطأ.
type: docs
weight: 110
url: /ar/net/aspose.words.saving/htmlsaveoptions/exportcidurlsformhtmlresources/
---
## HtmlSaveOptions.ExportCidUrlsForMhtmlResources property

يُحدد ما إذا كان سيتم استخدام عناوين URL لمعرف المحتوى (CID) للإشارة إلى الموارد (الصور، الخطوط، CSS) المضمنة في مستندات MHTML . القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool ExportCidUrlsForMhtmlResources { get; set; }
```

## ملاحظات

يؤثر هذا الخيار فقط على المستندات المحفوظة بتنسيق MHTML.

بشكل افتراضي، تتم الإشارة إلى الموارد في مستندات MHTML حسب اسم الملف (على سبيل المثال، "image.png")، والتي تتم مطابقتها مع رؤوس "Content-Location" لأجزاء MIME.

يتيح هذا الخيار طريقة بديلة، حيث تتم كتابة المراجع إلى ملفات الموارد كعناوين URL CID (Content-ID) (على سبيل المثال، "cid:image.png") ويتم مطابقتها مع رؤوس "Content-ID".

نظريًا، لا ينبغي أن يكون هناك فرق بين طريقتي الإشارة، ويجب أن تعمل أي منهما بشكل جيد في أي متصفح أو وكيل بريد. مع ذلك، عمليًا، تفشل بعض الوكلاء في جلب الموارد حسب اسم الملف. إذا رفض متصفحك أو وكيل بريدك تحميل الموارد المضمنة في مستند MTHML (لا يعرض صورًا أو لا يحمل أنماط CSS)، فحاول تصدير المستند باستخدام عناوين URL لمعرفات CID.

## أمثلة

يوضح كيفية تمكين معرفات المحتوى لمستندات MHTML الناتجة.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// سيؤدي تعيين هذا العلم إلى استبدال علامات "المحتوى-الموقع"
// مع علامات "Content-ID" لكل مورد من مستند الإدخال.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Mhtml)
{
    ExportCidUrlsForMhtmlResources = exportCidUrlsForMhtmlResources,
    CssStyleSheetType = CssStyleSheetType.External,
    ExportFontResources = true,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ContentIdUrls.mht", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ContentIdUrls.mht");

if (exportCidUrlsForMhtmlResources)
{
    Assert.True(outDocContents.Contains("Content-ID: <document.html>"));
    Assert.True(outDocContents.Contains("<link href=3D\"cid:styles.css\" type=3D\"text/css\" rel=3D\"stylesheet\" />"));
    Assert.True(outDocContents.Contains("@font-face { font-family:'Arial Black'; font-weight:bold; src:url('cid:arib=\r\nlk.ttf') }"));
    Assert.True(outDocContents.Contains("<img src=3D\"cid:image.003.jpeg\" width=3D\"350\" height=3D\"180\" alt=3D\"\" />"));
}
else
{
    Assert.True(outDocContents.Contains("Content-Location: document.html"));
    Assert.True(outDocContents.Contains("<link href=3D\"styles.css\" type=3D\"text/css\" rel=3D\"stylesheet\" />"));
    Assert.True(outDocContents.Contains("@font-face { font-family:'Arial Black'; font-weight:bold; src:url('ariblk.t=\r\ntf') }"));
    Assert.True(outDocContents.Contains("<img src=3D\"image.003.jpeg\" width=3D\"350\" height=3D\"180\" alt=3D\"\" />"));
}
```

### أنظر أيضا

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
