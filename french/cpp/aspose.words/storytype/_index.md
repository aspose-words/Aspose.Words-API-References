---
title: "Aspose::Words::StoryType enum"
linktitle: "StoryType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::StoryType enum. Le texte d'un document Word est stocké dans des histoires. StoryType identifie une histoire en C++."
type: docs
weight: 117000
url: /fr/cpp/aspose.words/storytype/
---
## StoryType enum


Le texte d'un document Word est stocké dans des histoires. [StoryType](./) identifie une histoire.

```cpp
enum class StoryType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| None | 0 | Valeur par défaut. Il n'existe aucune histoire de ce type dans le document. |
| MainText | 1 | Contient le texte principal du document, représenté par [Body](../body/). |
| Footnotes | 2 | Contient le texte de la note de bas de page, représenté par [Footnote](../../aspose.words.notes/footnote/). |
| Endnotes | 3 | Contient le texte des notes de fin, représenté par [Footnote](../../aspose.words.notes/footnote/). |
| Comments | 4 | Contient les commentaires du document (annotations), représentés par [Comment](../comment/). |
| Textbox | 5 | Contient le texte de la forme ou de la zone de texte, représenté par [Shape](../../aspose.words.drawing/shape/). |
| EvenPagesHeader | 6 | Contient le texte de l'en-tête des pages paires, représenté par [HeaderFooter](../headerfooter/). |
| PrimaryHeader | 7 | Contient le texte de l'en-tête principal. Lorsque l'en-tête diffère pour les pages impaires et paires, il contient le texte de l'en-tête des pages impaires. Représenté par [HeaderFooter](../headerfooter/). |
| EvenPagesFooter | 8 | Contient le texte du pied de page des pages paires, représenté par [HeaderFooter](../headerfooter/). |
| PrimaryFooter | 9 | Contient le texte du pied de page principal. Lorsque le pied de page diffère pour les pages impaires et paires, il contient le texte du pied de page des pages impaires. Représenté par [HeaderFooter](../headerfooter/). |
| FirstPageHeader | 10 | Contient le texte de l'en-tête de la première page, représenté par [HeaderFooter](../headerfooter/). |
| FirstPageFooter | 11 | Contient le texte du pied de page de la première page, représenté par [HeaderFooter](../headerfooter/). |
| FootnoteSeparator | 12 | Contient le texte du séparateur de note de bas de page. |
| FootnoteContinuationSeparator | 13 | Contient le texte du séparateur de continuation de note de bas de page. |
| FootnoteContinuationNotice | 14 | Contient le texte du séparateur d'avis de continuation de note de bas de page. |
| EndnoteSeparator | 15 | Contient le texte du séparateur de note de fin. |
| EndnoteContinuationSeparator | 16 | Contient le texte du séparateur de continuation de note de fin. |
| EndnoteContinuationNotice | 17 | Contient le texte du séparateur d'avis de continuation de note de fin. |


## Exemples



Montre comment supprimer toutes les formes d'un nœud.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Utilisez un DocumentBuilder pour insérer une forme. Il s'agit d'une forme en ligne,
// qui a un paragraphe parent, qui est un nœud enfant du Body de la première section.
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 100.0, 100.0);

ASSERT_EQ(1, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());

// Nous pouvons supprimer toutes les formes des paragraphes enfants de ce Corps.
ASSERT_EQ(Aspose::Words::StoryType::MainText, doc->get_FirstSection()->get_Body()->get_StoryType());
doc->get_FirstSection()->get_Body()->DeleteShapes();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
