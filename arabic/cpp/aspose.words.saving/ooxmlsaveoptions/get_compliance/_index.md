---
title: "طريقة Aspose::Words::Saving::OoxmlSaveOptions::get_Compliance"
linktitle: "get_Compliance"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::OoxmlSaveOptions::get_Compliance. يحدد إصدار OOXML للمستند الناتج. القيمة الافتراضية هي Ecma376_2006 في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.saving/ooxmlsaveoptions/get_compliance/
---
## OoxmlSaveOptions::get_Compliance method


يحدد إصدار OOXML للمستند الناتج. القيمة الافتراضية هي [Ecma376_2006](../../ooxmlcompliance/).

```cpp
Aspose::Words::Saving::OoxmlCompliance Aspose::Words::Saving::OoxmlSaveOptions::get_Compliance()
```


## أمثلة



يوضح كيفية تعيين مواصفة امتثال OOXML لمستند محفوظ للالتزام بها.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إذا قمنا بتكوين خيارات التوافق للامتثال مع Microsoft Word 2003،
// إدراج صورة سيحدد شكلها باستخدام VML.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2003);
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Vml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());

// معيار OOXML "ISO/IEC 29500:2008" لا يدعم أشكال VML.
// إذا قمنا بتعيين خاصية "Compliance" لكائن SaveOptions إلى "OoxmlCompliance.Iso29500_2008_Strict",
// أي مستند نقوم بحفظه مع تمرير هذا الكائن سيتعين عليه اتباع ذلك المعيار.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Docx);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// المستند المحفوظ لدينا يحدد الشكل باستخدام DML للالتزام بمعيار OOXML "ISO/IEC 29500:2008".
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Dml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());
```


يوضح كيفية تكوين قائمة لإعادة بدء الترقيم في كل قسم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->idx_get(0);
list->set_IsRestartAtEachSection(restartListAtEachSection);

// خاصية "IsRestartAtEachSection" ستكون صالحة فقط عندما
// مستوى امتثال OOXML للمستند هو معيار أحدث من "OoxmlComplianceCore.Ecma376".
auto options = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
options->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

builder->get_ListFormat()->set_List(list);

builder->Writeln(u"List item 1");
builder->Writeln(u"List item 2");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Writeln(u"List item 3");
builder->Writeln(u"List item 4");

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.RestartingDocumentList.docx", options);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.RestartingDocumentList.docx");

ASPOSE_ASSERT_EQ(restartListAtEachSection, doc->get_Lists()->idx_get(0)->get_IsRestartAtEachSection());
```


يوضح كيفية إدراج أشكال DML في مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// فيما يلي نوعان من التغليف التي قد تمتلكها الأشكال.
// 1 -  عائم:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::TopCornersRounded, Aspose::Words::Drawing::RelativeHorizontalPosition::Page, 100, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 100, 50, 50, Aspose::Words::Drawing::WrapType::None);

// 2 -  مدمج:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::DiagonalCornersRounded, 50, 50);

// إذا كنت بحاجة لإنشاء أشكال "غير أولية"، مثل SingleCornerSnipped، TopCornersSnipped، DiagonalCornersSnipped،
// TopCornersOneRoundedOneSnipped، SingleCornerRounded، TopCornersRounded، أو DiagonalCornersRounded،
// ثم احفظ المستند مع امتثال "Strict" أو "Transitional"، مما يسمح بحفظ الشكل كـ DML.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(get_ArtifactsDir() + u"Shape.ShapeInsertion.docx", saveOptions);
```

## انظر أيضًا

* Enum [OoxmlCompliance](../../ooxmlcompliance/)
* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
