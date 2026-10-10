---
title: "Aspose::Words::NodeType Enum"
linktitle: "NodeType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::NodeType‑Enum. Gibt den Typ eines Word‑Dokumentknotens in C++ an."
type: docs
weight: 102000
url: /de/cpp/aspose.words/nodetype/
---
## NodeType enum


Gibt den Typ eines Word-Dokumentknotens an.

```cpp
enum class NodeType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Alle | 0 | Gibt alle Knotentypen an. Ermöglicht die Auswahl aller untergeordneten Elemente. |
| Document | 1 | Ein [Document](../document/)-Objekt, das als Wurzel des Dokumentbaums Zugriff auf das gesamte Word‑Dokument bietet. Ein [Document](../document/)-Knoten kann [Section](../section/)-Knoten enthalten. |
| Section | 2 | Ein [Section](../section/)-Objekt, das einem Abschnitt in einem Word‑Dokument entspricht. Ein [Section](../section/)-Knoten kann [Body](../body/)- und [HeaderFooter](../headerfooter/)-Knoten enthalten. |
| Body | 3 | Ein [Body](../body/)-Objekt, das den Haupttext eines Abschnitts (Haupttext‑Story) enthält. Ein [Body](../body/)-Knoten kann [Paragraph](../paragraph/)- und [Table](../../aspose.words.tables/table/)-Knoten enthalten. |
| HeaderFooter | 4 | Ein [HeaderFooter](../headerfooter/)-Objekt, das den Text einer bestimmten Kopf‑ oder Fußzeile innerhalb eines Abschnitts enthält. Ein [HeaderFooter](../headerfooter/)-Knoten kann [Paragraph](../paragraph/)- und [Table](../../aspose.words.tables/table/)-Knoten enthalten. |
| Table | 5 | Ein [Table](../../aspose.words.tables/table/)-Objekt, das eine Tabelle in einem Word‑Dokument darstellt. Ein [Table](../../aspose.words.tables/table/)-Knoten kann [Row](../../aspose.words.tables/row/)-Knoten enthalten. |
| Row | 6 | Eine Zeile einer Tabelle. Ein [Row](../../aspose.words.tables/row/)-Knoten kann [Cell](../../aspose.words.tables/cell/)-Knoten enthalten. |
| Cell | 7 | Eine Zelle einer Tabellenzeile. Ein [Cell](../../aspose.words.tables/cell/)-Knoten kann [Paragraph](../paragraph/)- und [Table](../../aspose.words.tables/table/)-Knoten enthalten. |
| Paragraph | 8 | Ein Absatz von Text. Ein [Paragraph](../paragraph/)-Knoten ist ein Container für Inline‑Elemente [Run](../run/), [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/), [FormField](../../aspose.words.fields/formfield/), [Shape](../../aspose.words.drawing/shape/), [GroupShape](../../aspose.words.drawing/groupshape/), [Footnote](../../aspose.words.notes/footnote/), [Comment](../comment/), [SpecialChar](../specialchar/), sowie [BookmarkStart](../bookmarkstart/) und [BookmarkEnd](../bookmarkend/). |
| BookmarkStart | 9 | Der Beginn einer Lesezeichen‑Markierung. |
| BookmarkEnd | 10 | Das Ende einer Lesezeichen‑Markierung. |
| EditableRangeStart | 11 | Der Beginn eines bearbeitbaren Bereichs. |
| EditableRangeEnd | 12 | Das Ende eines bearbeitbaren Bereichs. |
| MoveFromRangeStart | 13 | Der Beginn eines MoveFrom‑Bereichs. |
| MoveFromRangeEnd | 14 | Ein Ende eines MoveFrom-Bereichs. |
| MoveToRangeStart | 15 | Ein Anfang eines MoveTo-Bereichs. |
| MoveToRangeEnd | 16 | Ein Ende eines MoveTo-Bereichs. |
| GroupShape | 17 | Eine Gruppe von Formen, Bildern, OLE-Objekten oder anderen Gruppierungsformen. Ein [GroupShape](../../aspose.words.drawing/groupshape/) Knoten kann andere [Shape](../../aspose.words.drawing/shape/) und [GroupShape](../../aspose.words.drawing/groupshape/) Knoten enthalten. |
| Shape | 18 | Ein Zeichenobjekt, wie z. B. eine OfficeArt-Form, ein Bild oder ein OLE-Objekt. Ein [Shape](../../aspose.words.drawing/shape/) Knoten kann [Paragraph](../paragraph/) und [Table](../../aspose.words.tables/table/) Knoten enthalten. |
| Comment | 19 | Ein Kommentar in einem Word-Dokument. Ein [Comment](../comment/) Knoten kann [Paragraph](../paragraph/) und [Table](../../aspose.words.tables/table/) Knoten enthalten. |
| Footnote | 20 | Eine Fußnote oder Endnote in einem Word-Dokument. Ein [Footnote](../../aspose.words.notes/footnote/) Knoten kann [Paragraph](../paragraph/) und [Table](../../aspose.words.tables/table/) Knoten enthalten. |
| Lauf | 21 | Ein Textlauf. |
| FieldStart | 22 | Ein Sonderzeichen, das den Beginn eines Word-Feldes bezeichnet. |
| FieldSeparator | 23 | Ein Sonderzeichen, das den Feldcode vom Feldergebnis trennt. |
| FieldEnd | 24 | Ein Sonderzeichen, das das Ende eines Word-Feldes bezeichnet. |
| FormField | 25 | Ein Formularfeld. |
| SpecialChar | 26 | Ein Sonderzeichen, das nicht zu den spezifischeren Sonderzeichenarten gehört. |
| SmartTag | 27 | Ein Smart-Tag um eine oder mehrere Inline-Strukturen (Läufe, Bilder, Felder usw.) innerhalb eines Absatzes. |
| StructuredDocumentTag | 28 | Ermöglicht die Definition kundenspezifischer Informationen und deren Darstellung. |
| StructuredDocumentTagRangeStart | 29 | Ein Beginn eines **ranged** strukturierten Dokumenten-Tags, das Inhalte mit mehreren Abschnitten akzeptiert. |
| StructuredDocumentTagRangeEnd | 30 | Ein Ende eines **ranged** strukturierten Dokumenten-Tags, das Inhalte mit mehreren Abschnitten akzeptiert. |
| GlossaryDocument | 31 | Ein Glossar-Dokument innerhalb des Hauptdokuments. |
| BuildingBlock | 32 | Ein Baustein innerhalb eines Glossar-Dokuments (z. B. Glossar-Dokumenteintrag). |
| CommentRangeStart | 33 | Ein Markierungsknoten, der den Beginn eines kommentierten Bereichs darstellt. |
| CommentRangeEnd | 34 | Ein Markierungsknoten, der das Ende eines kommentierten Bereichs darstellt. |
| OfficeMath | 35 | Ein Office-[Math](../../aspose.words.math/)-Objekt. Kann eine Gleichung, Funktion, Matrix oder eines der anderen mathematischen Objekte sein. Kann eine Sammlung mathematischer Objekte sein und auch nicht‑mathematische Objekte wie Textläufe enthalten. |
| SubDocument | 36 | Ein Unterdokument-Knoten, der ein Link zu einem anderen Dokument ist. |
| System | 37 | Für die interne Verwendung durch [Aspose.Words](../) reserviert. |
| Null | 38 | Für die interne Verwendung durch [Aspose.Words](../) reserviert. |


## Beispiele



Zeigt, wie man durch die Sammlung von Kindknoten eines Composite-Knotens traversiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Füge zwei Runs und eine Form als Kindknoten zum ersten Absatz dieses Dokuments hinzu.
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world! "));

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
// Beachten Sie, dass die 'CustomNodeId' nicht in einer Ausgabedatei gespeichert wird und nur während der Lebensdauer des Knotens existiert.
shape->set_CustomNodeId(100);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello again!"));

// Iterieren Sie durch die Sammlung unmittelbarer Kinder des Absatzes,
// und geben Sie alle Runs oder Shapes aus, die wir darin finden.
System::SharedPtr<Aspose::Words::NodeCollection> children = paragraph->GetChildNodes(Aspose::Words::NodeType::Any, false);

ASSERT_EQ(3, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count());

for (auto&& child : System::IterateOver(children))
{
    switch (child->get_NodeType())
    {
        case Aspose::Words::NodeType::Run:
            std::cout << "Run contents:" << std::endl;
            std::cout << System::String::Format(u"\t\"{0}\"", child->GetText().Trim()) << std::endl;
            break;

        case Aspose::Words::NodeType::Shape:
        {
            auto childShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(child);
            std::cout << "Shape:" << std::endl;
            std::cout << System::String::Format(u"\t{0}, {1}x{2}", childShape->get_ShapeType(), childShape->get_Width(), childShape->get_Height()) << std::endl;
            ASSERT_EQ(100, shape->get_CustomNodeId());
            break;
        }

        default:
            break;
    }
}
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
