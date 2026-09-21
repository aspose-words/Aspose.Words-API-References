---
title: "Aspose::Words::DocumentVisitor klass"
linktitle: "DocumentVisitor"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentVisitor klass. Basisklass för anpassade dokumentbesökare. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 23000
url: /sv/cpp/aspose.words/documentvisitor/
---
## DocumentVisitor class


Basklass för anpassade dokumentbesökare. För att läsa mer, besök artikeln [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) i dokumentationen.

```cpp
class DocumentVisitor : public virtual System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| virtual [VisitAbsolutePositionTab](./visitabsolutepositiontab/)(System::SharedPtr\<Aspose::Words::AbsolutePositionTab\>) | Kallas när en [AbsolutePositionTab](../absolutepositiontab/) nod påträffas i dokumentet. |
| virtual [VisitBodyEnd](./visitbodyend/)(System::SharedPtr\<Aspose::Words::Body\>) | Kallas när uppräkning av huvudtextberättelsen i ett avsnitt har avslutats. |
| virtual [VisitBodyStart](./visitbodystart/)(System::SharedPtr\<Aspose::Words::Body\>) | Kallas när uppräkning av huvudtextberättelsen i ett avsnitt har påbörjats. |
| virtual [VisitBookmarkEnd](./visitbookmarkend/)(System::SharedPtr\<Aspose::Words::BookmarkEnd\>) | Kallas när ett slut på ett bokmärke påträffas i dokumentet. |
| virtual [VisitBookmarkStart](./visitbookmarkstart/)(System::SharedPtr\<Aspose::Words::BookmarkStart\>) | Kallas när en start på ett bokmärke påträffas i dokumentet. |
| virtual [VisitBuildingBlockEnd](./visitbuildingblockend/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::BuildingBlock\>) | Kallas när uppräkning av ett byggblock har avslutats. |
| virtual [VisitBuildingBlockStart](./visitbuildingblockstart/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::BuildingBlock\>) | Kallas när uppräkning av ett byggblock har påbörjats. |
| virtual [VisitCellEnd](./visitcellend/)(System::SharedPtr\<Aspose::Words::Tables::Cell\>) | Kallas när uppräkning av en tabellcell har avslutats. |
| virtual [VisitCellStart](./visitcellstart/)(System::SharedPtr\<Aspose::Words::Tables::Cell\>) | Kallas när uppräkning av en tabellcell har påbörjats. |
| virtual [VisitCommentEnd](./visitcommentend/)(System::SharedPtr\<Aspose::Words::Comment\>) | Kallas när uppräkning av en kommentarstext har avslutats. |
| virtual [VisitCommentRangeEnd](./visitcommentrangeend/)(System::SharedPtr\<Aspose::Words::CommentRangeEnd\>) | Kallas när slutet på ett kommenterat textområde påträffas. |
| virtual [VisitCommentRangeStart](./visitcommentrangestart/)(System::SharedPtr\<Aspose::Words::CommentRangeStart\>) | Kallas när starten på ett kommenterat textområde påträffas. |
| virtual [VisitCommentStart](./visitcommentstart/)(System::SharedPtr\<Aspose::Words::Comment\>) | Kallas när uppräkning av en kommentarstext har påbörjats. |
| virtual [VisitDocumentEnd](./visitdocumentend/)(System::SharedPtr\<Aspose::Words::Document\>) | Kallas när uppräkning av dokumentet har avslutats. |
| virtual [VisitDocumentStart](./visitdocumentstart/)(System::SharedPtr\<Aspose::Words::Document\>) | Kallas när uppräkning av dokumentet har påbörjats. |
| virtual [VisitEditableRangeEnd](./visiteditablerangeend/)(System::SharedPtr\<Aspose::Words::EditableRangeEnd\>) | Kallas när ett slut på ett redigerbart område påträffas i dokumentet. |
| virtual [VisitEditableRangeStart](./visiteditablerangestart/)(System::SharedPtr\<Aspose::Words::EditableRangeStart\>) | Kallas när en början på ett redigerbart område påträffas i dokumentet. |
| virtual [VisitFieldEnd](./visitfieldend/)(System::SharedPtr\<Aspose::Words::Fields::FieldEnd\>) | Kallas när ett fält avslutas i dokumentet. |
| virtual [VisitFieldSeparator](./visitfieldseparator/)(System::SharedPtr\<Aspose::Words::Fields::FieldSeparator\>) | Kallas när en fältseparator påträffas i dokumentet. |
| virtual [VisitFieldStart](./visitfieldstart/)(System::SharedPtr\<Aspose::Words::Fields::FieldStart\>) | Kallas när ett fält startar i dokumentet. |
| virtual [VisitFootnoteEnd](./visitfootnoteend/)(System::SharedPtr\<Aspose::Words::Notes::Footnote\>) | Kallas när uppräkning av en fotnot- eller slutnotstext har avslutats. |
| virtual [VisitFootnoteStart](./visitfootnotestart/)(System::SharedPtr\<Aspose::Words::Notes::Footnote\>) | Kallas när uppräkning av en fotnot- eller slutnotstext har påbörjats. |
| virtual [VisitFormField](./visitformfield/)(System::SharedPtr\<Aspose::Words::Fields::FormField\>) | Kallas när ett formulärfält påträffas i dokumentet. |
| virtual [VisitGlossaryDocumentEnd](./visitglossarydocumentend/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>) | Kallas när uppräkning av ett glossaridokument har avslutats. |
| virtual [VisitGlossaryDocumentStart](./visitglossarydocumentstart/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>) | Kallas när uppräkning av ett glossaridokument har påbörjats. |
| virtual [VisitGroupShapeEnd](./visitgroupshapeend/)(System::SharedPtr\<Aspose::Words::Drawing::GroupShape\>) | Kallas när uppräkning av en gruppform har avslutats. |
| virtual [VisitGroupShapeStart](./visitgroupshapestart/)(System::SharedPtr\<Aspose::Words::Drawing::GroupShape\>) | Kallas när uppräkning av en gruppform har påbörjats. |
| virtual [VisitHeaderFooterEnd](./visitheaderfooterend/)(System::SharedPtr\<Aspose::Words::HeaderFooter\>) | Kallas när uppräkning av ett sidhuvud eller sidfot i ett avsnitt har avslutats. |
| virtual [VisitHeaderFooterStart](./visitheaderfooterstart/)(System::SharedPtr\<Aspose::Words::HeaderFooter\>) | Kallas när uppräkning av ett sidhuvud eller sidfot i ett avsnitt har påbörjats. |
| virtual [VisitOfficeMathEnd](./visitofficemathend/)(System::SharedPtr\<Aspose::Words::Math::OfficeMath\>) | Kallas när uppräkning av ett Office [Math](../../aspose.words.math/)‑objekt har avslutats. |
| virtual [VisitOfficeMathStart](./visitofficemathstart/)(System::SharedPtr\<Aspose::Words::Math::OfficeMath\>) | Kallas när uppräkning av ett Office [Math](../../aspose.words.math/)‑objekt har påbörjats. |
| virtual [VisitParagraphEnd](./visitparagraphend/)(System::SharedPtr\<Aspose::Words::Paragraph\>) | Kallas när uppräkning av ett stycke har avslutats. |
| virtual [VisitParagraphStart](./visitparagraphstart/)(System::SharedPtr\<Aspose::Words::Paragraph\>) | Kallas när uppräkning av ett stycke har påbörjats. |
| virtual [VisitRowEnd](./visitrowend/)(System::SharedPtr\<Aspose::Words::Tables::Row\>) | Kallas när uppräkning av en tabellrad har avslutats. |
| virtual [VisitRowStart](./visitrowstart/)(System::SharedPtr\<Aspose::Words::Tables::Row\>) | Kallas när uppräkning av en tabellrad har påbörjats. |
| virtual [VisitRun](./visitrun/)(System::SharedPtr\<Aspose::Words::Run\>) | Kallas när en textsekvens i den påträffas. |
| virtual [VisitSectionEnd](./visitsectionend/)(System::SharedPtr\<Aspose::Words::Section\>) | Kallas när uppräkning av ett avsnitt har avslutats. |
| virtual [VisitSectionStart](./visitsectionstart/)(System::SharedPtr\<Aspose::Words::Section\>) | Kallas när uppräkning av ett avsnitt har påbörjats. |
| virtual [VisitShapeEnd](./visitshapeend/)(System::SharedPtr\<Aspose::Words::Drawing::Shape\>) | Kallas när uppräkning av en form har avslutats. |
| virtual [VisitShapeStart](./visitshapestart/)(System::SharedPtr\<Aspose::Words::Drawing::Shape\>) | Kallas när uppräkning av en form har påbörjats. |
| virtual [VisitSmartTagEnd](./visitsmarttagend/)(System::SharedPtr\<Aspose::Words::Markup::SmartTag\>) | Kallas när uppräkning av en smart tagg har avslutats. |
| virtual [VisitSmartTagStart](./visitsmarttagstart/)(System::SharedPtr\<Aspose::Words::Markup::SmartTag\>) | Kallas när uppräkning av en smart tagg har påbörjats. |
| virtual [VisitSpecialChar](./visitspecialchar/)(System::SharedPtr\<Aspose::Words::SpecialChar\>) | Kallas när en [SpecialChar](../specialchar/) nod påträffas i dokumentet. |
| virtual [VisitStructuredDocumentTagEnd](./visitstructureddocumenttagend/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>) | Kallas när uppräkning av en strukturerad dokumenttagg har avslutats. |
| virtual [VisitStructuredDocumentTagRangeEnd](./visitstructureddocumenttagrangeend/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTagRangeEnd\>) | Kallas när en StructuredDocumentTagRangeEnd påträffas. |
| virtual [VisitStructuredDocumentTagRangeStart](./visitstructureddocumenttagrangestart/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTagRangeStart\>) | Kallas när en StructuredDocumentTagRangeStart påträffas. |
| virtual [VisitStructuredDocumentTagStart](./visitstructureddocumenttagstart/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>) | Kallas när uppräkning av en strukturerad dokumenttagg har påbörjats. |
| virtual [VisitSubDocument](./visitsubdocument/)(System::SharedPtr\<Aspose::Words::SubDocument\>) | Kallas när ett underdokument påträffas. |
| virtual [VisitTableEnd](./visittableend/)(System::SharedPtr\<Aspose::Words::Tables::Table\>) | Kallas när uppräkning av en tabell har avslutats. |
| virtual [VisitTableStart](./visittablestart/)(System::SharedPtr\<Aspose::Words::Tables::Table\>) | Kallas när uppräkning av en tabell har påbörjats. |
## Anmärkningar


Med [DocumentVisitor](./) kan du definiera och köra anpassade operationer som kräver uppräkning över dokumentträdet.

Till exempel använder Aspose.Words [DocumentVisitor](./) internt för att spara [Document](../document/) i olika format och för andra operationer som att hitta fält eller bokmärken i ett fragment av ett dokument.

För att använda [DocumentVisitor](./):

1. Skapa en klass som är härledd från [DocumentVisitor](./).
1. Åsidosätt och tillhandahåll implementationer för några eller alla VisitXXX‑metoder för att utföra anpassade operationer.
1. Anropa [Node.Accept](../node/accept/) på den [Node](../node/) som du vill börja uppräkningen från.



[DocumentVisitor](./) provides default implementations for all of the VisitXXX methods to make it easier to create new document visitors as only the methods required for the particular visitor need to be overridden. It is not necessary to override all of the visitor methods.

För mer information, se Visitor‑designmönstret.
## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
