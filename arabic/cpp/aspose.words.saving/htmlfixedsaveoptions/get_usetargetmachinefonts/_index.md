---
title: "طريقة Aspose::Words::Saving::HtmlFixedSaveOptions::get_UseTargetMachineFonts"
linktitle: "get_UseTargetMachineFonts"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::HtmlFixedSaveOptions::get_UseTargetMachineFonts. العلم يشير إلى ما إذا كان يجب استخدام الخطوط من الجهاز المستهدف لعرض المستند. إذا تم تعيين هذا العلم إلى true، فإن خاصيتي FontFormat و ExportEmbeddedFonts لا تأثير لهما، كما أن ResourceSavingCallback لا يتم استدعاؤه للخطوط. القيمة الافتراضية هي false في C++."
type: docs
weight: 20000
url: /ar/cpp/aspose.words.saving/htmlfixedsaveoptions/get_usetargetmachinefonts/
---
## HtmlFixedSaveOptions::get_UseTargetMachineFonts method


العلم يشير إلى ما إذا كان يجب استخدام الخطوط من الجهاز المستهدف لعرض المستند. إذا تم تعيين هذا العلم إلى **true**، فإن خاصيتي [FontFormat](../get_fontformat/) و [ExportEmbeddedFonts](../get_exportembeddedfonts/) لا تأثير لهما، كما أن [ResourceSavingCallback](../get_resourcesavingcallback/) لا يتم استدعاؤه للخطوط. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_UseTargetMachineFonts() const
```


## أمثلة



يظهر كيفية استخدام الخطوط فقط من الجهاز المستهدف عند حفظ مستند إلى HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Bullet points with alternative font.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
saveOptions->set_ExportEmbeddedCss(true);
saveOptions->set_UseTargetMachineFonts(useTargetMachineFonts);
saveOptions->set_FontFormat(Aspose::Words::Saving::ExportFontFormat::Ttf);
saveOptions->set_ExportEmbeddedFonts(false);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.UsingMachineFonts.html");

if (useTargetMachineFonts)
{
    ASSERT_FALSE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"@font-face")->get_Success());
}
else
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], ") + u"url[(]'HtmlFixedSaveOptions.UsingMachineFonts/font001.ttf'[)] format[(]'truetype'[)]; }")->get_Success());
}
```

## انظر أيضًا

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
