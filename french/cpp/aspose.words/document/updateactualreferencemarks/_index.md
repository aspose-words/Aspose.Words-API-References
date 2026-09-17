---
title: "Aspose::Words::Document::UpdateActualReferenceMarks méthode"
linktitle: "UpdateActualReferenceMarks"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::UpdateActualReferenceMarks méthode. Met à jour la propriété ActualReferenceMark de toutes les notes de bas de page et notes de fin dans le document en C++."
type: docs
weight: 95500
url: /fr/cpp/aspose.words/document/updateactualreferencemarks/
---
## Document::UpdateActualReferenceMarks method


Met à jour la propriété [ActualReferenceMark](../../../aspose.words.notes/footnote/get_actualreferencemark/) de toutes les notes de bas de page et notes de fin dans le document.

```cpp
void Aspose::Words::Document::UpdateActualReferenceMarks()
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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
