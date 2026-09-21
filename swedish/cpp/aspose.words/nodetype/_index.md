---
title: "Aspose::Words::NodeType enum"
linktitle: "NodeType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::NodeType enum. Anger typen av en Word-dokumentnod i C++."
type: docs
weight: 102000
url: /sv/cpp/aspose.words/nodetype/
---
## NodeType enum


Anger typen av en Word-dokumentnod.

```cpp
enum class NodeType
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Any | 0 | Indikerar alla nodtyper. Tillåter att välja alla barn. |
| Document | 1 | Ett [Document](../document/)‑objekt som, som roten i dokumentträdet, ger åtkomst till hela Word‑dokumentet. En [Document](../document/)‑nod kan ha [Section](../section/)‑noder. |
| Section | 2 | Ett [Section](../section/)‑objekt som motsvarar ett avsnitt i ett Word‑dokument. En [Section](../section/)‑nod kan ha [Body](../body/)‑ och [HeaderFooter](../headerfooter/)‑noder. |
| Body | 3 | Ett [Body](../body/)‑objekt som innehåller huvudtexten i ett avsnitt (huvudtextberättelse). En [Body](../body/)‑nod kan ha [Paragraph](../paragraph/)‑ och [Table](../../aspose.words.tables/table/)‑noder. |
| HeaderFooter | 4 | Ett [HeaderFooter](../headerfooter/)‑objekt som innehåller texten för ett specifikt sidhuvud eller sidfot i ett avsnitt. En [HeaderFooter](../headerfooter/)‑nod kan ha [Paragraph](../paragraph/)‑ och [Table](../../aspose.words.tables/table/)‑noder. |
| Table | 5 | Ett [Table](../../aspose.words.tables/table/)‑objekt som representerar en tabell i ett Word‑dokument. En [Table](../../aspose.words.tables/table/)‑nod kan ha [Row](../../aspose.words.tables/row/)‑noder. |
| Row | 6 | En rad i en tabell. En [Row](../../aspose.words.tables/row/)‑nod kan ha [Cell](../../aspose.words.tables/cell/)‑noder. |
| Cell | 7 | En cell i en tabellrad. En [Cell](../../aspose.words.tables/cell/)‑nod kan ha [Paragraph](../paragraph/)‑ och [Table](../../aspose.words.tables/table/)‑noder. |
| Paragraph | 8 | Ett textstycke. En [Paragraph](../paragraph/)‑nod är en behållare för inline‑elementen [Run](../run/), [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/), [FormField](../../aspose.words.fields/formfield/), [Shape](../../aspose.words.drawing/shape/), [GroupShape](../../aspose.words.drawing/groupshape/), [Footnote](../../aspose.words.notes/footnote/), [Comment](../comment/), [SpecialChar](../specialchar/), samt [BookmarkStart](../bookmarkstart/) och [BookmarkEnd](../bookmarkend/). |
| BookmarkStart | 9 | En början på en bokmärkesmarkör. |
| BookmarkEnd | 10 | Ett slut på en bokmärkesmarkör. |
| EditableRangeStart | 11 | En början på ett redigerbart område. |
| EditableRangeEnd | 12 | Ett slut på ett redigerbart område. |
| MoveFromRangeStart | 13 | En början på ett MoveFrom‑område. |
| MoveFromRangeEnd | 14 | Ett slut på ett MoveFrom-intervall. |
| MoveToRangeStart | 15 | En början på ett MoveTo-intervall. |
| MoveToRangeEnd | 16 | Ett slut på ett MoveTo-intervall. |
| GroupShape | 17 | En grupp av former, bilder, OLE-objekt eller andra gruppformer. En [GroupShape](../../aspose.words.drawing/groupshape/) nod kan innehålla andra [Shape](../../aspose.words.drawing/shape/) och [GroupShape](../../aspose.words.drawing/groupshape/) noder. |
| Shape | 18 | Ett ritobjekt, till exempel en OfficeArt-form, bild eller ett OLE-objekt. En [Shape](../../aspose.words.drawing/shape/) nod kan innehålla [Paragraph](../paragraph/) och [Table](../../aspose.words.tables/table/) noder. |
| Comment | 19 | En kommentar i ett Word-dokument. En [Comment](../comment/) nod kan ha [Paragraph](../paragraph/) och [Table](../../aspose.words.tables/table/) noder. |
| Footnote | 20 | En fotnot eller slutnot i ett Word-dokument. En [Footnote](../../aspose.words.notes/footnote/) nod kan ha [Paragraph](../paragraph/) och [Table](../../aspose.words.tables/table/) noder. |
| Run | 21 | En textsekvens. |
| FieldStart | 22 | Ett specialtecken som betecknar början på ett Word-fält. |
| FieldSeparator | 23 | Ett specialtecken som separerar fältkoden från fältresultatet. |
| FieldEnd | 24 | Ett specialtecken som betecknar slutet på ett Word-fält. |
| FormField | 25 | Ett formulärfält. |
| SpecialChar | 26 | Ett specialtecken som inte är någon av de mer specifika specialteckentyperna. |
| SmartTag | 27 | En smart tagg runt en eller flera inline-strukturer (sekvenser, bilder, fält, osv.) inom ett stycke. |
| StructuredDocumentTag | 28 | Tillåter att definiera kundspecifik information och dess presentationssätt. |
| StructuredDocumentTagRangeStart | 29 | En början på **ranged** strukturerad dokumenttagg som accepterar innehåll med flera sektioner. |
| StructuredDocumentTagRangeEnd | 30 | Ett slut på **ranged** strukturerad dokumenttagg som accepterar innehåll med flera sektioner. |
| GlossaryDocument | 31 | Ett glossariedokument i huvuddokumentet. |
| BuildingBlock | 32 | En byggsten inom ett glossariedokument (t.ex. glossariedokumentpost). |
| CommentRangeStart | 33 | En markörnod som representerar början av ett kommenterat område. |
| CommentRangeEnd | 34 | En markörnod som representerar slutet av ett kommenterat område. |
| OfficeMath | 35 | Ett Office [Math](../../aspose.words.math/)‑objekt. Kan vara en ekvation, funktion, matris eller ett av andra matematiska objekt. Kan vara en samling av matematiska objekt och kan också innehålla vissa icke‑matematiska objekt såsom textsekvenser. |
| SubDocument | 36 | En subdokumentnod som är en länk till ett annat dokument. |
| System | 37 | Reserverad för internt bruk av [Aspose.Words](../). |
| Null | 38 | Reserverad för internt bruk av [Aspose.Words](../). |


## Exempel



Visar hur man traverserar en sammansatt nods samling av barnnoder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Lägg till två run och en shape som barnnoder till det första stycket i detta dokument.
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world! "));

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
// Observera att 'CustomNodeId' inte sparas till en utdatafil och endast existerar under nodens livstid.
shape->set_CustomNodeId(100);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello again!"));

// Iterera genom styckets samling av omedelbara barn,
// och skriv ut eventuella run eller shapes som vi hittar där.
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

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
