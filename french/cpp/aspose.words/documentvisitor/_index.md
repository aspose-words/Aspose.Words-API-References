---
title: "Classe Aspose::Words::DocumentVisitor"
linktitle: "DocumentVisitor"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::DocumentVisitor. Classe de base pour les visiteurs de documents personnalisés. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 23000
url: /fr/cpp/aspose.words/documentvisitor/
---
## DocumentVisitor class


Classe de base pour les visiteurs de document personnalisés. Pour en savoir plus, consultez l'article de documentation [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class DocumentVisitor : public virtual System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| virtual [VisitAbsolutePositionTab](./visitabsolutepositiontab/)(System::SharedPtr\<Aspose::Words::AbsolutePositionTab\>) | Appelé lorsqu'un nœud [AbsolutePositionTab](../absolutepositiontab/) est rencontré dans le document. |
| virtual [VisitBodyEnd](./visitbodyend/)(System::SharedPtr\<Aspose::Words::Body\>) | Appelé lorsque l'énumération de l'histoire principale du texte dans une section est terminée. |
| virtual [VisitBodyStart](./visitbodystart/)(System::SharedPtr\<Aspose::Words::Body\>) | Appelé lorsque l'énumération de l'histoire principale du texte dans une section a commencé. |
| virtual [VisitBookmarkEnd](./visitbookmarkend/)(System::SharedPtr\<Aspose::Words::BookmarkEnd\>) | Appelé lorsqu'une fin de signet est rencontrée dans le document. |
| virtual [VisitBookmarkStart](./visitbookmarkstart/)(System::SharedPtr\<Aspose::Words::BookmarkStart\>) | Appelé lorsqu'un début de signet est rencontré dans le document. |
| virtual [VisitBuildingBlockEnd](./visitbuildingblockend/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::BuildingBlock\>) | Appelé lorsque l'énumération d'un bloc de construction est terminée. |
| virtual [VisitBuildingBlockStart](./visitbuildingblockstart/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::BuildingBlock\>) | Appelé lorsque l'énumération d'un bloc de construction a commencé. |
| virtual [VisitCellEnd](./visitcellend/)(System::SharedPtr\<Aspose::Words::Tables::Cell\>) | Appelé lorsque l'énumération d'une cellule de tableau est terminée. |
| virtual [VisitCellStart](./visitcellstart/)(System::SharedPtr\<Aspose::Words::Tables::Cell\>) | Appelé lorsque l'énumération d'une cellule de tableau a commencé. |
| virtual [VisitCommentEnd](./visitcommentend/)(System::SharedPtr\<Aspose::Words::Comment\>) | Appelé lorsque l'énumération d'un texte de commentaire est terminée. |
| virtual [VisitCommentRangeEnd](./visitcommentrangeend/)(System::SharedPtr\<Aspose::Words::CommentRangeEnd\>) | Appelé lorsqu'une fin d'une plage de texte commentée est rencontrée. |
| virtual [VisitCommentRangeStart](./visitcommentrangestart/)(System::SharedPtr\<Aspose::Words::CommentRangeStart\>) | Appelé lorsqu'un début d'une plage de texte commentée est rencontré. |
| virtual [VisitCommentStart](./visitcommentstart/)(System::SharedPtr\<Aspose::Words::Comment\>) | Appelé lorsque l'énumération d'un texte de commentaire a commencé. |
| virtual [VisitDocumentEnd](./visitdocumentend/)(System::SharedPtr\<Aspose::Words::Document\>) | Appelé lorsque l'énumération du document est terminée. |
| virtual [VisitDocumentStart](./visitdocumentstart/)(System::SharedPtr\<Aspose::Words::Document\>) | Appelé lorsque l'énumération du document a commencé. |
| virtual [VisitEditableRangeEnd](./visiteditablerangeend/)(System::SharedPtr\<Aspose::Words::EditableRangeEnd\>) | Appelé lorsqu'une fin d'une plage modifiable est rencontrée dans le document. |
| virtual [VisitEditableRangeStart](./visiteditablerangestart/)(System::SharedPtr\<Aspose::Words::EditableRangeStart\>) | Appelé lorsqu'un début d'une plage modifiable est rencontré dans le document. |
| virtual [VisitFieldEnd](./visitfieldend/)(System::SharedPtr\<Aspose::Words::Fields::FieldEnd\>) | Appelé lorsqu'un champ se termine dans le document. |
| virtual [VisitFieldSeparator](./visitfieldseparator/)(System::SharedPtr\<Aspose::Words::Fields::FieldSeparator\>) | Appelé lorsqu'un séparateur de champ est rencontré dans le document. |
| virtual [VisitFieldStart](./visitfieldstart/)(System::SharedPtr\<Aspose::Words::Fields::FieldStart\>) | Appelé lorsqu'un champ commence dans le document. |
| virtual [VisitFootnoteEnd](./visitfootnoteend/)(System::SharedPtr\<Aspose::Words::Notes::Footnote\>) | Appelé lorsque l'énumération d'un texte de note de bas de page ou de note de fin est terminée. |
| virtual [VisitFootnoteStart](./visitfootnotestart/)(System::SharedPtr\<Aspose::Words::Notes::Footnote\>) | Appelé lorsque l'énumération d'un texte de note de bas de page ou de note de fin a commencé. |
| virtual [VisitFormField](./visitformfield/)(System::SharedPtr\<Aspose::Words::Fields::FormField\>) | Appelé lorsqu'un champ de formulaire est rencontré dans le document. |
| virtual [VisitGlossaryDocumentEnd](./visitglossarydocumentend/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>) | Appelé lorsque l'énumération d'un document de glossaire est terminée. |
| virtual [VisitGlossaryDocumentStart](./visitglossarydocumentstart/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>) | Appelé lorsque l'énumération d'un document de glossaire a commencé. |
| virtual [VisitGroupShapeEnd](./visitgroupshapeend/)(System::SharedPtr\<Aspose::Words::Drawing::GroupShape\>) | Appelé lorsque l'énumération d'une forme groupée est terminée. |
| virtual [VisitGroupShapeStart](./visitgroupshapestart/)(System::SharedPtr\<Aspose::Words::Drawing::GroupShape\>) | Appelé lorsque l'énumération d'une forme groupée a commencé. |
| virtual [VisitHeaderFooterEnd](./visitheaderfooterend/)(System::SharedPtr\<Aspose::Words::HeaderFooter\>) | Appelé lorsque l'énumération d'un en-tête ou d'un pied de page dans une section est terminée. |
| virtual [VisitHeaderFooterStart](./visitheaderfooterstart/)(System::SharedPtr\<Aspose::Words::HeaderFooter\>) | Appelé lorsque l'énumération d'un en-tête ou d'un pied de page dans une section a commencé. |
| virtual [VisitOfficeMathEnd](./visitofficemathend/)(System::SharedPtr\<Aspose::Words::Math::OfficeMath\>) | Appelé lorsque l'énumération d'un objet Office [Math](../../aspose.words.math/) est terminée. |
| virtual [VisitOfficeMathStart](./visitofficemathstart/)(System::SharedPtr\<Aspose::Words::Math::OfficeMath\>) | Appelé lorsque l'énumération d'un objet Office [Math](../../aspose.words.math/) a commencé. |
| virtual [VisitParagraphEnd](./visitparagraphend/)(System::SharedPtr\<Aspose::Words::Paragraph\>) | Appelé lorsque l'énumération d'un paragraphe est terminée. |
| virtual [VisitParagraphStart](./visitparagraphstart/)(System::SharedPtr\<Aspose::Words::Paragraph\>) | Appelé lorsque l'énumération d'un paragraphe a commencé. |
| virtual [VisitRowEnd](./visitrowend/)(System::SharedPtr\<Aspose::Words::Tables::Row\>) | Appelé lorsque l'énumération d'une ligne de tableau est terminée. |
| virtual [VisitRowStart](./visitrowstart/)(System::SharedPtr\<Aspose::Words::Tables::Row\>) | Appelé lorsque l'énumération d'une ligne de tableau a commencé. |
| virtual [VisitRun](./visitrun/)(System::SharedPtr\<Aspose::Words::Run\>) | Appelé lorsqu'une séquence de texte est rencontrée. |
| virtual [VisitSectionEnd](./visitsectionend/)(System::SharedPtr\<Aspose::Words::Section\>) | Appelé lorsque l'énumération d'une section est terminée. |
| virtual [VisitSectionStart](./visitsectionstart/)(System::SharedPtr\<Aspose::Words::Section\>) | Appelé lorsque l'énumération d'une section a commencé. |
| virtual [VisitShapeEnd](./visitshapeend/)(System::SharedPtr\<Aspose::Words::Drawing::Shape\>) | Appelé lorsque l'énumération d'une forme est terminée. |
| virtual [VisitShapeStart](./visitshapestart/)(System::SharedPtr\<Aspose::Words::Drawing::Shape\>) | Appelé lorsque l'énumération d'une forme a commencé. |
| virtual [VisitSmartTagEnd](./visitsmarttagend/)(System::SharedPtr\<Aspose::Words::Markup::SmartTag\>) | Appelé lorsque l'énumération d'une balise intelligente est terminée. |
| virtual [VisitSmartTagStart](./visitsmarttagstart/)(System::SharedPtr\<Aspose::Words::Markup::SmartTag\>) | Appelé lorsque l'énumération d'une balise intelligente a commencé. |
| virtual [VisitSpecialChar](./visitspecialchar/)(System::SharedPtr\<Aspose::Words::SpecialChar\>) | Appelé lorsqu'un nœud [SpecialChar](../specialchar/) est rencontré dans le document. |
| virtual [VisitStructuredDocumentTagEnd](./visitstructureddocumenttagend/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>) | Appelé lorsque l'énumération d'une balise de document structuré est terminée. |
| virtual [VisitStructuredDocumentTagRangeEnd](./visitstructureddocumenttagrangeend/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTagRangeEnd\>) | Appelé lorsqu'un StructuredDocumentTagRangeEnd est rencontré. |
| virtual [VisitStructuredDocumentTagRangeStart](./visitstructureddocumenttagrangestart/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTagRangeStart\>) | Appelé lorsqu'un StructuredDocumentTagRangeStart est rencontré. |
| virtual [VisitStructuredDocumentTagStart](./visitstructureddocumenttagstart/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>) | Appelé lorsque l'énumération d'une balise de document structuré a commencé. |
| virtual [VisitSubDocument](./visitsubdocument/)(System::SharedPtr\<Aspose::Words::SubDocument\>) | Appelé lorsqu'un sous-document est rencontré. |
| virtual [VisitTableEnd](./visittableend/)(System::SharedPtr\<Aspose::Words::Tables::Table\>) | Appelé lorsque l'énumération d'un tableau est terminée. |
| virtual [VisitTableStart](./visittablestart/)(System::SharedPtr\<Aspose::Words::Tables::Table\>) | Appelé lorsque l'énumération d'un tableau a commencé. |
## Remarques


Avec [DocumentVisitor](./) vous pouvez définir et exécuter des opérations personnalisées qui nécessitent une énumération de l'arbre du document.

Par exemple, Aspose.Words utilise [DocumentVisitor](./) en interne pour enregistrer [Document](../document/) dans divers formats et pour d'autres opérations comme la recherche de champs ou de signets sur un fragment de document.

Pour utiliser [DocumentVisitor](./) :

1. Créez une classe dérivée de [DocumentVisitor](./).
1. Surchargez et fournissez des implémentations pour certaines ou toutes les méthodes VisitXXX afin d'effectuer des opérations personnalisées.
1. Appelez [Node.Accept](../node/accept/) sur le [Node](../node/) à partir duquel vous souhaitez démarrer l'énumération.



[DocumentVisitor](./) provides default implementations for all of the VisitXXX methods to make it easier to create new document visitors as only the methods required for the particular visitor need to be overridden. It is not necessary to override all of the visitor methods.

Pour plus d'informations, consultez le patron de conception Visitor.
## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
