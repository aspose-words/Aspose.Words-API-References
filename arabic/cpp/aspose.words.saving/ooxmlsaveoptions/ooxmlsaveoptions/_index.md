---
title: "منشئ Aspose::Words::Saving::OoxmlSaveOptions::OoxmlSaveOptions"
linktitle: "OoxmlSaveOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "منشئ Aspose::Words::Saving::OoxmlSaveOptions::OoxmlSaveOptions. يهيء مثيلاً جديداً لهذه الفئة يمكن استخدامه لحفظ مستند بتنسيق Docx في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.saving/ooxmlsaveoptions/ooxmlsaveoptions/
---
## OoxmlSaveOptions::OoxmlSaveOptions() constructor


يهيء مثيلاً جديداً لهذه الفئة يمكن استخدامه لحفظ مستند بتنسيق [Docx](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::Saving::OoxmlSaveOptions::OoxmlSaveOptions()
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

## انظر أيضًا

* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## OoxmlSaveOptions::OoxmlSaveOptions(Aspose::Words::SaveFormat) constructor


يهيء مثيلاً جديداً لهذه الفئة يمكن استخدامه لحفظ مستند بتنسيق [Docx](../../../aspose.words/saveformat/)، [Docm](../../../aspose.words/saveformat/)، [Dotx](../../../aspose.words/saveformat/)، [Dotm](../../../aspose.words/saveformat/) أو [FlatOpc](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::Saving::OoxmlSaveOptions::OoxmlSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | يمكن أن يكون [Docx](../../../aspose.words/saveformat/)، [Docm](../../../aspose.words/saveformat/)، [Dotx](../../../aspose.words/saveformat/)، [Dotm](../../../aspose.words/saveformat/) أو [FlatOpc](../../../aspose.words/saveformat/). |

## أمثلة



يوضح كيفية دعم أحرف التحكم القديمة عند التحويل إلى .docx.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Legacy control character.doc");

// عند حفظ المستند بتنسيق OOXML، يمكننا إنشاء كائن OoxmlSaveOptions
// ثم نمرره إلى طريقة حفظ المستند لتعديل طريقة حفظ المستند.
// عيّن الخاصية "KeepLegacyControlChars" إلى "true" للحفاظ على
// حرف "ShortDateTime" القديم أثناء الحفظ.
// عيّن الخاصية "KeepLegacyControlChars" إلى "false" لإزالة
// حرف "ShortDateTime" القديم من المستند الناتج.
auto so = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
so->set_KeepLegacyControlChars(keepLegacyControlChars);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.KeepLegacyControlChars.docx", so);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.KeepLegacyControlChars.docx");

ASSERT_EQ(keepLegacyControlChars ? System::String(u"\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f") : System::String(u"\u001e\f"), doc->get_FirstSection()->get_Body()->GetText());
```

## انظر أيضًا

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
