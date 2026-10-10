---
title: "Aspose::Words::Layout::LayoutCollector classe"
linktitle: "LayoutCollector"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Layout::LayoutCollector classe. Cette classe permet de calculer les numéros de page des nœuds du document. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 1000
url: /fr/cpp/aspose.words.layout/layoutcollector/
---
## LayoutCollector class


Cette classe permet de calculer les numéros de page des nœuds du document. Pour en savoir plus, consultez l'article de documentation [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/).

```cpp
class LayoutCollector : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Clear](./clear/)() | Efface toutes les données de mise en page collectées. Appelez cette méthode après que le document a été mis à jour manuellement, ou que la mise en page a été reconstruite. |
| [get_Document](./get_document/)() const | Obtient ou définit le document auquel cette instance du collecteur est attachée. |
| [GetEndPageIndex](./getendpageindex/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtient l'index basé sur 1 de la page où le nœud se termine. Retourne 0 si le nœud ne peut pas être mappé à une page. |
| [GetEntity](./getentity/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Retourne une position opaque du [LayoutEnumerator](../layoutenumerator/) qui correspond au nœud spécifié. Vous pouvez utiliser la valeur retournée comme argument pour [Current](../layoutenumerator/get_current/) étant donné que le document en cours d'énumération et le document du nœud sont les mêmes. |
| [GetNumPagesSpanned](./getnumpagesspanned/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtient le nombre de pages que le nœud spécifié occupe. 0 si le nœud se trouve sur une seule page. C'est équivalent à [GetEndPageIndex()](../) - [GetStartPageIndex()](../). |
| [GetStartPageIndex](./getstartpageindex/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtient l'index basé sur 1 de la page où le nœud commence. Retourne 0 si le nœud ne peut pas être mappé à une page. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LayoutCollector](./layoutcollector/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Initialise une instance de cette classe. |
| [set_Document](./set_document/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Mutateur pour [Aspose::Words::Layout::LayoutCollector::get_Document](./get_document/). |
| static [Type](./type/)() |  |
## Remarques


Lorsque vous créez un [LayoutCollector](./) et spécifiez un objet [Document](../../aspose.words/document/) à attacher, le collecteur enregistrera le mappage des nœuds du document vers les objets de mise en page lorsque le document est formaté en pages.

Vous pourrez déterminer sur quelle page se trouve un nœud de document particulier (p. ex. run, paragraphe ou cellule de tableau) en utilisant les méthodes [GetStartPageIndex()](../), [GetEndPageIndex()](../) et [GetNumPagesSpanned()](../). Ces méthodes construisent automatiquement le modèle de mise en page du document et mettent à jour les champs si nécessaire.

Lorsque vous n'avez plus besoin de collecter des informations de mise en page, il est préférable de définir la propriété [Document](./get_document/) sur **null** afin d'éviter la collecte inutile de davantage de mappages de mise en page.

## Exemples



Montre comment voir les intervalles de pages qu'un nœud occupe.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto layoutCollector = System::MakeObject<Aspose::Words::Layout::LayoutCollector>(doc);

// Appelez la méthode "GetNumPagesSpanned" pour compter le nombre de pages que le contenu de notre document occupe.
// Comme le document est vide, ce nombre de pages est actuellement zéro.
ASPOSE_ASSERT_EQ(doc, layoutCollector->get_Document());
ASSERT_EQ(0, layoutCollector->GetNumPagesSpanned(doc));

// Remplissez le document avec 5 pages de contenu.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);
builder->Write(u"Section 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Avant le collecteur de mise en page, nous devons appeler la méthode "UpdatePageLayout" pour nous fournir
// une mesure précise pour toute métrique liée à la mise en page, comme le nombre de pages.
ASSERT_EQ(0, layoutCollector->GetNumPagesSpanned(doc));

layoutCollector->Clear();
doc->UpdatePageLayout();

ASSERT_EQ(5, layoutCollector->GetNumPagesSpanned(doc));

// Nous pouvons voir les numéros des pages de début et de fin de n'importe quel nœud ainsi que leurs étendues de pages globales.
System::SharedPtr<Aspose::Words::NodeCollection> nodes = doc->GetChildNodes(Aspose::Words::NodeType::Any, true);
for (auto&& node : System::IterateOver(nodes))
{
    std::cout << System::String::Format(u"->  NodeType.{0}: ", node->get_NodeType()) << std::endl;
    std::cout << (System::String::Format(u"\tStarts on page {0}, ends on page {1},", layoutCollector->GetStartPageIndex(node), layoutCollector->GetEndPageIndex(node)) + System::String::Format(u" spanning {0} pages.", layoutCollector->GetNumPagesSpanned(node))) << std::endl;
}

// Nous pouvons itérer sur les entités de mise en page en utilisant un LayoutEnumerator.
auto layoutEnumerator = System::MakeObject<Aspose::Words::Layout::LayoutEnumerator>(doc);

ASSERT_EQ(Aspose::Words::Layout::LayoutEntityType::Page, layoutEnumerator->get_Type());

// Le LayoutEnumerator peut parcourir la collection d'entités de mise en page comme un arbre.
// Nous pouvons également l'appliquer à l'entité de mise en page correspondante de n'importe quel nœud.
layoutEnumerator->set_Current(layoutCollector->GetEntity(doc->GetChild(Aspose::Words::NodeType::Paragraph, 1, true)));

ASSERT_EQ(Aspose::Words::Layout::LayoutEntityType::Span, layoutEnumerator->get_Type());
ASSERT_EQ(u"¶", layoutEnumerator->get_Text());
```

## Voir aussi

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
