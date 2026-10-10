---
title: "Aspose::Words::DocumentVisitor clase"
linktitle: "DocumentVisitor"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentVisitor clase. Clase base para visitantes de documentos personalizados. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 23000
url: /es/cpp/aspose.words/documentvisitor/
---
## DocumentVisitor class


Clase base para visitantes de documentos personalizados. Para obtener más información, visite el artículo de documentación [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class DocumentVisitor : public virtual System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| virtual [VisitAbsolutePositionTab](./visitabsolutepositiontab/)(System::SharedPtr\<Aspose::Words::AbsolutePositionTab\>) | Se llama cuando se encuentra un nodo [AbsolutePositionTab](../absolutepositiontab/) en el documento. |
| virtual [VisitBodyEnd](./visitbodyend/)(System::SharedPtr\<Aspose::Words::Body\>) | Se llama cuando la enumeración de la historia principal de texto en una sección ha finalizado. |
| virtual [VisitBodyStart](./visitbodystart/)(System::SharedPtr\<Aspose::Words::Body\>) | Se llama cuando la enumeración de la historia principal de texto en una sección ha comenzado. |
| virtual [VisitBookmarkEnd](./visitbookmarkend/)(System::SharedPtr\<Aspose::Words::BookmarkEnd\>) | Se llama cuando se encuentra el final de un marcador en el documento. |
| virtual [VisitBookmarkStart](./visitbookmarkstart/)(System::SharedPtr\<Aspose::Words::BookmarkStart\>) | Se llama cuando se encuentra el inicio de un marcador en el documento. |
| virtual [VisitBuildingBlockEnd](./visitbuildingblockend/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::BuildingBlock\>) | Se llama cuando la enumeración de un bloque de construcción ha finalizado. |
| virtual [VisitBuildingBlockStart](./visitbuildingblockstart/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::BuildingBlock\>) | Se llama cuando la enumeración de un bloque de construcción ha comenzado. |
| virtual [VisitCellEnd](./visitcellend/)(System::SharedPtr\<Aspose::Words::Tables::Cell\>) | Se llama cuando la enumeración de una celda de tabla ha finalizado. |
| virtual [VisitCellStart](./visitcellstart/)(System::SharedPtr\<Aspose::Words::Tables::Cell\>) | Se llama cuando la enumeración de una celda de tabla ha comenzado. |
| virtual [VisitCommentEnd](./visitcommentend/)(System::SharedPtr\<Aspose::Words::Comment\>) | Se llama cuando la enumeración de un texto de comentario ha finalizado. |
| virtual [VisitCommentRangeEnd](./visitcommentrangeend/)(System::SharedPtr\<Aspose::Words::CommentRangeEnd\>) | Se llama cuando se encuentra el final de un rango de texto comentado. |
| virtual [VisitCommentRangeStart](./visitcommentrangestart/)(System::SharedPtr\<Aspose::Words::CommentRangeStart\>) | Se llama cuando se encuentra el inicio de un rango de texto comentado. |
| virtual [VisitCommentStart](./visitcommentstart/)(System::SharedPtr\<Aspose::Words::Comment\>) | Se llama cuando la enumeración de un texto de comentario ha comenzado. |
| virtual [VisitDocumentEnd](./visitdocumentend/)(System::SharedPtr\<Aspose::Words::Document\>) | Se llama cuando la enumeración del documento ha finalizado. |
| virtual [VisitDocumentStart](./visitdocumentstart/)(System::SharedPtr\<Aspose::Words::Document\>) | Se llama cuando la enumeración del documento ha comenzado. |
| virtual [VisitEditableRangeEnd](./visiteditablerangeend/)(System::SharedPtr\<Aspose::Words::EditableRangeEnd\>) | Se llama cuando se encuentra el final de un rango editable en el documento. |
| virtual [VisitEditableRangeStart](./visiteditablerangestart/)(System::SharedPtr\<Aspose::Words::EditableRangeStart\>) | Se llama cuando se encuentra el inicio de un rango editable en el documento. |
| virtual [VisitFieldEnd](./visitfieldend/)(System::SharedPtr\<Aspose::Words::Fields::FieldEnd\>) | Se llama cuando un campo termina en el documento. |
| virtual [VisitFieldSeparator](./visitfieldseparator/)(System::SharedPtr\<Aspose::Words::Fields::FieldSeparator\>) | Se llama cuando se encuentra un separador de campo en el documento. |
| virtual [VisitFieldStart](./visitfieldstart/)(System::SharedPtr\<Aspose::Words::Fields::FieldStart\>) | Se llama cuando comienza un campo en el documento. |
| virtual [VisitFootnoteEnd](./visitfootnoteend/)(System::SharedPtr\<Aspose::Words::Notes::Footnote\>) | Se llama cuando la enumeración del texto de una nota al pie o nota al final ha finalizado. |
| virtual [VisitFootnoteStart](./visitfootnotestart/)(System::SharedPtr\<Aspose::Words::Notes::Footnote\>) | Se llama cuando la enumeración del texto de una nota al pie o nota al final ha comenzado. |
| virtual [VisitFormField](./visitformfield/)(System::SharedPtr\<Aspose::Words::Fields::FormField\>) | Se llama cuando se encuentra un campo de formulario en el documento. |
| virtual [VisitGlossaryDocumentEnd](./visitglossarydocumentend/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>) | Se llama cuando la enumeración de un documento de glosario ha finalizado. |
| virtual [VisitGlossaryDocumentStart](./visitglossarydocumentstart/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>) | Se llama cuando la enumeración de un documento de glosario ha comenzado. |
| virtual [VisitGroupShapeEnd](./visitgroupshapeend/)(System::SharedPtr\<Aspose::Words::Drawing::GroupShape\>) | Se llama cuando la enumeración de una forma de grupo ha finalizado. |
| virtual [VisitGroupShapeStart](./visitgroupshapestart/)(System::SharedPtr\<Aspose::Words::Drawing::GroupShape\>) | Se llama cuando la enumeración de una forma de grupo ha comenzado. |
| virtual [VisitHeaderFooterEnd](./visitheaderfooterend/)(System::SharedPtr\<Aspose::Words::HeaderFooter\>) | Se llama cuando la enumeración de un encabezado o pie de página en una sección ha finalizado. |
| virtual [VisitHeaderFooterStart](./visitheaderfooterstart/)(System::SharedPtr\<Aspose::Words::HeaderFooter\>) | Se llama cuando la enumeración de un encabezado o pie de página en una sección ha comenzado. |
| virtual [VisitOfficeMathEnd](./visitofficemathend/)(System::SharedPtr\<Aspose::Words::Math::OfficeMath\>) | Se llama cuando la enumeración de un objeto Office [Math](../../aspose.words.math/) ha finalizado. |
| virtual [VisitOfficeMathStart](./visitofficemathstart/)(System::SharedPtr\<Aspose::Words::Math::OfficeMath\>) | Se llama cuando la enumeración de un objeto Office [Math](../../aspose.words.math/) ha comenzado. |
| virtual [VisitParagraphEnd](./visitparagraphend/)(System::SharedPtr\<Aspose::Words::Paragraph\>) | Se llama cuando la enumeración de un párrafo ha finalizado. |
| virtual [VisitParagraphStart](./visitparagraphstart/)(System::SharedPtr\<Aspose::Words::Paragraph\>) | Se llama cuando la enumeración de un párrafo ha comenzado. |
| virtual [VisitRowEnd](./visitrowend/)(System::SharedPtr\<Aspose::Words::Tables::Row\>) | Se llama cuando la enumeración de una fila de tabla ha finalizado. |
| virtual [VisitRowStart](./visitrowstart/)(System::SharedPtr\<Aspose::Words::Tables::Row\>) | Se llama cuando la enumeración de una fila de tabla ha comenzado. |
| virtual [VisitRun](./visitrun/)(System::SharedPtr\<Aspose::Words::Run\>) | Se llama cuando se encuentra una ejecución de texto en el documento. |
| virtual [VisitSectionEnd](./visitsectionend/)(System::SharedPtr\<Aspose::Words::Section\>) | Se llama cuando la enumeración de una sección ha finalizado. |
| virtual [VisitSectionStart](./visitsectionstart/)(System::SharedPtr\<Aspose::Words::Section\>) | Se llama cuando la enumeración de una sección ha comenzado. |
| virtual [VisitShapeEnd](./visitshapeend/)(System::SharedPtr\<Aspose::Words::Drawing::Shape\>) | Se llama cuando la enumeración de una forma ha finalizado. |
| virtual [VisitShapeStart](./visitshapestart/)(System::SharedPtr\<Aspose::Words::Drawing::Shape\>) | Se llama cuando la enumeración de una forma ha comenzado. |
| virtual [VisitSmartTagEnd](./visitsmarttagend/)(System::SharedPtr\<Aspose::Words::Markup::SmartTag\>) | Se llama cuando la enumeración de una etiqueta inteligente ha finalizado. |
| virtual [VisitSmartTagStart](./visitsmarttagstart/)(System::SharedPtr\<Aspose::Words::Markup::SmartTag\>) | Se llama cuando la enumeración de una etiqueta inteligente ha comenzado. |
| virtual [VisitSpecialChar](./visitspecialchar/)(System::SharedPtr\<Aspose::Words::SpecialChar\>) | Se llama cuando se encuentra un nodo [SpecialChar](../specialchar/) en el documento. |
| virtual [VisitStructuredDocumentTagEnd](./visitstructureddocumenttagend/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>) | Se llama cuando la enumeración de una etiqueta de documento estructurado ha finalizado. |
| virtual [VisitStructuredDocumentTagRangeEnd](./visitstructureddocumenttagrangeend/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTagRangeEnd\>) | Se llama cuando se encuentra un StructuredDocumentTagRangeEnd. |
| virtual [VisitStructuredDocumentTagRangeStart](./visitstructureddocumenttagrangestart/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTagRangeStart\>) | Se llama cuando se encuentra un StructuredDocumentTagRangeStart. |
| virtual [VisitStructuredDocumentTagStart](./visitstructureddocumenttagstart/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>) | Se llama cuando la enumeración de una etiqueta de documento estructurado ha comenzado. |
| virtual [VisitSubDocument](./visitsubdocument/)(System::SharedPtr\<Aspose::Words::SubDocument\>) | Se llama cuando se encuentra un subdocumento. |
| virtual [VisitTableEnd](./visittableend/)(System::SharedPtr\<Aspose::Words::Tables::Table\>) | Se llama cuando la enumeración de una tabla ha finalizado. |
| virtual [VisitTableStart](./visittablestart/)(System::SharedPtr\<Aspose::Words::Tables::Table\>) | Se llama cuando la enumeración de una tabla ha comenzado. |
## Observaciones


Con [DocumentVisitor](./) puedes definir y ejecutar operaciones personalizadas que requieren enumeración sobre el árbol del documento.

Por ejemplo, Aspose.Words utiliza [DocumentVisitor](./) internamente para guardar [Document](../document/) en varios formatos y para otras operaciones como buscar campos o marcadores en un fragmento de un documento.

Para usar [DocumentVisitor](./):

1. Crea una clase derivada de [DocumentVisitor](./).
1. Sobrescribe y proporciona implementaciones para algunos o todos los métodos VisitXXX para realizar operaciones personalizadas.
1. Llama a [Node.Accept](../node/accept/) en el [Node](../node/) desde el que deseas iniciar la enumeración.



[DocumentVisitor](./) provides default implementations for all of the VisitXXX methods to make it easier to create new document visitors as only the methods required for the particular visitor need to be overridden. It is not necessary to override all of the visitor methods.

Para más información, consulta el patrón de diseño Visitor.
## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
