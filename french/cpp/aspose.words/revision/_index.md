---
title: "classe Aspose::Words::Revision"
linktitle: "Révision"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "classe Aspose::Words::Revision. Représente une révision (modification suivie) dans un nœud ou un style de document. Utilisez RevisionType pour vérifier le type de cette révision. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 52000
url: /fr/cpp/aspose.words/revision/
---
## Revision class


Représente une révision (modification suivie) dans un nœud ou un style de document. Utilisez [RevisionType](./get_revisiontype/) pour vérifier le type de cette révision. Pour en savoir plus, consultez l'article de documentation [Track Changes in a Document](https://docs.aspose.com/words/cpp/track-changes-in-a-document/).

```cpp
class Revision : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Accept](./accept/)() | Accepte cette révision. |
| [get_Author](./get_author/)() | Obtient ou définit l'auteur de cette révision. Ne peut pas être une chaîne vide ou **null**. |
| [get_DateTime](./get_datetime/)() | Obtient ou définit la date/heure de cette révision. |
| [get_Group](./get_group/)() | Obtient le groupe de révision. Retourne **null** si la révision n'appartient à aucun groupe. |
| [get_ParentNode](./get_parentnode/)() | Obtient le nœud parent immédiat (propriétaire) de cette révision. Cette propriété fonctionnera pour tout type de révision autre que [StyleDefinitionChange](../revisiontype/). |
| [get_ParentStyle](./get_parentstyle/)() | Obtient le style parent immédiat (propriétaire) de cette révision. Cette propriété ne fonctionnera que pour le type de révision [StyleDefinitionChange](../revisiontype/). |
| [get_RevisionType](./get_revisiontype/)() const | Obtient le type de cette révision. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Reject](./reject/)() | Rejeter cette révision. |
| [set_Author](./set_author/)(const System::String\&) | Mutateur pour [Aspose::Words::Revision::get_Author](./get_author/). |
| [set_DateTime](./set_datetime/)(System::DateTime) | Mutateur pour [Aspose::Words::Revision::get_DateTime](./get_datetime/). |
| static [Type](./type/)() |  |

## Exemples



Montre comment travailler avec les révisions dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// La modification normale du document ne compte pas comme une révision.
builder->Write(u"This does not count as a revision. ");

ASSERT_FALSE(doc->get_HasRevisions());

// Pour enregistrer nos modifications en tant que révisions, nous devons déclarer un auteur, puis commencer à les suivre.
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());

builder->Write(u"This is revision #1. ");

ASSERT_TRUE(doc->get_HasRevisions());
ASSERT_EQ(1, doc->get_Revisions()->get_Count());

// Ce drapeau correspond à l'option "Review" -> "Tracking" -> "Track Changes" dans Microsoft Word.
// La méthode "StartTrackRevisions" n'affecte pas sa valeur,
// et le document suit les révisions de manière programmatique malgré une valeur de "false".
// Si nous ouvrons ce document avec Microsoft Word, il ne suivra pas les révisions.
ASSERT_FALSE(doc->get_TrackRevisions());

// Nous avons ajouté du texte à l'aide du constructeur de document, ainsi la première révision est une révision de type insertion.
System::SharedPtr<Aspose::Words::Revision> revision = doc->get_Revisions()->idx_get(0);
ASSERT_EQ(u"John Doe", revision->get_Author());
ASSERT_EQ(u"This is revision #1. ", revision->get_ParentNode()->GetText());
ASSERT_EQ(Aspose::Words::RevisionType::Insertion, revision->get_RevisionType());
ASSERT_EQ(revision->get_DateTime().get_Date(), System::DateTime::get_Now().get_Date());
ASPOSE_ASSERT_EQ(doc->get_Revisions()->get_Groups()->idx_get(0), revision->get_Group());

// Supprimez un run pour créer une révision de type suppression.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->Remove();

// L'ajout d'une nouvelle révision la place au début de la collection de révisions.
ASSERT_EQ(Aspose::Words::RevisionType::Deletion, doc->get_Revisions()->idx_get(0)->get_RevisionType());
ASSERT_EQ(2, doc->get_Revisions()->get_Count());

// Les révisions d'insertion apparaissent dans le corps du document même avant que nous acceptions/rejetions la révision.
// Rejeter la révision supprimera ses nœuds du corps. Inversement, les nœuds qui composent les révisions de suppression
// persistent également dans le document jusqu'à ce que nous acceptions la révision.
ASSERT_EQ(u"This does not count as a revision. This is revision #1.", doc->GetText().Trim());

// Accepter la révision de suppression supprimera son nœud parent du texte du paragraphe
// et supprimera ensuite la révision elle‑même de la collection.
doc->get_Revisions()->idx_get(0)->Accept();

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"This is revision #1.", doc->GetText().Trim());

builder->Writeln(u"");
builder->Write(u"This is revision #2.");

// Déplacez maintenant le nœud pour créer un type de révision de déplacement.
System::SharedPtr<Aspose::Words::Node> node = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1);
System::SharedPtr<Aspose::Words::Node> endNode = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_NextSibling();
System::SharedPtr<Aspose::Words::Node> referenceNode = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0);

while (node != endNode)
{
    System::SharedPtr<Aspose::Words::Node> nextNode = node->get_NextSibling();
    doc->get_FirstSection()->get_Body()->InsertBefore<System::SharedPtr<Aspose::Words::Node>>(node, referenceNode);
    node = nextNode;
}

ASSERT_EQ(Aspose::Words::RevisionType::Moving, doc->get_Revisions()->idx_get(0)->get_RevisionType());
ASSERT_EQ(8, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"This is revision #2.\rThis is revision #1. \rThis is revision #2.", doc->GetText().Trim());

// La révision de déplacement est maintenant à l'index 1. Rejetez la révision pour supprimer son contenu.
doc->get_Revisions()->idx_get(1)->Reject();

ASSERT_EQ(6, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"This is revision #1. \rThis is revision #2.", doc->GetText().Trim());
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
