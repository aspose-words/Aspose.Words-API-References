---
title: "Aspose::Words::Math::OfficeMath::get_Justification método"
linktitle: "get_Justification"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Math::OfficeMath::get_Justification método. Obtiene/establece la justificación de Office Math en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.math/officemath/get_justification/
---
## OfficeMath::get_Justification method


Obtiene/establece la justificación de Office [Math](../../).

```cpp
Aspose::Words::Math::OfficeMathJustification Aspose::Words::Math::OfficeMath::get_Justification()
```

## Observaciones


No se puede establecer la justificación del Office [Math](../../) con el tipo de formato de visualización [Inline](../../officemathdisplaytype/).

[Inline](../../../aspose.words/inline/) justification cannot be set to the Office [Math](../../) with display format type [Display](../../officemathdisplaytype/).

El [DisplayType](../get_displaytype/) correspondiente debe establecerse antes de establecer la justificación del Office [Math](../../).

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

* Enum [OfficeMathJustification](../../officemathjustification/)
* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words for C++](../../../)
