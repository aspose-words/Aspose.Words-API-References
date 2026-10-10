---
title: "Aspose::Words::Math::OfficeMathDisplayType enum"
linktitle: "OfficeMathDisplayType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Math::OfficeMathDisplayType enum. Specifica il tipo di formato di visualizzazione dell'equazione in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.math/officemathdisplaytype/
---
## OfficeMathDisplayType enum


Specifica il tipo di formato di visualizzazione dell'equazione.

```cpp
enum class OfficeMathDisplayType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Display | 0 | L'Office [Math](../) viene visualizzato su una propria riga. |
| Inline | 1 | L'Office [Math](../) viene visualizzato inline con il testo. |


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
