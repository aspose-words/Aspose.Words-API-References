---
title: "Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath metod"
linktitle: "get_ConvertShapeToOfficeMath"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath metod. Hämtar eller anger om former med EquationXML ska konverteras till Office Math‑objekt i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.loading/loadoptions/get_convertshapetoofficemath/
---
## LoadOptions::get_ConvertShapeToOfficeMath method


Hämtar eller anger om former med EquationXML ska konverteras till Office [Math](../../../aspose.words.math/) objekt.

```cpp
bool Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath() const
```


## Exempel



Visar hur man konverterar EquationXML‑former till Office [Math](../../../aspose.words.math/) objekt.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();

// Använd den här flaggan för att ange om former med EquationXML‑attribut ska konverteras
// till Office Math‑objekt och sedan ladda dokumentet.
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

## Se även

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
