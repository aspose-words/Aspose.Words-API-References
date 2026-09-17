---
title: "Méthode Aspose::Words::Range::UnlinkFields"
linktitle: "UnlinkFields"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Range::UnlinkFields. Dissocie les champs dans cette plage en C++."
type: docs
weight: 14000
url: /fr/cpp/aspose.words/range/unlinkfields/
---
## Range::UnlinkFields method


Délie les champs dans cette plage.

```cpp
void Aspose::Words::Range::UnlinkFields()
```

## Remarques


Remplace tous les champs de cette plage par leurs résultats les plus récents.

Pour dissocier les champs dans tout le document, utilisez [UnlinkFields](./).

## Exemples



Montre comment dissocier tous les champs dans une plage.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Linked fields.docx");

auto newSection = System::ExplicitCast<Aspose::Words::Section>(System::ExplicitCast<Aspose::Words::Node>(doc->get_Sections()->idx_get(0))->Clone(true));
doc->get_Sections()->Add(newSection);

doc->get_Sections()->idx_get(1)->get_Range()->UnlinkFields();
```

## Voir aussi

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
