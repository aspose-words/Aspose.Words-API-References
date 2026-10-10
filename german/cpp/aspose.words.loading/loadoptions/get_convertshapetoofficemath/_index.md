---
title: "Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath Methode"
linktitle: "get_ConvertShapeToOfficeMath"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath Methode. Gibt an oder legt fest, ob Formen mit EquationXML in Office‑Math‑Objekte konvertiert werden sollen in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words.loading/loadoptions/get_convertshapetoofficemath/
---
## LoadOptions::get_ConvertShapeToOfficeMath method


Gibt an oder legt fest, ob Formen mit EquationXML in Office [Math](../../../aspose.words.math/) Objekte konvertiert werden.

```cpp
bool Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath() const
```


## Beispiele



Zeigt, wie man EquationXML‑Formen in Office [Math](../../../aspose.words.math/) Objekte konvertiert.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();

// Verwenden Sie dieses Flag, um anzugeben, ob die Formen mit EquationXML‑Attributen konvertiert werden sollen
// zu Office‑Math‑Objekten und anschließend das Dokument zu laden.
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

## Siehe auch

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
