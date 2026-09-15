---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources طريقة"
linktitle: "get_ExportCidUrlsForMhtmlResources"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources طريقة. يحدد ما إذا كان يجب استخدام عناوين URL من نوع CID (Content-ID) للإشارة إلى الموارد (الصور، الخطوط، CSS) المضمنة في مستندات MHTML. القيمة الافتراضية هي false في C++."
type: docs
weight: 13000
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/get_exportcidurlsformhtmlresources/
---
## HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources method


يحدد ما إذا كان سيتم استخدام عناوين URL من نوع CID (Content-ID) للإشارة إلى الموارد (الصور، الخطوط، CSS) المتضمنة في مستندات MHTML. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources() const
```

## ملاحظات


هذا الخيار يؤثر فقط على المستندات التي يتم حفظها إلى MHTML.

بشكل افتراضي، يتم الإشارة إلى الموارد في مستندات MHTML بواسطة اسم الملف (على سبيل المثال، "image.png")، والذي يُطابق رؤوس "Content-Location" لأجزاء MIME.

هذا الخيار يتيح طريقة بديلة، حيث تُكتب الإشارات إلى ملفات الموارد كعناوين URL من نوع CID (Content-ID) (على سبيل المثال، "cid:image.png") وتُطابق مع رؤوس "Content-ID".

نظريًا، لا ينبغي أن يكون هناك فرق بين طريقتي الإشارة ويجب أن تعمل أي منهما بشكل جيد في أي متصفح أو عميل بريد. عمليًا، ومع ذلك، بعض العملاء يفشلون في جلب الموارد بواسطة اسم الملف. إذا كان متصفحك أو عميل البريد يرفض تحميل الموارد المضمنة في مستند MTHML (لا يعرض الصور أو لا يحمل أنماط CSS)، جرّب تصدير المستند باستخدام عناوين CID.

## أمثلة



يوضح كيفية تمكين معرفات المحتوى لمستندات MHTML الناتجة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// ضبط هذه العلامة سيستبدل وسوم "Content-Location"
// بوسوم "Content-ID" لكل مورد من المستند الإدخالي.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Mhtml);
options->set_ExportCidUrlsForMhtmlResources(exportCidUrlsForMhtmlResources);
options->set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType::External);
options->set_ExportFontResources(true);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ContentIdUrls.mht", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ContentIdUrls.mht");

if (exportCidUrlsForMhtmlResources)
{
    ASSERT_TRUE(outDocContents.Contains(u"Content-ID: <document.html>"));
    ASSERT_TRUE(outDocContents.Contains(u"<link href=3D\"cid:styles.css\" type=3D\"text/css\" rel=3D\"stylesheet\" />"));
    ASSERT_TRUE(outDocContents.Contains(u"@font-face { font-family:'Arial Black'; font-weight:bold; src:url('cid:arib=\r\nlk.ttf') }"));
    ASSERT_TRUE(outDocContents.Contains(u"<img src=3D\"cid:image.003.jpeg\" width=3D\"350\" height=3D\"180\" alt=3D\"\" />"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"Content-Location: document.html"));
    ASSERT_TRUE(outDocContents.Contains(u"<link href=3D\"styles.css\" type=3D\"text/css\" rel=3D\"stylesheet\" />"));
    ASSERT_TRUE(outDocContents.Contains(u"@font-face { font-family:'Arial Black'; font-weight:bold; src:url('ariblk.t=\r\ntf') }"));
    ASSERT_TRUE(outDocContents.Contains(u"<img src=3D\"image.003.jpeg\" width=3D\"350\" height=3D\"180\" alt=3D\"\" />"));
}
```

## انظر أيضًا

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
