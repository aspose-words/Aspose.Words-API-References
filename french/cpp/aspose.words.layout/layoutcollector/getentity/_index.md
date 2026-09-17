---
title: "Méthode Aspose::Words::Layout::LayoutCollector::GetEntity"
linktitle: "GetEntity"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Layout::LayoutCollector::GetEntity. Retourne une position opaque du LayoutEnumerator qui correspond au nœud spécifié. Vous pouvez utiliser la valeur retournée comme argument pour Current tant que le document en cours d'énumération et le document du nœud sont les mêmes en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.layout/layoutcollector/getentity/
---
## LayoutCollector::GetEntity method


Retourne une position opaque du [LayoutEnumerator](../../layoutenumerator/) qui correspond au nœud spécifié. Vous pouvez utiliser la valeur retournée comme argument pour [Current](../../layoutenumerator/get_current/) tant que le document en cours d'énumération et le document du nœud sont les mêmes.

```cpp
System::SharedPtr<System::Object> Aspose::Words::Layout::LayoutCollector::GetEntity(const System::SharedPtr<Aspose::Words::Node> &node)
```

## Remarques


Cette méthode fonctionne uniquement pour les nœuds [Paragraph](../../../aspose.words/paragraph/), ainsi que pour les nœuds en ligne indivisibles, par ex. [BookmarkStart](../../../aspose.words/bookmarkstart/) ou [Shape](../../../aspose.words.drawing/shape/). Elle ne fonctionne pas pour les nœuds [Run](../../../aspose.words/run/), [Cell](../../../aspose.words.tables/cell/)[Row](../../../aspose.words.tables/row/) ou [Table](../../../aspose.words.tables/table/), ni pour les nœuds situés dans l’en-tête/pied de page.

Notez que l'entité retournée pour un nœud [Paragraph](../../../aspose.words/paragraph/) est un segment de saut de paragraphe. Utilisez la méthode appropriée pour remonter à la ligne parent.

Si vous devez naviguer vers un [Run](../../../aspose.words/run/) de texte, vous pouvez insérer un signet juste avant et naviguer ensuite vers ce signet.

Si vous devez naviguer vers un nœud [Cell](../../../aspose.words.tables/cell/), vous pouvez vous déplacer vers un nœud [Paragraph](../../../aspose.words/paragraph/) dans cette cellule, puis remonter à l'entité parent. La même approche peut être utilisée pour les nœuds [Row](../../../aspose.words.tables/row/) et [Table](../../../aspose.words.tables/table/).

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

* Class [Node](../../../aspose.words/node/)
* Class [LayoutCollector](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
