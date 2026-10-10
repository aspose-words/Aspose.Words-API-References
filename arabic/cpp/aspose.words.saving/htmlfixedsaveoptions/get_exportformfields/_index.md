---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields طريقة"
linktitle: "get_ExportFormFields"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields طريقة. يحصل أو يحدد إشارة ما إذا كانت حقول النموذج تُصدَّر كعناصر تفاعلية (كعلامة ''input'') بدلاً من تحويلها إلى نص أو رسومات في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportformfields/
---
## HtmlFixedSaveOptions::get_ExportFormFields method


يحصل أو يضبط إشارة ما إذا كانت حقول النموذج تُصدّر كعناصر تفاعلية (كوسم 'input') بدلاً من تحويلها إلى نص أو رسومات.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields() const
```


## أمثلة



يظهر كيفية تصدير حقول النموذج إلى Html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertCheckBox(u"CheckBox", false, 15);

// عند تصدير مستند يحتوي على حقول نموذج إلى .html،
// هناك طريقتان يمكن من خلالهما Aspose.Words تصدير حقول النموذج.
// ضبط علامة "ExportFormFields" إلى "true" سيقوم بتصديرها ككائنات تفاعلية.
// ضبط هذه العلامة إلى "false" سيعرض حقول النموذج كنص عادي.
// سيؤدي ذلك إلى تجميدها عند قيمتها الحالية، ومنع قارئ مستند HTML الخاص بنا
// من القدرة على التفاعل معها.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportFormFields(exportFormFields);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportFormFields.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportFormFields.html");

if (exportFormFields)
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>") + u"<input style=\"position:absolute; left:0pt; top:0pt;\" type=\"checkbox\" name=\"CheckBox\" />")->get_Success());
}
else
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>") + u"<div class=\"awdiv\" style=\"left:0.8pt; top:0.8pt; width:14.25pt; height:14.25pt; border:solid 0.75pt #000000;\"")->get_Success());
}
```

## انظر أيضًا

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
