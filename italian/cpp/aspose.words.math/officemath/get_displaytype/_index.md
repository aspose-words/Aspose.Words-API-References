---
title: "Aspose::Words::Math::OfficeMath::get_DisplayType metodo"
linktitle: "get_DisplayType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Math::OfficeMath::get_DisplayType. Ottiene/imposta il tipo di formato di visualizzazione di Office Math che rappresenta se un'equazione è visualizzata in linea con il testo o su una propria riga in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.math/officemath/get_displaytype/
---
## OfficeMath::get_DisplayType method


Ottiene/imposta il tipo di formato di visualizzazione di Office [Math](../../) che rappresenta se un'equazione è visualizzata in linea con il testo o su una propria riga.

```cpp
Aspose::Words::Math::OfficeMathDisplayType Aspose::Words::Math::OfficeMath::get_DisplayType()
```

## Note


Il tipo di formato di visualizzazione ha effetto solo per Office [Math](../../) di livello superiore.

Il tipo di formato di visualizzazione restituito è sempre [Inline](../../officemathdisplaytype/) per Office [Math](../../) annidati.

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

* Enum [OfficeMathDisplayType](../../officemathdisplaytype/)
* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words for C++](../../../)
