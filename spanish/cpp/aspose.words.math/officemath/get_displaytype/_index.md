---
title: "Aspose::Words::Math::OfficeMath::get_DisplayType método"
linktitle: "get_DisplayType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Math::OfficeMath::get_DisplayType método. Obtiene/establece el tipo de formato de visualización de Office Math que representa si una ecuación se muestra en línea con el texto o se muestra en una línea propia en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.math/officemath/get_displaytype/
---
## OfficeMath::get_DisplayType method


Obtiene/establece el tipo de formato de visualización de Office [Math](../../) que representa si una ecuación se muestra en línea con el texto o se muestra en una línea propia.

```cpp
Aspose::Words::Math::OfficeMathDisplayType Aspose::Words::Math::OfficeMath::get_DisplayType()
```

## Observaciones


El tipo de formato de visualización tiene efecto solo para el Office [Math](../../) de nivel superior.

El tipo de formato de visualización devuelto es siempre [Inline](../../officemathdisplaytype/) para Office [Math](../../) anidados.

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

* Enum [OfficeMathDisplayType](../../officemathdisplaytype/)
* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words for C++](../../../)
