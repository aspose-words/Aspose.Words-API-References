---
title: "طريقة Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath"
linktitle: "get_ConvertShapeToOfficeMath"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath. يحصل أو يحدد ما إذا كان سيتم تحويل الأشكال التي تحتوي على EquationXML إلى كائنات Office Math في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.loading/loadoptions/get_convertshapetoofficemath/
---
## LoadOptions::get_ConvertShapeToOfficeMath method


يحصل أو يحدد ما إذا كان سيتم تحويل الأشكال التي تحتوي على EquationXML إلى كائنات Office [Math](../../../aspose.words.math/).

```cpp
bool Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath() const
```


## أمثلة



يظهر كيفية تحويل أشكال EquationXML إلى كائنات Office [Math](../../../aspose.words.math/).
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();

// استخدم هذه العلامة لتحديد ما إذا كان سيتم تحويل الأشكال التي تحتوي على سمات EquationXML
// إلى كائنات Office Math ثم تحميل المستند.
loadOptions->set_ConvertShapeToOfficeMath(isConvertShapeToOfficeMath);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Math shapes.docx", loadOptions);

if (isConvertShapeToOfficeMath)
{
    ASSERT_EQ(16, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
    ASSERT_EQ(34, doc->GetChildNodes(Aspose::Words::NodeType::OfficeMath, true)->get_Count());
}
else
{
    ASSERT_EQ(24, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
    ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::OfficeMath, true)->get_Count());
}
```

## انظر أيضًا

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
