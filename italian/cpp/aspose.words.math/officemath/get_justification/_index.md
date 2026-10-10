---
title: "Metodo Aspose::Words::Math::OfficeMath::get_Justification"
linktitle: "get_Justification"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Math::OfficeMath::get_Justification method. Ottiene/imposta la giustificazione di Office Math in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.math/officemath/get_justification/
---
## OfficeMath::get_Justification method


Ottiene/imposta la giustificazione di Office [Math](../../).

```cpp
Aspose::Words::Math::OfficeMathJustification Aspose::Words::Math::OfficeMath::get_Justification()
```

## Note


La giustificazione non può essere impostata per l'Office [Math](../../) con il tipo di formato di visualizzazione [Inline](../../officemathdisplaytype/).

[Inline](../../../aspose.words/inline/) justification cannot be set to the Office [Math](../../) with display format type [Display](../../officemathdisplaytype/).

Il corrispondente [DisplayType](../get_displaytype/) deve essere impostato prima di impostare la giustificazione di Office [Math](../../).

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

* Enum [OfficeMathJustification](../../officemathjustification/)
* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words for C++](../../../)
