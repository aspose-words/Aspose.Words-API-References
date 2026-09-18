---
title: "Aspose::Words::Layout::LayoutCollector class"
linktitle: "LayoutCollector"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Layout::LayoutCollector class. Diese Klasse ermöglicht die Berechnung von Seitenzahlen von Dokumentknoten. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 1000
url: /de/cpp/aspose.words.layout/layoutcollector/
---
## LayoutCollector class


Diese Klasse ermöglicht die Berechnung von Seitenzahlen von Dokumentknoten. Weitere Informationen finden Sie im Dokumentationsartikel [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/).

```cpp
class LayoutCollector : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Clear](./clear/)() | Löscht alle gesammelten Layoutdaten. Rufen Sie diese Methode auf, nachdem das Dokument manuell aktualisiert wurde oder das Layout neu erstellt wurde. |
| [get_Document](./get_document/)() const | Liefert oder setzt das Dokument, an das diese Sammlungsinstanz angehängt ist. |
| [GetEndPageIndex](./getendpageindex/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Liefert den einsbasierten Index der Seite, auf der der Knoten endet. Gibt 0 zurück, wenn der Knoten keiner Seite zugeordnet werden kann. |
| [GetEntity](./getentity/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gibt eine undurchsichtige Position des [LayoutEnumerator](../layoutenumerator/) zurück, die dem angegebenen Knoten entspricht. Sie können den zurückgegebenen Wert als Argument für [Current](../layoutenumerator/get_current/) verwenden, sofern das enumerierte Dokument und das Dokument des Knotens identisch sind. |
| [GetNumPagesSpanned](./getnumpagesspanned/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Liefert die Anzahl der Seiten, die der angegebene Knoten umfasst. 0, wenn der Knoten innerhalb einer einzelnen Seite liegt. Dies entspricht [GetEndPageIndex()](../) - [GetStartPageIndex()](../). |
| [GetStartPageIndex](./getstartpageindex/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Liefert den einsbasierten Index der Seite, auf der der Knoten beginnt. Gibt 0 zurück, wenn der Knoten keiner Seite zugeordnet werden kann. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LayoutCollector](./layoutcollector/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Initialisiert eine Instanz dieser Klasse. |
| [set_Document](./set_document/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Setter für [Aspose::Words::Layout::LayoutCollector::get_Document](./get_document/). |
| static [Type](./type/)() |  |
## Hinweise


Wenn Sie einen [LayoutCollector](./) erstellen und ein [Document](../../aspose.words/document/) Dokumentobjekt angeben, an das er angehängt werden soll, zeichnet der Collector die Zuordnung von Dokumentknoten zu Layoutobjekten auf, wenn das Dokument in Seiten formatiert wird.

Sie können herausfinden, auf welcher Seite ein bestimmter Dokumentknoten (z. B. Run, Absatz oder Tabellenzelle) sich befindet, indem Sie die Methoden [GetStartPageIndex()](../), [GetEndPageIndex()](../) und [GetNumPagesSpanned()](../) verwenden. Diese Methoden erstellen automatisch das Seitenlayout‑Modell des Dokuments und aktualisieren bei Bedarf die Felder.

Wenn Sie die Layout‑Informationen nicht mehr benötigen, sollten Sie die Eigenschaft [Document](./get_document/) auf **null** setzen, um die unnötige Sammlung weiterer Layout‑Zuordnungen zu vermeiden.

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

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
