---
title: "metodo Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath"
linktitle: "get_ConvertShapeToOfficeMath"
second_title: "Riferimento API Aspose.Words per C++"
description: "metodo Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath. Ottiene o imposta se convertire le forme con EquationXML in oggetti Office Math in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.loading/loadoptions/get_convertshapetoofficemath/
---
## LoadOptions::get_ConvertShapeToOfficeMath method


Ottiene o imposta se convertire le forme con EquationXML in oggetti Office [Math](../../../aspose.words.math/).

```cpp
bool Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath() const
```


## Esempi



Mostra come convertire le forme EquationXML in oggetti Office [Math](../../../aspose.words.math/).
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();

// Utilizza questo flag per specificare se convertire le forme con attributi EquationXML
// in oggetti Office Math e poi caricare il documento.
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

## Vedi anche

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
