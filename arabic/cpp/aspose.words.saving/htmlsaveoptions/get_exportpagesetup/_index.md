---
title: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup"
linktitle: "get_ExportPageSetup"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup. يحدد ما إذا كان إعداد الصفحة يتم تصديره إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي false في C++."
type: docs
weight: 24000
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/get_exportpagesetup/
---
## HtmlSaveOptions::get_ExportPageSetup method


يحدد ما إذا كان إعداد الصفحة يتم تصديره إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup() const
```

## ملاحظات


كل [Section](../../../aspose.words/section/) في نموذج مستندات Aspose.Words يوفر معلومات إعداد الصفحة عبر فئة [PageSetup](../../../aspose.words/pagesetup/). عند تصدير مستند إلى تنسيق HTML قد تحتاج إلى الاحتفاظ بهذه المعلومات للاستخدام لاحقًا. على وجه الخصوص، قد يكون إعداد الصفحة مهمًا للتصيير إلى وسائط مقسمة إلى صفحات (الطباعة) أو للتحويل اللاحق إلى صيغ ملفات Microsoft Word الأصلية (DOCX، DOC، RTF، WML).

في معظم الحالات يُقصد بـ HTML للعرض في المتصفحات حيث لا يتم تنفيذ التقسيم إلى صفحات. لذلك تكون هذه الميزة غير مفعلة افتراضيًا.

## أمثلة



يوضح كيفية اتخاذ القرار بشأن ما إذا كان يجب الحفاظ على بنية القسم/معلومات إعداد الصفحة عند الحفظ إلى HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_TopMargin(36.0);
pageSetup->set_BottomMargin(36.0);
pageSetup->set_PaperSize(Aspose::Words::PaperSize::A5);

// عند حفظ المستند كـ HTML، يمكننا تمرير كائن SaveOptions
// لتحديد ما إذا كان يجب الحفاظ على إعدادات الصفحة أو تجاهلها.
// إذا قمنا بتعيين علامة "ExportPageSetup" إلى "true"، سيحتوي مستند HTML الناتج على تكوين إعداد الصفحة الخاص بنا.
// إذا قمنا بتعيين علامة "ExportPageSetup" إلى "false"، ستتجاهل عملية الحفظ إعدادات الصفحة الخاصة بنا
// للقسم الأول، وستظهر كلا القسمين متطابقتين.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportPageSetup(exportPageSetup);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportPageSetup.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportPageSetup.html");

if (exportPageSetup)
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<style type=\"text/css\">") + u"@page Section_1 { size:419.55pt 595.3pt; margin:36pt 70.85pt; -aw-footer-distance:35.4pt; -aw-header-distance:35.4pt }" + u"@page Section_2 { size:612pt 792pt; margin:70.85pt; -aw-footer-distance:35.4pt; -aw-header-distance:35.4pt }" + u"div.Section_1 { page:Section_1 }div.Section_2 { page:Section_2 }" + u"</style>"));

    ASSERT_TRUE(outDocContents.Contains(System::String(u"<div class=\"Section_1\">") + u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" + u"<span>Section 1</span>" + u"</p>" + u"</div>"));
}
else
{
    ASSERT_FALSE(outDocContents.Contains(u"style type=\"text/css\">"));

    ASSERT_TRUE(outDocContents.Contains(System::String(u"<div>") + u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" + u"<span>Section 1</span>" + u"</p>" + u"</div>"));
}
```

## انظر أيضًا

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
