---
title: "Aspose::Words::RevisionsView enum"
linktitle: "RevisionsView"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::RevisionsView enum. Permet de spécifier s'il faut travailler avec la version originale ou révisée d'un document en C++."
type: docs
weight: 112000
url: /fr/cpp/aspose.words/revisionsview/
---
## RevisionsView enum


Permet de spécifier s'il faut travailler avec la version originale ou révisée d'un document.

```cpp
enum class RevisionsView
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Original | 0 | Spécifie la version originale d'un document. |
| Final | 1 | Spécifie la version révisée d'un document. |


## Exemples



Montre comment basculer entre la vue révisée et la vue originale d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions at list levels.docx");
doc->UpdateListLabels();

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();
ASSERT_EQ(u"1.", paragraphs->idx_get(0)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"a.", paragraphs->idx_get(1)->get_ListLabel()->get_LabelString());
ASSERT_EQ(System::String::Empty, paragraphs->idx_get(2)->get_ListLabel()->get_LabelString());

// Affiche l'objet document comme si toutes les révisions étaient acceptées. Prend actuellement en charge les libellés de liste.
doc->set_RevisionsView(Aspose::Words::RevisionsView::Final);

ASSERT_EQ(System::String::Empty, paragraphs->idx_get(0)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"1.", paragraphs->idx_get(1)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"a.", paragraphs->idx_get(2)->get_ListLabel()->get_LabelString());
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
