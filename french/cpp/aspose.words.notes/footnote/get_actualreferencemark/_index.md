---
title: "Aspose::Words::Notes::Footnote::get_ActualReferenceMark méthode"
linktitle: "get_ActualReferenceMark"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Notes::Footnote::get_ActualReferenceMark méthode. Obtient le texte réel du marqueur de référence affiché dans le document pour cette note de bas de page en C++."
type: docs
weight: 3834
url: /fr/cpp/aspose.words.notes/footnote/get_actualreferencemark/
---
## Footnote::get_ActualReferenceMark method


Obtient le texte réel du repère affiché dans le document pour cette note de bas de page.

```cpp
System::String Aspose::Words::Notes::Footnote::get_ActualReferenceMark()
```


## Exemples



Montre comment obtenir le véritable marqueur de référence de la note de bas de page.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

auto footnote = System::ExplicitCast<Aspose::Words::Notes::Footnote>(doc->GetChild(Aspose::Words::NodeType::Footnote, 1, true));
doc->UpdateFields();
doc->UpdateActualReferenceMarks();

ASSERT_EQ(u"1", footnote->get_ActualReferenceMark());
```

## Voir aussi

* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
