---
title: "Aspose::Words::Math::OfficeMathJustification enum"
linktitle: "OfficeMathJustification"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Math::OfficeMathJustification enum. Specifica la giustificazione dell'equazione in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.math/officemathjustification/
---
## OfficeMathJustification enum


Specifica l'allineamento dell'equazione.

```cpp
enum class OfficeMathJustification
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| CenterGroup | 1 | Giustifica le istanze di testo matematico a sinistra rispetto a ciascuna, e centra il gruppo di testo matematico (il [Math](../)[Paragraph](../../aspose.words/paragraph/)) rispetto alla pagina. |
| Centro | 2 | Centra individualmente ciascuna istanza di testo matematico rispetto ai margini. |
| Left | 3 | Allineamento a sinistra del [Math](../)[Paragraph](../../aspose.words/paragraph/). |
| Right | 4 | Allineamento a destra del [Math](../)[Paragraph](../../aspose.words/paragraph/). |
| Inline | 7 | Posizione [Inline](../../aspose.words/inline/) di [Math](../). |
| Default | n/a | Valore predefinito [CenterGroup](./). |


## Esempi



Mostra come impostare la formattazione di visualizzazione di Office Math.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto officeMath = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

// I nodi OfficeMath che sono figli di altri nodi OfficeMath sono sempre inline.
// Il nodo con cui stiamo lavorando è il nodo base per modificare la sua posizione e il tipo di visualizzazione.
ASSERT_EQ(Aspose::Words::Math::MathObjectType::OMathPara, officeMath->get_MathObjectType());
ASSERT_EQ(Aspose::Words::NodeType::OfficeMath, officeMath->get_NodeType());
ASPOSE_ASSERT_EQ(officeMath->get_ParentNode(), officeMath->get_ParentParagraph());

// Modifica la posizione e il tipo di visualizzazione del nodo OfficeMath.
officeMath->set_DisplayType(Aspose::Words::Math::OfficeMathDisplayType::Display);
officeMath->set_Justification(Aspose::Words::Math::OfficeMathJustification::Left);

doc->Save(get_ArtifactsDir() + u"Shape.OfficeMath.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Math](../)
* Library [Aspose.Words for C++](../../)
