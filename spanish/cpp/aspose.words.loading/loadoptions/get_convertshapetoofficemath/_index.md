---
title: "Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath método"
linktitle: "get_ConvertShapeToOfficeMath"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath método. Obtiene o establece si se convierten las formas con EquationXML a objetos Office Math en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.loading/loadoptions/get_convertshapetoofficemath/
---
## LoadOptions::get_ConvertShapeToOfficeMath method


Obtiene o establece si se convierten las formas con EquationXML a objetos Office [Math](../../../aspose.words.math/).

```cpp
bool Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath() const
```


## Ejemplos



Muestra cómo convertir formas EquationXML a objetos Office [Math](../../../aspose.words.math/).
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();

// Utilice esta bandera para especificar si se convierten las formas con atributos EquationXML
// a objetos Office Math y luego cargar el documento.
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

## Ver también

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
