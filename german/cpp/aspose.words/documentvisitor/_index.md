---
title: "Aspose::Words::DocumentVisitor Klasse"
linktitle: "DocumentVisitor"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentVisitor Klasse. Basisklasse für benutzerdefinierte Dokumentbesucher. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 23000
url: /de/cpp/aspose.words/documentvisitor/
---
## DocumentVisitor class


Basisklasse für benutzerdefinierte Dokumentbesucher. Weitere Informationen finden Sie im Dokumentationsartikel [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class DocumentVisitor : public virtual System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| virtual [VisitAbsolutePositionTab](./visitabsolutepositiontab/)(System::SharedPtr\<Aspose::Words::AbsolutePositionTab\>) | Wird aufgerufen, wenn ein [AbsolutePositionTab](../absolutepositiontab/) Knoten im Dokument gefunden wird. |
| virtual [VisitBodyEnd](./visitbodyend/)(System::SharedPtr\<Aspose::Words::Body\>) | Wird aufgerufen, wenn die Aufzählung der Haupttextgeschichte in einem Abschnitt beendet ist. |
| virtual [VisitBodyStart](./visitbodystart/)(System::SharedPtr\<Aspose::Words::Body\>) | Wird aufgerufen, wenn die Aufzählung der Haupttextgeschichte in einem Abschnitt begonnen hat. |
| virtual [VisitBookmarkEnd](./visitbookmarkend/)(System::SharedPtr\<Aspose::Words::BookmarkEnd\>) | Wird aufgerufen, wenn das Ende eines Lesezeichens im Dokument gefunden wird. |
| virtual [VisitBookmarkStart](./visitbookmarkstart/)(System::SharedPtr\<Aspose::Words::BookmarkStart\>) | Wird aufgerufen, wenn der Beginn eines Lesezeichens im Dokument gefunden wird. |
| virtual [VisitBuildingBlockEnd](./visitbuildingblockend/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::BuildingBlock\>) | Wird aufgerufen, wenn die Aufzählung eines Bausteins beendet ist. |
| virtual [VisitBuildingBlockStart](./visitbuildingblockstart/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::BuildingBlock\>) | Wird aufgerufen, wenn die Aufzählung eines Bausteins begonnen hat. |
| virtual [VisitCellEnd](./visitcellend/)(System::SharedPtr\<Aspose::Words::Tables::Cell\>) | Wird aufgerufen, wenn die Aufzählung einer Tabellenzelle beendet ist. |
| virtual [VisitCellStart](./visitcellstart/)(System::SharedPtr\<Aspose::Words::Tables::Cell\>) | Wird aufgerufen, wenn die Aufzählung einer Tabellenzelle begonnen hat. |
| virtual [VisitCommentEnd](./visitcommentend/)(System::SharedPtr\<Aspose::Words::Comment\>) | Wird aufgerufen, wenn die Aufzählung eines Kommentartexts beendet ist. |
| virtual [VisitCommentRangeEnd](./visitcommentrangeend/)(System::SharedPtr\<Aspose::Words::CommentRangeEnd\>) | Wird aufgerufen, wenn das Ende eines kommentierten Textbereichs gefunden wird. |
| virtual [VisitCommentRangeStart](./visitcommentrangestart/)(System::SharedPtr\<Aspose::Words::CommentRangeStart\>) | Wird aufgerufen, wenn der Beginn eines kommentierten Textbereichs gefunden wird. |
| virtual [VisitCommentStart](./visitcommentstart/)(System::SharedPtr\<Aspose::Words::Comment\>) | Wird aufgerufen, wenn die Aufzählung eines Kommentartexts begonnen hat. |
| virtual [VisitDocumentEnd](./visitdocumentend/)(System::SharedPtr\<Aspose::Words::Document\>) | Wird aufgerufen, wenn die Aufzählung des Dokuments abgeschlossen ist. |
| virtual [VisitDocumentStart](./visitdocumentstart/)(System::SharedPtr\<Aspose::Words::Document\>) | Wird aufgerufen, wenn die Aufzählung des Dokuments begonnen hat. |
| virtual [VisitEditableRangeEnd](./visiteditablerangeend/)(System::SharedPtr\<Aspose::Words::EditableRangeEnd\>) | Aufgerufen, wenn das Ende eines bearbeitbaren Bereichs im Dokument gefunden wird. |
| virtual [VisitEditableRangeStart](./visiteditablerangestart/)(System::SharedPtr\<Aspose::Words::EditableRangeStart\>) | Aufgerufen, wenn der Anfang eines bearbeitbaren Bereichs im Dokument gefunden wird. |
| virtual [VisitFieldEnd](./visitfieldend/)(System::SharedPtr\<Aspose::Words::Fields::FieldEnd\>) | Aufgerufen, wenn ein Feld im Dokument endet. |
| virtual [VisitFieldSeparator](./visitfieldseparator/)(System::SharedPtr\<Aspose::Words::Fields::FieldSeparator\>) | Aufgerufen, wenn ein Feldtrennzeichen im Dokument gefunden wird. |
| virtual [VisitFieldStart](./visitfieldstart/)(System::SharedPtr\<Aspose::Words::Fields::FieldStart\>) | Aufgerufen, wenn ein Feld im Dokument beginnt. |
| virtual [VisitFootnoteEnd](./visitfootnoteend/)(System::SharedPtr\<Aspose::Words::Notes::Footnote\>) | Aufgerufen, wenn die Aufzählung eines Fuß- oder Endnotentextes beendet ist. |
| virtual [VisitFootnoteStart](./visitfootnotestart/)(System::SharedPtr\<Aspose::Words::Notes::Footnote\>) | Aufgerufen, wenn die Aufzählung eines Fuß- oder Endnotentextes begonnen hat. |
| virtual [VisitFormField](./visitformfield/)(System::SharedPtr\<Aspose::Words::Fields::FormField\>) | Aufgerufen, wenn ein Formularfeld im Dokument gefunden wird. |
| virtual [VisitGlossaryDocumentEnd](./visitglossarydocumentend/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>) | Aufgerufen, wenn die Aufzählung eines Glossar-Dokuments beendet ist. |
| virtual [VisitGlossaryDocumentStart](./visitglossarydocumentstart/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>) | Aufgerufen, wenn die Aufzählung eines Glossar-Dokuments begonnen hat. |
| virtual [VisitGroupShapeEnd](./visitgroupshapeend/)(System::SharedPtr\<Aspose::Words::Drawing::GroupShape\>) | Aufgerufen, wenn die Aufzählung einer Gruppenform beendet ist. |
| virtual [VisitGroupShapeStart](./visitgroupshapestart/)(System::SharedPtr\<Aspose::Words::Drawing::GroupShape\>) | Aufgerufen, wenn die Aufzählung einer Gruppenform begonnen hat. |
| virtual [VisitHeaderFooterEnd](./visitheaderfooterend/)(System::SharedPtr\<Aspose::Words::HeaderFooter\>) | Aufgerufen, wenn die Aufzählung einer Kopf- oder Fußzeile in einem Abschnitt beendet ist. |
| virtual [VisitHeaderFooterStart](./visitheaderfooterstart/)(System::SharedPtr\<Aspose::Words::HeaderFooter\>) | Aufgerufen, wenn die Aufzählung einer Kopf- oder Fußzeile in einem Abschnitt begonnen hat. |
| virtual [VisitOfficeMathEnd](./visitofficemathend/)(System::SharedPtr\<Aspose::Words::Math::OfficeMath\>) | Aufgerufen, wenn die Aufzählung eines Office [Math](../../aspose.words.math/) Objekts beendet ist. |
| virtual [VisitOfficeMathStart](./visitofficemathstart/)(System::SharedPtr\<Aspose::Words::Math::OfficeMath\>) | Aufgerufen, wenn die Aufzählung eines Office [Math](../../aspose.words.math/) Objekts begonnen hat. |
| virtual [VisitParagraphEnd](./visitparagraphend/)(System::SharedPtr\<Aspose::Words::Paragraph\>) | Aufgerufen, wenn die Aufzählung eines Absatzes beendet ist. |
| virtual [VisitParagraphStart](./visitparagraphstart/)(System::SharedPtr\<Aspose::Words::Paragraph\>) | Aufgerufen, wenn die Aufzählung eines Absatzes begonnen hat. |
| virtual [VisitRowEnd](./visitrowend/)(System::SharedPtr\<Aspose::Words::Tables::Row\>) | Aufgerufen, wenn die Aufzählung einer Tabellenzeile beendet ist. |
| virtual [VisitRowStart](./visitrowstart/)(System::SharedPtr\<Aspose::Words::Tables::Row\>) | Aufgerufen, wenn die Aufzählung einer Tabellenzeile begonnen hat. |
| virtual [VisitRun](./visitrun/)(System::SharedPtr\<Aspose::Words::Run\>) | Aufgerufen, wenn ein Textlauf im Dokument gefunden wird. |
| virtual [VisitSectionEnd](./visitsectionend/)(System::SharedPtr\<Aspose::Words::Section\>) | Aufgerufen, wenn die Aufzählung eines Abschnitts beendet ist. |
| virtual [VisitSectionStart](./visitsectionstart/)(System::SharedPtr\<Aspose::Words::Section\>) | Aufgerufen, wenn die Aufzählung eines Abschnitts begonnen hat. |
| virtual [VisitShapeEnd](./visitshapeend/)(System::SharedPtr\<Aspose::Words::Drawing::Shape\>) | Aufgerufen, wenn die Aufzählung einer Form beendet ist. |
| virtual [VisitShapeStart](./visitshapestart/)(System::SharedPtr\<Aspose::Words::Drawing::Shape\>) | Aufgerufen, wenn die Aufzählung einer Form begonnen hat. |
| virtual [VisitSmartTagEnd](./visitsmarttagend/)(System::SharedPtr\<Aspose::Words::Markup::SmartTag\>) | Aufgerufen, wenn die Aufzählung eines Smart-Tags beendet ist. |
| virtual [VisitSmartTagStart](./visitsmarttagstart/)(System::SharedPtr\<Aspose::Words::Markup::SmartTag\>) | Aufgerufen, wenn die Aufzählung eines Smart-Tags begonnen hat. |
| virtual [VisitSpecialChar](./visitspecialchar/)(System::SharedPtr\<Aspose::Words::SpecialChar\>) | Aufgerufen, wenn ein [SpecialChar](../specialchar/)‑Knoten im Dokument gefunden wird. |
| virtual [VisitStructuredDocumentTagEnd](./visitstructureddocumenttagend/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>) | Aufgerufen, wenn die Aufzählung eines strukturierten Dokumenttags beendet ist. |
| virtual [VisitStructuredDocumentTagRangeEnd](./visitstructureddocumenttagrangeend/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTagRangeEnd\>) | Aufgerufen, wenn ein StructuredDocumentTagRangeEnd gefunden wird. |
| virtual [VisitStructuredDocumentTagRangeStart](./visitstructureddocumenttagrangestart/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTagRangeStart\>) | Aufgerufen, wenn ein StructuredDocumentTagRangeStart gefunden wird. |
| virtual [VisitStructuredDocumentTagStart](./visitstructureddocumenttagstart/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>) | Aufgerufen, wenn die Aufzählung eines strukturierten Dokumenttags begonnen hat. |
| virtual [VisitSubDocument](./visitsubdocument/)(System::SharedPtr\<Aspose::Words::SubDocument\>) | Aufgerufen, wenn ein Unterdokument gefunden wird. |
| virtual [VisitTableEnd](./visittableend/)(System::SharedPtr\<Aspose::Words::Tables::Table\>) | Aufgerufen, wenn die Aufzählung einer Tabelle beendet ist. |
| virtual [VisitTableStart](./visittablestart/)(System::SharedPtr\<Aspose::Words::Tables::Table\>) | Aufgerufen, wenn die Aufzählung einer Tabelle begonnen hat. |
## Hinweise


Mit [DocumentVisitor](./) können Sie benutzerdefinierte Vorgänge definieren und ausführen, die eine Aufzählung des Dokumentbaums erfordern.

Zum Beispiel verwendet Aspose.Words intern [DocumentVisitor](./) zum Speichern von [Document](../document/) in verschiedenen Formaten und für andere Vorgänge wie das Suchen von Feldern oder Lesezeichen in einem Dokumentfragment.

So verwenden Sie [DocumentVisitor](./):

1. Erstellen Sie eine Klasse, die von [DocumentVisitor](./) abgeleitet ist.
1. Überschreiben Sie und implementieren Sie einige oder alle VisitXXX‑Methoden, um benutzerdefinierte Vorgänge auszuführen.
1. Rufen Sie [Node.Accept](../node/accept/) auf dem [Node](../node/) auf, von dem Sie die Aufzählung starten möchten.



[DocumentVisitor](./) provides default implementations for all of the VisitXXX methods to make it easier to create new document visitors as only the methods required for the particular visitor need to be overridden. It is not necessary to override all of the visitor methods.

Weitere Informationen finden Sie im Visitor-Entwurfsmuster.
## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
