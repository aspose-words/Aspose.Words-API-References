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


Gets or sets whether to convert shapes with EquationXML to Office [Math](../../../aspose.words.math/) objects.

```cpp
bool Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath() const
```


## Examples



Shows how to convert EquationXML shapes to Office [Math](../../../aspose.words.math/) objects. 
```cpp
auto loadOptions = MakeObject<LoadOptions>();

// Use this flag to specify whether to convert the shapes with EquationXML attributes
// to Office Math objects and then load the document.
loadOptions->set_ConvertShapeToOfficeMath(isConvertShapeToOfficeMath);

auto doc = MakeObject<Document>(MyDir + u"Math shapes.docx", loadOptions);

if (isConvertShapeToOfficeMath)
{
    ASSERT_EQ(16, doc->GetChildNodes(NodeType::Shape, true)->get_Count());
    ASSERT_EQ(34, doc->GetChildNodes(NodeType::OfficeMath, true)->get_Count());
}
else
{
    ASSERT_EQ(24, doc->GetChildNodes(NodeType::Shape, true)->get_Count());
    ASSERT_EQ(0, doc->GetChildNodes(NodeType::OfficeMath, true)->get_Count());
}
```

## See Also

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
