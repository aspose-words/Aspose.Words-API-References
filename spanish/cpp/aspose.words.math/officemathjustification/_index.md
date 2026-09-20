---
title: "Aspose::Words::Math::OfficeMathJustification enum"
linktitle: "OfficeMathJustification"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Math::OfficeMathJustification enum. Especifica la justificación de la ecuación en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.math/officemathjustification/
---
## OfficeMathJustification enum


Especifica la justificación de la ecuación.

```cpp
enum class OfficeMathJustification
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| CenterGroup | 1 | Justifica las instancias de texto matemático a la izquierda respecto a cada una, y centra el grupo de texto matemático (el [Math](../)[Paragraph](../../aspose.words/paragraph/)) respecto a la página. |
| Centro | 2 | Centra cada instancia de texto matemático individualmente respecto a los márgenes. |
| Left | 3 | Justificación a la izquierda de [Math](../)[Paragraph](../../aspose.words/paragraph/). |
| Right | 4 | Justificación a la derecha de [Math](../)[Paragraph](../../aspose.words/paragraph/). |
| Inline | 7 | Posición [Inline](../../aspose.words/inline/) de [Math](../). |
| Default | n/a | Valor predeterminado [CenterGroup](./). |


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
