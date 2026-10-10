---
title: "Méthode Aspose::Words::Paragraph::get_IsMoveFromRevision"
linktitle: "get_IsMoveFromRevision"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Paragraph::get_IsMoveFromRevision. Retourne true si cet objet a été déplacé (supprimé) dans Microsoft Word alors que le suivi des modifications était activé en C++."
type: docs
weight: 16000
url: /fr/cpp/aspose.words/paragraph/get_ismovefromrevision/
---
## Paragraph::get_IsMoveFromRevision method


Renvoie **true** si cet objet a été déplacé (supprimé) dans Microsoft Word alors que le suivi des modifications était activé.

```cpp
bool Aspose::Words::Paragraph::get_IsMoveFromRevision()
```


## Exemples



Montre comment vérifier si un paragraphe est une révision de déplacement.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

// Ce document contient des révisions \"Move\", qui apparaissent lorsque nous sélectionnons du texte avec le curseur,
// et que nous le faisons glisser pour le déplacer vers un autre emplacement
// tout en suivant les révisions dans Microsoft Word via \"Review\" -> \"Track changes\".
ASSERT_EQ(6, doc->get_Revisions()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Revision>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Revision> r)>>([](System::SharedPtr<Aspose::Words::Revision> r) -> bool
{
    return r->get_RevisionType() == Aspose::Words::RevisionType::Moving;
}))));

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

// Les révisions de déplacement sont constituées de paires de révisions \"Move from\" et \"Move to\".
// Ces révisions sont des modifications potentielles du document que nous pouvons soit accepter, soit rejeter.
// Avant d'accepter/rejeter une révision de déplacement, le document
// doit garder une trace à la fois des destinations de départ et d'arrivée du texte.
// Le deuxième et le quatrième paragraphe définissent une telle révision, et donc les deux ont le même contenu.
ASSERT_EQ(paragraphs->idx_get(1)->GetText(), paragraphs->idx_get(3)->GetText());

// La révision \"Move from\" est le paragraphe d'où nous avons fait glisser le texte.
// Si nous acceptons la révision, ce paragraphe disparaîtra,
// et l'autre restera et ne sera plus une révision.
ASSERT_TRUE(paragraphs->idx_get(1)->get_IsMoveFromRevision());

// La révision \"Move to\" est le paragraphe vers lequel nous avons fait glisser le texte.
// Si nous rejetons la révision, ce paragraphe disparaîtra à la place, et l'autre restera.
ASSERT_TRUE(paragraphs->idx_get(3)->get_IsMoveToRevision());
```

## Voir aussi

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
