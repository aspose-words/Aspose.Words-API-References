---
title: "Classe Aspose::Words::DocumentVisitor"
linktitle: "DocumentVisitor"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::DocumentVisitor. Classe base per i visitatori di documento personalizzati. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 23000
url: /it/cpp/aspose.words/documentvisitor/
---
## DocumentVisitor class


Classe base per i visitatori di documenti personalizzati. Per saperne di più, visita l'articolo di documentazione [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class DocumentVisitor : public virtual System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| virtual [VisitAbsolutePositionTab](./visitabsolutepositiontab/)(System::SharedPtr\<Aspose::Words::AbsolutePositionTab\>) | Chiamato quando nel documento viene incontrato un nodo [AbsolutePositionTab](../absolutepositiontab/). |
| virtual [VisitBodyEnd](./visitbodyend/)(System::SharedPtr\<Aspose::Words::Body\>) | Chiamato quando l'enumerazione della storia di testo principale in una sezione è terminata. |
| virtual [VisitBodyStart](./visitbodystart/)(System::SharedPtr\<Aspose::Words::Body\>) | Chiamato quando l'enumerazione della storia di testo principale in una sezione è iniziata. |
| virtual [VisitBookmarkEnd](./visitbookmarkend/)(System::SharedPtr\<Aspose::Words::BookmarkEnd\>) | Chiamato quando nel documento viene incontrata la fine di un segnalibro. |
| virtual [VisitBookmarkStart](./visitbookmarkstart/)(System::SharedPtr\<Aspose::Words::BookmarkStart\>) | Chiamato quando nel documento viene incontrato l'inizio di un segnalibro. |
| virtual [VisitBuildingBlockEnd](./visitbuildingblockend/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::BuildingBlock\>) | Chiamato quando l'enumerazione di un blocco di costruzione è terminata. |
| virtual [VisitBuildingBlockStart](./visitbuildingblockstart/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::BuildingBlock\>) | Chiamato quando l'enumerazione di un blocco di costruzione è iniziata. |
| virtual [VisitCellEnd](./visitcellend/)(System::SharedPtr\<Aspose::Words::Tables::Cell\>) | Chiamato quando l'enumerazione di una cella di tabella è terminata. |
| virtual [VisitCellStart](./visitcellstart/)(System::SharedPtr\<Aspose::Words::Tables::Cell\>) | Chiamato quando l'enumerazione di una cella di tabella è iniziata. |
| virtual [VisitCommentEnd](./visitcommentend/)(System::SharedPtr\<Aspose::Words::Comment\>) | Chiamato quando l'enumerazione di un testo di commento è terminata. |
| virtual [VisitCommentRangeEnd](./visitcommentrangeend/)(System::SharedPtr\<Aspose::Words::CommentRangeEnd\>) | Chiamato quando viene incontrata la fine di un intervallo di testo commentato. |
| virtual [VisitCommentRangeStart](./visitcommentrangestart/)(System::SharedPtr\<Aspose::Words::CommentRangeStart\>) | Chiamato quando viene incontrato l'inizio di un intervallo di testo commentato. |
| virtual [VisitCommentStart](./visitcommentstart/)(System::SharedPtr\<Aspose::Words::Comment\>) | Chiamato quando l'enumerazione di un testo di commento è iniziata. |
| virtual [VisitDocumentEnd](./visitdocumentend/)(System::SharedPtr\<Aspose::Words::Document\>) | Chiamato quando l'enumerazione del documento è terminata. |
| virtual [VisitDocumentStart](./visitdocumentstart/)(System::SharedPtr\<Aspose::Words::Document\>) | Chiamato quando l'enumerazione del documento è iniziata. |
| virtual [VisitEditableRangeEnd](./visiteditablerangeend/)(System::SharedPtr\<Aspose::Words::EditableRangeEnd\>) | Chiamato quando nel documento viene incontrata la fine di un intervallo modificabile. |
| virtual [VisitEditableRangeStart](./visiteditablerangestart/)(System::SharedPtr\<Aspose::Words::EditableRangeStart\>) | Chiamato quando nel documento viene incontrato l'inizio di un intervallo modificabile. |
| virtual [VisitFieldEnd](./visitfieldend/)(System::SharedPtr\<Aspose::Words::Fields::FieldEnd\>) | Chiamato quando un campo termina nel documento. |
| virtual [VisitFieldSeparator](./visitfieldseparator/)(System::SharedPtr\<Aspose::Words::Fields::FieldSeparator\>) | Chiamato quando viene incontrato un separatore di campo nel documento. |
| virtual [VisitFieldStart](./visitfieldstart/)(System::SharedPtr\<Aspose::Words::Fields::FieldStart\>) | Chiamato quando inizia un campo nel documento. |
| virtual [VisitFootnoteEnd](./visitfootnoteend/)(System::SharedPtr\<Aspose::Words::Notes::Footnote\>) | Chiamato quando l'enumerazione di un testo di nota a piè di pagina o di nota finale è terminata. |
| virtual [VisitFootnoteStart](./visitfootnotestart/)(System::SharedPtr\<Aspose::Words::Notes::Footnote\>) | Chiamato quando inizia l'enumerazione di un testo di nota a piè di pagina o di nota finale. |
| virtual [VisitFormField](./visitformfield/)(System::SharedPtr\<Aspose::Words::Fields::FormField\>) | Chiamato quando viene incontrato un campo modulo nel documento. |
| virtual [VisitGlossaryDocumentEnd](./visitglossarydocumentend/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>) | Chiamato quando l'enumerazione di un documento di glossario è terminata. |
| virtual [VisitGlossaryDocumentStart](./visitglossarydocumentstart/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>) | Chiamato quando inizia l'enumerazione di un documento di glossario. |
| virtual [VisitGroupShapeEnd](./visitgroupshapeend/)(System::SharedPtr\<Aspose::Words::Drawing::GroupShape\>) | Chiamato quando l'enumerazione di una forma di gruppo è terminata. |
| virtual [VisitGroupShapeStart](./visitgroupshapestart/)(System::SharedPtr\<Aspose::Words::Drawing::GroupShape\>) | Chiamato quando inizia l'enumerazione di una forma di gruppo. |
| virtual [VisitHeaderFooterEnd](./visitheaderfooterend/)(System::SharedPtr\<Aspose::Words::HeaderFooter\>) | Chiamato quando l'enumerazione di un'intestazione o di un piè di pagina in una sezione è terminata. |
| virtual [VisitHeaderFooterStart](./visitheaderfooterstart/)(System::SharedPtr\<Aspose::Words::HeaderFooter\>) | Chiamato quando inizia l'enumerazione di un'intestazione o di un piè di pagina in una sezione. |
| virtual [VisitOfficeMathEnd](./visitofficemathend/)(System::SharedPtr\<Aspose::Words::Math::OfficeMath\>) | Chiamato quando l'enumerazione di un oggetto Office [Math](../../aspose.words.math/) è terminata. |
| virtual [VisitOfficeMathStart](./visitofficemathstart/)(System::SharedPtr\<Aspose::Words::Math::OfficeMath\>) | Chiamato quando inizia l'enumerazione di un oggetto Office [Math](../../aspose.words.math/). |
| virtual [VisitParagraphEnd](./visitparagraphend/)(System::SharedPtr\<Aspose::Words::Paragraph\>) | Chiamato quando l'enumerazione di un paragrafo è terminata. |
| virtual [VisitParagraphStart](./visitparagraphstart/)(System::SharedPtr\<Aspose::Words::Paragraph\>) | Chiamato quando inizia l'enumerazione di un paragrafo. |
| virtual [VisitRowEnd](./visitrowend/)(System::SharedPtr\<Aspose::Words::Tables::Row\>) | Chiamato quando l'enumerazione di una riga di tabella è terminata. |
| virtual [VisitRowStart](./visitrowstart/)(System::SharedPtr\<Aspose::Words::Tables::Row\>) | Chiamato quando inizia l'enumerazione di una riga di tabella. |
| virtual [VisitRun](./visitrun/)(System::SharedPtr\<Aspose::Words::Run\>) | Chiamato quando viene incontrata una sequenza di testo nel documento. |
| virtual [VisitSectionEnd](./visitsectionend/)(System::SharedPtr\<Aspose::Words::Section\>) | Chiamato quando l'enumerazione di una sezione è terminata. |
| virtual [VisitSectionStart](./visitsectionstart/)(System::SharedPtr\<Aspose::Words::Section\>) | Chiamato quando inizia l'enumerazione di una sezione. |
| virtual [VisitShapeEnd](./visitshapeend/)(System::SharedPtr\<Aspose::Words::Drawing::Shape\>) | Chiamato quando l'enumerazione di una forma è terminata. |
| virtual [VisitShapeStart](./visitshapestart/)(System::SharedPtr\<Aspose::Words::Drawing::Shape\>) | Chiamato quando inizia l'enumerazione di una forma. |
| virtual [VisitSmartTagEnd](./visitsmarttagend/)(System::SharedPtr\<Aspose::Words::Markup::SmartTag\>) | Chiamato quando l'enumerazione di un tag intelligente è terminata. |
| virtual [VisitSmartTagStart](./visitsmarttagstart/)(System::SharedPtr\<Aspose::Words::Markup::SmartTag\>) | Chiamato quando inizia l'enumerazione di un tag intelligente. |
| virtual [VisitSpecialChar](./visitspecialchar/)(System::SharedPtr\<Aspose::Words::SpecialChar\>) | Chiamato quando viene incontrato un nodo [SpecialChar](../specialchar/) nel documento. |
| virtual [VisitStructuredDocumentTagEnd](./visitstructureddocumenttagend/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>) | Chiamata quando l'enumerazione di un tag di documento strutturato è terminata. |
| virtual [VisitStructuredDocumentTagRangeEnd](./visitstructureddocumenttagrangeend/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTagRangeEnd\>) | Chiamata quando viene incontrato un StructuredDocumentTagRangeEnd. |
| virtual [VisitStructuredDocumentTagRangeStart](./visitstructureddocumenttagrangestart/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTagRangeStart\>) | Chiamata quando viene incontrato un StructuredDocumentTagRangeStart. |
| virtual [VisitStructuredDocumentTagStart](./visitstructureddocumenttagstart/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>) | Chiamata quando l'enumerazione di un tag di documento strutturato è iniziata. |
| virtual [VisitSubDocument](./visitsubdocument/)(System::SharedPtr\<Aspose::Words::SubDocument\>) | Chiamata quando viene incontrato un sotto-documento. |
| virtual [VisitTableEnd](./visittableend/)(System::SharedPtr\<Aspose::Words::Tables::Table\>) | Chiamata quando l'enumerazione di una tabella è terminata. |
| virtual [VisitTableStart](./visittablestart/)(System::SharedPtr\<Aspose::Words::Tables::Table\>) | Chiamata quando l'enumerazione di una tabella è iniziata. |
## Note


Con [DocumentVisitor](./) è possibile definire ed eseguire operazioni personalizzate che richiedono l'enumerazione dell'albero del documento.

Ad esempio, Aspose.Words utilizza internamente [DocumentVisitor](./) per salvare [Document](../document/) in vari formati e per altre operazioni come la ricerca di campi o segnalibri su un frammento di documento.

Per utilizzare [DocumentVisitor](./):

1. Creare una classe derivata da [DocumentVisitor](./).
1. Sovrascrivere e fornire implementazioni per alcuni o tutti i metodi VisitXXX per eseguire operazioni personalizzate.
1. Chiamare [Node.Accept](../node/accept/) sul [Node](../node/) da cui si desidera avviare l'enumerazione.



[DocumentVisitor](./) provides default implementations for all of the VisitXXX methods to make it easier to create new document visitors as only the methods required for the particular visitor need to be overridden. It is not necessary to override all of the visitor methods.

Per ulteriori informazioni, vedere il pattern di progettazione Visitor.
## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
