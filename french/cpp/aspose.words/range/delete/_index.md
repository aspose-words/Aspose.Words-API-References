---
title: "Aspose::Words::Range::Delete méthode"
linktitle: "Supprimer"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Range::Delete méthode. Supprime tous les caractères de la plage en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words/range/delete/
---
## Range::Delete method


Supprime tous les caractères de la plage.

```cpp
void Aspose::Words::Range::Delete()
```


## Exemples



Montre comment supprimer tous les nœuds d'une plage.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ajoutez du texte à la première section du document, puis ajoutez une autre section.
builder->Write(u"Section 1. ");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakContinuous);
builder->Write(u"Section 2.");

ASSERT_EQ(u"Section 1. \fSection 2.", doc->GetText().Trim());

// Supprimez complètement la première section en supprimant tous les nœuds
// dans sa plage, y compris la section elle‑même.
doc->get_Sections()->idx_get(0)->get_Range()->Delete();

ASSERT_EQ(1, doc->get_Sections()->get_Count());
ASSERT_EQ(u"Section 2.", doc->GetText().Trim());
```

## Voir aussi

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
