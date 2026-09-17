---
title: "Aspose::Words::NodeCollection::RemoveAt méthode"
linktitle: "RemoveAt"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::NodeCollection::RemoveAt méthode. Supprime le nœud à l'index spécifié de la collection et du document en C++."
type: docs
weight: 13000
url: /fr/cpp/aspose.words/nodecollection/removeat/
---
## NodeCollection::RemoveAt method


Supprime le nœud à l'index spécifié de la collection et du document.

```cpp
void Aspose::Words::NodeCollection::RemoveAt(int32_t index)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| index | int32_t | L’index zéro‑basé du nœud. Les index négatifs sont autorisés et indiquent un accès depuis la fin de la liste. Par exemple, -1 signifie le dernier nœud, -2 le deuxième avant le dernier, etc. |

## Exemples



Montre comment ajouter et supprimer des sections dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");

ASSERT_EQ(u"Section 1\x000c" u"Section 2", doc->GetText().Trim());

// Supprimez la première section du document.
doc->get_Sections()->RemoveAt(0);

ASSERT_EQ(u"Section 2", doc->GetText().Trim());

// Ajoutez une copie de ce qui est maintenant la première section à la fin du document.
int32_t lastSectionIdx = doc->get_Sections()->get_Count() - 1;
System::SharedPtr<Aspose::Words::Section> newSection = doc->get_Sections()->idx_get(lastSectionIdx)->Clone();
doc->get_Sections()->Add(newSection);

ASSERT_EQ(u"Section 2\x000c" u"Section 2", doc->GetText().Trim());
```

## Voir aussi

* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
