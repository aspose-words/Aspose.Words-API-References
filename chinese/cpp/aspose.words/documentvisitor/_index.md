---
title: "Aspose::Words::DocumentVisitor class"
linktitle: "DocumentVisitor"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentVisitor 类。自定义文档访问器的基类。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 23000
url: /zh/cpp/aspose.words/documentvisitor/
---
## DocumentVisitor class


自定义文档访问器的基类。要了解更多信息，请访问 [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) 文档文章。

```cpp
class DocumentVisitor : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| virtual [VisitAbsolutePositionTab](./visitabsolutepositiontab/)(System::SharedPtr\<Aspose::Words::AbsolutePositionTab\>) | 当文档中遇到 [AbsolutePositionTab](../absolutepositiontab/) 节点时调用。 |
| virtual [VisitBodyEnd](./visitbodyend/)(System::SharedPtr\<Aspose::Words::Body\>) | 当章节中主文本故事的枚举结束时调用。 |
| virtual [VisitBodyStart](./visitbodystart/)(System::SharedPtr\<Aspose::Words::Body\>) | 当章节中主文本故事的枚举开始时调用。 |
| virtual [VisitBookmarkEnd](./visitbookmarkend/)(System::SharedPtr\<Aspose::Words::BookmarkEnd\>) | 当文档中遇到书签结束时调用。 |
| virtual [VisitBookmarkStart](./visitbookmarkstart/)(System::SharedPtr\<Aspose::Words::BookmarkStart\>) | 当文档中遇到书签开始时调用。 |
| virtual [VisitBuildingBlockEnd](./visitbuildingblockend/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::BuildingBlock\>) | 当构建块的枚举结束时调用。 |
| virtual [VisitBuildingBlockStart](./visitbuildingblockstart/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::BuildingBlock\>) | 当构建块的枚举开始时调用。 |
| virtual [VisitCellEnd](./visitcellend/)(System::SharedPtr\<Aspose::Words::Tables::Cell\>) | 当表格单元格的枚举结束时调用。 |
| virtual [VisitCellStart](./visitcellstart/)(System::SharedPtr\<Aspose::Words::Tables::Cell\>) | 当表格单元格的枚举开始时调用。 |
| virtual [VisitCommentEnd](./visitcommentend/)(System::SharedPtr\<Aspose::Words::Comment\>) | 当注释文本的枚举结束时调用。 |
| virtual [VisitCommentRangeEnd](./visitcommentrangeend/)(System::SharedPtr\<Aspose::Words::CommentRangeEnd\>) | 当遇到注释文本范围的结束时调用。 |
| virtual [VisitCommentRangeStart](./visitcommentrangestart/)(System::SharedPtr\<Aspose::Words::CommentRangeStart\>) | 当遇到注释文本范围的开始时调用。 |
| virtual [VisitCommentStart](./visitcommentstart/)(System::SharedPtr\<Aspose::Words::Comment\>) | 当注释文本的枚举开始时调用。 |
| virtual [VisitDocumentEnd](./visitdocumentend/)(System::SharedPtr\<Aspose::Words::Document\>) | 当文档的枚举完成时调用。 |
| virtual [VisitDocumentStart](./visitdocumentstart/)(System::SharedPtr\<Aspose::Words::Document\>) | 当文档的枚举开始时调用。 |
| virtual [VisitEditableRangeEnd](./visiteditablerangeend/)(System::SharedPtr\<Aspose::Words::EditableRangeEnd\>) | 当在文档中遇到可编辑范围的结束时调用。 |
| virtual [VisitEditableRangeStart](./visiteditablerangestart/)(System::SharedPtr\<Aspose::Words::EditableRangeStart\>) | 当在文档中遇到可编辑范围的开始时调用。 |
| virtual [VisitFieldEnd](./visitfieldend/)(System::SharedPtr\<Aspose::Words::Fields::FieldEnd\>) | 当文档中的字段结束时调用。 |
| virtual [VisitFieldSeparator](./visitfieldseparator/)(System::SharedPtr\<Aspose::Words::Fields::FieldSeparator\>) | 当文档中遇到字段分隔符时调用。 |
| virtual [VisitFieldStart](./visitfieldstart/)(System::SharedPtr\<Aspose::Words::Fields::FieldStart\>) | 当文档中的字段开始时调用。 |
| virtual [VisitFootnoteEnd](./visitfootnoteend/)(System::SharedPtr\<Aspose::Words::Notes::Footnote\>) | 当脚注或尾注文本的枚举结束时调用。 |
| virtual [VisitFootnoteStart](./visitfootnotestart/)(System::SharedPtr\<Aspose::Words::Notes::Footnote\>) | 当脚注或尾注文本的枚举开始时调用。 |
| virtual [VisitFormField](./visitformfield/)(System::SharedPtr\<Aspose::Words::Fields::FormField\>) | 当在文档中遇到表单字段时调用。 |
| virtual [VisitGlossaryDocumentEnd](./visitglossarydocumentend/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>) | 当词汇表文档的枚举结束时调用。 |
| virtual [VisitGlossaryDocumentStart](./visitglossarydocumentstart/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>) | 当词汇表文档的枚举开始时调用。 |
| virtual [VisitGroupShapeEnd](./visitgroupshapeend/)(System::SharedPtr\<Aspose::Words::Drawing::GroupShape\>) | 当组合形状的枚举结束时调用。 |
| virtual [VisitGroupShapeStart](./visitgroupshapestart/)(System::SharedPtr\<Aspose::Words::Drawing::GroupShape\>) | 当组合形状的枚举开始时调用。 |
| virtual [VisitHeaderFooterEnd](./visitheaderfooterend/)(System::SharedPtr\<Aspose::Words::HeaderFooter\>) | 当节中页眉或页脚的枚举结束时调用。 |
| virtual [VisitHeaderFooterStart](./visitheaderfooterstart/)(System::SharedPtr\<Aspose::Words::HeaderFooter\>) | 当节中页眉或页脚的枚举开始时调用。 |
| virtual [VisitOfficeMathEnd](./visitofficemathend/)(System::SharedPtr\<Aspose::Words::Math::OfficeMath\>) | 当 Office [Math](../../aspose.words.math/) 对象的枚举结束时调用。 |
| virtual [VisitOfficeMathStart](./visitofficemathstart/)(System::SharedPtr\<Aspose::Words::Math::OfficeMath\>) | 当开始枚举 Office [Math](../../aspose.words.math/) 对象时调用。 |
| virtual [VisitParagraphEnd](./visitparagraphend/)(System::SharedPtr\<Aspose::Words::Paragraph\>) | 当段落枚举结束时调用。 |
| virtual [VisitParagraphStart](./visitparagraphstart/)(System::SharedPtr\<Aspose::Words::Paragraph\>) | 当段落枚举开始时调用。 |
| virtual [VisitRowEnd](./visitrowend/)(System::SharedPtr\<Aspose::Words::Tables::Row\>) | 当表格行枚举结束时调用。 |
| virtual [VisitRowStart](./visitrowstart/)(System::SharedPtr\<Aspose::Words::Tables::Row\>) | 当表格行枚举开始时调用。 |
| virtual [VisitRun](./visitrun/)(System::SharedPtr\<Aspose::Words::Run\>) | 当遇到文本运行时调用。 |
| virtual [VisitSectionEnd](./visitsectionend/)(System::SharedPtr\<Aspose::Words::Section\>) | 当章节枚举结束时调用。 |
| virtual [VisitSectionStart](./visitsectionstart/)(System::SharedPtr\<Aspose::Words::Section\>) | 当章节枚举开始时调用。 |
| virtual [VisitShapeEnd](./visitshapeend/)(System::SharedPtr\<Aspose::Words::Drawing::Shape\>) | 当形状枚举结束时调用。 |
| virtual [VisitShapeStart](./visitshapestart/)(System::SharedPtr\<Aspose::Words::Drawing::Shape\>) | 当形状枚举开始时调用。 |
| virtual [VisitSmartTagEnd](./visitsmarttagend/)(System::SharedPtr\<Aspose::Words::Markup::SmartTag\>) | 当智能标签枚举结束时调用。 |
| virtual [VisitSmartTagStart](./visitsmarttagstart/)(System::SharedPtr\<Aspose::Words::Markup::SmartTag\>) | 当智能标签枚举开始时调用。 |
| virtual [VisitSpecialChar](./visitspecialchar/)(System::SharedPtr\<Aspose::Words::SpecialChar\>) | 当在文档中遇到 [SpecialChar](../specialchar/) 节点时调用。 |
| virtual [VisitStructuredDocumentTagEnd](./visitstructureddocumenttagend/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>) | 当结构化文档标签枚举结束时调用。 |
| virtual [VisitStructuredDocumentTagRangeEnd](./visitstructureddocumenttagrangeend/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTagRangeEnd\>) | 当遇到 StructuredDocumentTagRangeEnd 时调用。 |
| virtual [VisitStructuredDocumentTagRangeStart](./visitstructureddocumenttagrangestart/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTagRangeStart\>) | 当遇到 StructuredDocumentTagRangeStart 时调用。 |
| virtual [VisitStructuredDocumentTagStart](./visitstructureddocumenttagstart/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>) | 当结构化文档标签枚举开始时调用。 |
| virtual [VisitSubDocument](./visitsubdocument/)(System::SharedPtr\<Aspose::Words::SubDocument\>) | 当遇到子文档时调用。 |
| virtual [VisitTableEnd](./visittableend/)(System::SharedPtr\<Aspose::Words::Tables::Table\>) | 当表格枚举结束时调用。 |
| virtual [VisitTableStart](./visittablestart/)(System::SharedPtr\<Aspose::Words::Tables::Table\>) | 当表格枚举开始时调用。 |
## 备注


使用 [DocumentVisitor](./) 您可以定义并执行需要对文档树进行枚举的自定义操作。

例如，Aspose.Words 在内部使用 [DocumentVisitor](./) 来保存 [Document](../document/) 为各种格式，并执行其他操作，如在文档片段中查找字段或书签。

要使用 [DocumentVisitor](./)：

1. 创建一个从 [DocumentVisitor](./) 派生的类。
1. 重写并为部分或全部 VisitXXX 方法提供实现，以执行一些自定义操作。
1. 调用您想要开始枚举的 [Node](../node/) 上的 [Node.Accept](../node/accept/) 方法。



[DocumentVisitor](./) provides default implementations for all of the VisitXXX methods to make it easier to create new document visitors as only the methods required for the particular visitor need to be overridden. It is not necessary to override all of the visitor methods.

欲了解更多信息，请参阅 Visitor 设计模式。
## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
