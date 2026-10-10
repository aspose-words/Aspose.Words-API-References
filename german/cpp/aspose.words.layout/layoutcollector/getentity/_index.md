---
title: "Aspose::Words::Layout::LayoutCollector::GetEntity Methode"
linktitle: "GetEntity"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Layout::LayoutCollector::GetEntity Methode. Gibt eine undurchsichtige Position des LayoutEnumerators zurück, die dem angegebenen Knoten entspricht. Der zurückgegebene Wert kann als Argument für Current verwendet werden, sofern das enumerierte Dokument und das Dokument des Knotens identisch sind in C++."
type: docs
weight: 6000
url: /de/cpp/aspose.words.layout/layoutcollector/getentity/
---
## LayoutCollector::GetEntity method


Gibt eine undurchsichtige Position des [LayoutEnumerator](../../layoutenumerator/) zurück, die dem angegebenen Knoten entspricht. Der zurückgegebene Wert kann als Argument für [Current](../../layoutenumerator/get_current/) verwendet werden, sofern das enumerierte Dokument und das Dokument des Knotens identisch sind.

```cpp
System::SharedPtr<System::Object> Aspose::Words::Layout::LayoutCollector::GetEntity(const System::SharedPtr<Aspose::Words::Node> &node)
```

## Hinweise


Diese Methode funktioniert nur für [Paragraph](../../../aspose.words/paragraph/) Knoten sowie für unteilbare Inline‑Knoten, z. B. [BookmarkStart](../../../aspose.words/bookmarkstart/) oder [Shape](../../../aspose.words.drawing/shape/). Sie funktioniert nicht für [Run](../../../aspose.words/run/), [Cell](../../../aspose.words.tables/cell/)[Row](../../../aspose.words.tables/row/) oder [Table](../../../aspose.words.tables/table/) Knoten und für Knoten innerhalb von Kopf‑/Fußzeilen.

Beachten Sie, dass die für einen [Paragraph](../../../aspose.words/paragraph/) Knoten zurückgegebene Entität ein Absatzumbruch‑Span ist. Verwenden Sie die entsprechende Methode, um zur übergeordneten Zeile aufzusteigen.

Wenn Sie zu einem [Run](../../../aspose.words/run/) Text navigieren müssen, können Sie ein Lesezeichen direkt davor einfügen und stattdessen zu diesem Lesezeichen navigieren.

Wenn Sie zu einem [Cell](../../../aspose.words.tables/cell/) Knoten navigieren müssen, können Sie zu einem [Paragraph](../../../aspose.words/paragraph/) Knoten in dieser Zelle wechseln und dann zur übergeordneten Entität aufsteigen. Der gleiche Ansatz kann für [Row](../../../aspose.words.tables/row/) und [Table](../../../aspose.words.tables/table/) Knoten verwendet werden.

## Beispiele



Zeigt, wie man die Seitenbereiche sieht, die ein Knoten umfasst.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto layoutCollector = System::MakeObject<Aspose::Words::Layout::LayoutCollector>(doc);

// Rufen Sie die Methode \"GetNumPagesSpanned\" auf, um zu zählen, wie viele Seiten der Inhalt unseres Dokuments umfasst.
// Da das Dokument leer ist, beträgt die aktuelle Seitenzahl null.
ASPOSE_ASSERT_EQ(doc, layoutCollector->get_Document());
ASSERT_EQ(0, layoutCollector->GetNumPagesSpanned(doc));

// Füllen Sie das Dokument mit 5 Seiten Inhalt.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);
builder->Write(u"Section 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Vor dem Layout‑Collector müssen wir die Methode \"UpdatePageLayout\" aufrufen, um uns
// eine genaue Angabe für jede layoutbezogene Kennzahl, wie z. B. die Seitenzahl.
ASSERT_EQ(0, layoutCollector->GetNumPagesSpanned(doc));

layoutCollector->Clear();
doc->UpdatePageLayout();

ASSERT_EQ(5, layoutCollector->GetNumPagesSpanned(doc));

// Wir können die Nummern der Start‑ und Endseiten jedes Knotens sowie deren gesamte Seitenbereiche sehen.
System::SharedPtr<Aspose::Words::NodeCollection> nodes = doc->GetChildNodes(Aspose::Words::NodeType::Any, true);
for (auto&& node : System::IterateOver(nodes))
{
    std::cout << System::String::Format(u"->  NodeType.{0}: ", node->get_NodeType()) << std::endl;
    std::cout << (System::String::Format(u"\tStarts on page {0}, ends on page {1},", layoutCollector->GetStartPageIndex(node), layoutCollector->GetEndPageIndex(node)) + System::String::Format(u" spanning {0} pages.", layoutCollector->GetNumPagesSpanned(node))) << std::endl;
}

// Wir können über die Layout‑Entitäten mit einem LayoutEnumerator iterieren.
auto layoutEnumerator = System::MakeObject<Aspose::Words::Layout::LayoutEnumerator>(doc);

ASSERT_EQ(Aspose::Words::Layout::LayoutEntityType::Page, layoutEnumerator->get_Type());

// Der LayoutEnumerator kann die Sammlung von Layout‑Entitäten wie einen Baum durchlaufen.
// Wir können ihn auch auf die entsprechende Layout‑Entität eines beliebigen Knotens anwenden.
layoutEnumerator->set_Current(layoutCollector->GetEntity(doc->GetChild(Aspose::Words::NodeType::Paragraph, 1, true)));

ASSERT_EQ(Aspose::Words::Layout::LayoutEntityType::Span, layoutEnumerator->get_Type());
ASSERT_EQ(u"¶", layoutEnumerator->get_Text());
```

## Siehe auch

* Class [Node](../../../aspose.words/node/)
* Class [LayoutCollector](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
