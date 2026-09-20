---
title: "Aspose::Words::DocumentVisitor класс"
linktitle: "DocumentVisitor"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentVisitor класс. Базовый класс для пользовательских посетителей документов. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 23000
url: /ru/cpp/aspose.words/documentvisitor/
---
## DocumentVisitor class


Базовый класс для пользовательских посетителей документа. Чтобы узнать больше, посетите статью документации [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class DocumentVisitor : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| virtual [VisitAbsolutePositionTab](./visitabsolutepositiontab/)(System::SharedPtr\<Aspose::Words::AbsolutePositionTab\>) | Вызывается, когда в документе встречается узел [AbsolutePositionTab](../absolutepositiontab/). |
| virtual [VisitBodyEnd](./visitbodyend/)(System::SharedPtr\<Aspose::Words::Body\>) | Вызывается, когда перечисление основной текстовой истории в разделе завершилось. |
| virtual [VisitBodyStart](./visitbodystart/)(System::SharedPtr\<Aspose::Words::Body\>) | Вызывается, когда перечисление основной текстовой истории в разделе началось. |
| virtual [VisitBookmarkEnd](./visitbookmarkend/)(System::SharedPtr\<Aspose::Words::BookmarkEnd\>) | Вызывается, когда в документе встречается конец закладки. |
| virtual [VisitBookmarkStart](./visitbookmarkstart/)(System::SharedPtr\<Aspose::Words::BookmarkStart\>) | Вызывается, когда в документе встречается начало закладки. |
| virtual [VisitBuildingBlockEnd](./visitbuildingblockend/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::BuildingBlock\>) | Вызывается, когда перечисление строительного блока завершилось. |
| virtual [VisitBuildingBlockStart](./visitbuildingblockstart/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::BuildingBlock\>) | Вызывается, когда перечисление строительного блока началось. |
| virtual [VisitCellEnd](./visitcellend/)(System::SharedPtr\<Aspose::Words::Tables::Cell\>) | Вызывается, когда перечисление ячейки таблицы завершилось. |
| virtual [VisitCellStart](./visitcellstart/)(System::SharedPtr\<Aspose::Words::Tables::Cell\>) | Вызывается, когда перечисление ячейки таблицы началось. |
| virtual [VisitCommentEnd](./visitcommentend/)(System::SharedPtr\<Aspose::Words::Comment\>) | Вызывается, когда перечисление текста комментария завершилось. |
| virtual [VisitCommentRangeEnd](./visitcommentrangeend/)(System::SharedPtr\<Aspose::Words::CommentRangeEnd\>) | Вызывается, когда встречается конец комментируемого диапазона текста. |
| virtual [VisitCommentRangeStart](./visitcommentrangestart/)(System::SharedPtr\<Aspose::Words::CommentRangeStart\>) | Вызывается, когда встречается начало комментируемого диапазона текста. |
| virtual [VisitCommentStart](./visitcommentstart/)(System::SharedPtr\<Aspose::Words::Comment\>) | Вызывается, когда перечисление текста комментария началось. |
| virtual [VisitDocumentEnd](./visitdocumentend/)(System::SharedPtr\<Aspose::Words::Document\>) | Вызывается, когда перечисление документа завершилось. |
| virtual [VisitDocumentStart](./visitdocumentstart/)(System::SharedPtr\<Aspose::Words::Document\>) | Вызывается, когда перечисление документа началось. |
| virtual [VisitEditableRangeEnd](./visiteditablerangeend/)(System::SharedPtr\<Aspose::Words::EditableRangeEnd\>) | Вызывается, когда в документе встречается конец редактируемого диапазона. |
| virtual [VisitEditableRangeStart](./visiteditablerangestart/)(System::SharedPtr\<Aspose::Words::EditableRangeStart\>) | Вызывается, когда в документе встречается начало редактируемого диапазона. |
| virtual [VisitFieldEnd](./visitfieldend/)(System::SharedPtr\<Aspose::Words::Fields::FieldEnd\>) | Вызывается, когда в документе заканчивается поле. |
| virtual [VisitFieldSeparator](./visitfieldseparator/)(System::SharedPtr\<Aspose::Words::Fields::FieldSeparator\>) | Вызывается, когда в документе встречается разделитель полей. |
| virtual [VisitFieldStart](./visitfieldstart/)(System::SharedPtr\<Aspose::Words::Fields::FieldStart\>) | Вызывается, когда в документе начинается поле. |
| virtual [VisitFootnoteEnd](./visitfootnoteend/)(System::SharedPtr\<Aspose::Words::Notes::Footnote\>) | Вызывается, когда перечисление текста сноски или концевой сноски завершилось. |
| virtual [VisitFootnoteStart](./visitfootnotestart/)(System::SharedPtr\<Aspose::Words::Notes::Footnote\>) | Вызывается, когда начинается перечисление текста сноски или концевой сноски. |
| virtual [VisitFormField](./visitformfield/)(System::SharedPtr\<Aspose::Words::Fields::FormField\>) | Вызывается, когда в документе встречается поле формы. |
| virtual [VisitGlossaryDocumentEnd](./visitglossarydocumentend/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>) | Вызывается, когда перечисление глоссарного документа завершилось. |
| virtual [VisitGlossaryDocumentStart](./visitglossarydocumentstart/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>) | Вызывается, когда начинается перечисление глоссарного документа. |
| virtual [VisitGroupShapeEnd](./visitgroupshapeend/)(System::SharedPtr\<Aspose::Words::Drawing::GroupShape\>) | Вызывается, когда перечисление групповой фигуры завершилось. |
| virtual [VisitGroupShapeStart](./visitgroupshapestart/)(System::SharedPtr\<Aspose::Words::Drawing::GroupShape\>) | Вызывается, когда начинается перечисление групповой фигуры. |
| virtual [VisitHeaderFooterEnd](./visitheaderfooterend/)(System::SharedPtr\<Aspose::Words::HeaderFooter\>) | Вызывается, когда перечисление верхнего или нижнего колонтитула в разделе завершилось. |
| virtual [VisitHeaderFooterStart](./visitheaderfooterstart/)(System::SharedPtr\<Aspose::Words::HeaderFooter\>) | Вызывается, когда начинается перечисление верхнего или нижнего колонтитула в разделе. |
| virtual [VisitOfficeMathEnd](./visitofficemathend/)(System::SharedPtr\<Aspose::Words::Math::OfficeMath\>) | Вызывается, когда перечисление объекта Office [Math](../../aspose.words.math/) завершилось. |
| virtual [VisitOfficeMathStart](./visitofficemathstart/)(System::SharedPtr\<Aspose::Words::Math::OfficeMath\>) | Вызывается, когда начинается перечисление объекта Office [Math](../../aspose.words.math/). |
| virtual [VisitParagraphEnd](./visitparagraphend/)(System::SharedPtr\<Aspose::Words::Paragraph\>) | Вызывается, когда перечисление абзаца завершилось. |
| virtual [VisitParagraphStart](./visitparagraphstart/)(System::SharedPtr\<Aspose::Words::Paragraph\>) | Вызывается, когда начинается перечисление абзаца. |
| virtual [VisitRowEnd](./visitrowend/)(System::SharedPtr\<Aspose::Words::Tables::Row\>) | Вызывается, когда перечисление строки таблицы завершилось. |
| virtual [VisitRowStart](./visitrowstart/)(System::SharedPtr\<Aspose::Words::Tables::Row\>) | Вызывается, когда начинается перечисление строки таблицы. |
| virtual [VisitRun](./visitrun/)(System::SharedPtr\<Aspose::Words::Run\>) | Вызывается, когда в документе встречается последовательность текста. |
| virtual [VisitSectionEnd](./visitsectionend/)(System::SharedPtr\<Aspose::Words::Section\>) | Вызывается, когда перечисление раздела завершилось. |
| virtual [VisitSectionStart](./visitsectionstart/)(System::SharedPtr\<Aspose::Words::Section\>) | Вызывается, когда начинается перечисление раздела. |
| virtual [VisitShapeEnd](./visitshapeend/)(System::SharedPtr\<Aspose::Words::Drawing::Shape\>) | Вызывается, когда перечисление фигуры завершилось. |
| virtual [VisitShapeStart](./visitshapestart/)(System::SharedPtr\<Aspose::Words::Drawing::Shape\>) | Вызывается, когда начинается перечисление фигуры. |
| virtual [VisitSmartTagEnd](./visitsmarttagend/)(System::SharedPtr\<Aspose::Words::Markup::SmartTag\>) | Вызывается, когда перечисление смарт‑тега завершилось. |
| virtual [VisitSmartTagStart](./visitsmarttagstart/)(System::SharedPtr\<Aspose::Words::Markup::SmartTag\>) | Вызывается, когда начинается перечисление смарт‑тега. |
| virtual [VisitSpecialChar](./visitspecialchar/)(System::SharedPtr\<Aspose::Words::SpecialChar\>) | Вызывается, когда в документе встречается узел [SpecialChar](../specialchar/). |
| virtual [VisitStructuredDocumentTagEnd](./visitstructureddocumenttagend/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>) | Вызывается, когда перечисление структурного тега документа завершено. |
| virtual [VisitStructuredDocumentTagRangeEnd](./visitstructureddocumenttagrangeend/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTagRangeEnd\>) | Вызывается, когда встречается StructuredDocumentTagRangeEnd. |
| virtual [VisitStructuredDocumentTagRangeStart](./visitstructureddocumenttagrangestart/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTagRangeStart\>) | Вызывается, когда встречается StructuredDocumentTagRangeStart. |
| virtual [VisitStructuredDocumentTagStart](./visitstructureddocumenttagstart/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>) | Вызывается, когда началось перечисление структурного тега документа. |
| virtual [VisitSubDocument](./visitsubdocument/)(System::SharedPtr\<Aspose::Words::SubDocument\>) | Вызывается, когда обнаруживается вложенный документ. |
| virtual [VisitTableEnd](./visittableend/)(System::SharedPtr\<Aspose::Words::Tables::Table\>) | Вызывается, когда перечисление таблицы завершено. |
| virtual [VisitTableStart](./visittablestart/)(System::SharedPtr\<Aspose::Words::Tables::Table\>) | Вызывается, когда началось перечисление таблицы. |
## Примечания


С помощью [DocumentVisitor](./) вы можете определять и выполнять пользовательские операции, требующие перечисления дерева документа.

Например, Aspose.Words использует [DocumentVisitor](./) внутри для сохранения [Document](../document/) в различных форматах и для других операций, таких как поиск полей или закладок в фрагменте документа.

Чтобы использовать [DocumentVisitor](./):

1. Создайте класс, наследующийся от [DocumentVisitor](./).
1. Переопределите и предоставьте реализации некоторых или всех методов VisitXXX для выполнения пользовательских операций.
1. Вызовите [Node.Accept](../node/accept/) у [Node](../node/), с которого вы хотите начать перечисление.



[DocumentVisitor](./) provides default implementations for all of the VisitXXX methods to make it easier to create new document visitors as only the methods required for the particular visitor need to be overridden. It is not necessary to override all of the visitor methods.

Для получения дополнительной информации см. шаблон проектирования Visitor.
## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
