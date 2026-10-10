---
title: "Aspose::Words::Math::OfficeMathDisplayType enum"
linktitle: "OfficeMathDisplayType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Math::OfficeMathDisplayType enum. Especifica el tipo de formato de visualización de la ecuación en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.math/officemathdisplaytype/
---
## OfficeMathDisplayType enum


Especifica el tipo de formato de visualización de la ecuación.

```cpp
enum class OfficeMathDisplayType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Display | 0 | El Office [Math](../) se muestra en una línea propia. |
| Inline | 1 | El Office [Math](../) se muestra en línea con el texto. |


## Ejemplos



Muestra cómo establecer el formato de visualización de Office Math.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto officeMath = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

// Los nodos OfficeMath que son hijos de otros nodos OfficeMath siempre están en línea.
// El nodo con el que estamos trabajando es el nodo base para cambiar su ubicación y tipo de visualización.
ASSERT_EQ(Aspose::Words::Math::MathObjectType::OMathPara, officeMath->get_MathObjectType());
ASSERT_EQ(Aspose::Words::NodeType::OfficeMath, officeMath->get_NodeType());
ASPOSE_ASSERT_EQ(officeMath->get_ParentNode(), officeMath->get_ParentParagraph());

// Cambiar la ubicación y el tipo de visualización del nodo OfficeMath.
officeMath->set_DisplayType(Aspose::Words::Math::OfficeMathDisplayType::Display);
officeMath->set_Justification(Aspose::Words::Math::OfficeMathJustification::Left);

doc->Save(get_ArtifactsDir() + u"Shape.OfficeMath.docx");
```

## Ver también

* Namespace [Aspose::Words::Math](../)
* Library [Aspose.Words for C++](../../)
