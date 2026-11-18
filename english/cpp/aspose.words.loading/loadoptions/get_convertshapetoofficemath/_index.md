---
title: Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath method
linktitle: get_ConvertShapeToOfficeMath
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath method. Gets or sets whether to convert shapes with EquationXML to Office Math objects in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.loading/loadoptions/get_convertshapetoofficemath/
---
## LoadOptions::get_ConvertShapeToOfficeMath method


Gets or sets whether to convert shapes with EquationXML to Office Math objects.

```cpp
_Bool Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath() const
```

## Examples


Shows how to convert EquationXML shapes to Office Math objects.

```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();

// Use this flag to specify whether to convert the shapes with EquationXML attributes
// to Office Math objects and then load the document.
loadOptions->set_ConvertShapeToOfficeMath(isConvertShapeToOfficeMath);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Math shapes.docx", loadOptions);

if (isConvertShapeToOfficeMath)
{
    ASSERT_EQ(doc->GetChildNodes(NodeType::Shape, true)->get_Count(), 16);
    ASSERT_EQ(doc->GetChildNodes(NodeType::OfficeMath, true)->get_Count(), 34);
}
else
{
    ASSERT_EQ(doc->GetChildNodes(NodeType::Shape, true)->get_Count(), 24);
    ASSERT_EQ(doc->GetChildNodes(NodeType::OfficeMath, true)->get_Count(), 0);
}
```
## See Also

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
