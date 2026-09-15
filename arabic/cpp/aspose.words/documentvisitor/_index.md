---
title: "Aspose::Words::DocumentVisitor فئة"
linktitle: "DocumentVisitor"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DocumentVisitor فئة. الفئة الأساسية لزوار المستندات المخصصين. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 23000
url: /ar/cpp/aspose.words/documentvisitor/
---
## DocumentVisitor class


الفئة الأساسية لزوار المستند المخصصين. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class DocumentVisitor : public virtual System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| virtual [VisitAbsolutePositionTab](./visitabsolutepositiontab/)(System::SharedPtr\<Aspose::Words::AbsolutePositionTab\>) | يتم الاستدعاء عندما يتم العثور على عقدة [AbsolutePositionTab](../absolutepositiontab/) في المستند. |
| virtual [VisitBodyEnd](./visitbodyend/)(System::SharedPtr\<Aspose::Words::Body\>) | يتم الاستدعاء عندما ينتهي تعداد قصة النص الرئيسي في قسم. |
| virtual [VisitBodyStart](./visitbodystart/)(System::SharedPtr\<Aspose::Words::Body\>) | يتم الاستدعاء عندما يبدأ تعداد قصة النص الرئيسي في قسم. |
| virtual [VisitBookmarkEnd](./visitbookmarkend/)(System::SharedPtr\<Aspose::Words::BookmarkEnd\>) | يتم الاستدعاء عندما يتم العثور على نهاية إشارة مرجعية في المستند. |
| virtual [VisitBookmarkStart](./visitbookmarkstart/)(System::SharedPtr\<Aspose::Words::BookmarkStart\>) | يتم الاستدعاء عندما يتم العثور على بداية إشارة مرجعية في المستند. |
| virtual [VisitBuildingBlockEnd](./visitbuildingblockend/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::BuildingBlock\>) | يتم الاستدعاء عندما ينتهي تعداد كتلة بناء. |
| virtual [VisitBuildingBlockStart](./visitbuildingblockstart/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::BuildingBlock\>) | يتم الاستدعاء عندما يبدأ تعداد كتلة بناء. |
| virtual [VisitCellEnd](./visitcellend/)(System::SharedPtr\<Aspose::Words::Tables::Cell\>) | يتم الاستدعاء عندما ينتهي تعداد خلية جدول. |
| virtual [VisitCellStart](./visitcellstart/)(System::SharedPtr\<Aspose::Words::Tables::Cell\>) | يتم الاستدعاء عندما يبدأ تعداد خلية جدول. |
| virtual [VisitCommentEnd](./visitcommentend/)(System::SharedPtr\<Aspose::Words::Comment\>) | يتم الاستدعاء عندما ينتهي تعداد نص تعليق. |
| virtual [VisitCommentRangeEnd](./visitcommentrangeend/)(System::SharedPtr\<Aspose::Words::CommentRangeEnd\>) | يتم الاستدعاء عندما يتم العثور على نهاية نطاق نص معلق. |
| virtual [VisitCommentRangeStart](./visitcommentrangestart/)(System::SharedPtr\<Aspose::Words::CommentRangeStart\>) | يتم الاستدعاء عندما يتم العثور على بداية نطاق نص معلق. |
| virtual [VisitCommentStart](./visitcommentstart/)(System::SharedPtr\<Aspose::Words::Comment\>) | يتم الاستدعاء عندما يبدأ تعداد نص تعليق. |
| virtual [VisitDocumentEnd](./visitdocumentend/)(System::SharedPtr\<Aspose::Words::Document\>) | يتم الاستدعاء عندما ينتهي تعداد المستند. |
| virtual [VisitDocumentStart](./visitdocumentstart/)(System::SharedPtr\<Aspose::Words::Document\>) | يتم الاستدعاء عندما يبدأ تعداد المستند. |
| virtual [VisitEditableRangeEnd](./visiteditablerangeend/)(System::SharedPtr\<Aspose::Words::EditableRangeEnd\>) | يتم الاستدعاء عندما يتم العثور على نهاية نطاق قابل للتحرير في المستند. |
| virtual [VisitEditableRangeStart](./visiteditablerangestart/)(System::SharedPtr\<Aspose::Words::EditableRangeStart\>) | يتم الاستدعاء عندما يتم العثور على بداية نطاق قابل للتحرير في المستند. |
| virtual [VisitFieldEnd](./visitfieldend/)(System::SharedPtr\<Aspose::Words::Fields::FieldEnd\>) | يتم الاستدعاء عندما ينتهي حقل في المستند. |
| virtual [VisitFieldSeparator](./visitfieldseparator/)(System::SharedPtr\<Aspose::Words::Fields::FieldSeparator\>) | يتم استدعاؤه عندما يتم العثور على فاصل حقل في المستند. |
| virtual [VisitFieldStart](./visitfieldstart/)(System::SharedPtr\<Aspose::Words::Fields::FieldStart\>) | يتم استدعاؤه عندما يبدأ حقل في المستند. |
| virtual [VisitFootnoteEnd](./visitfootnoteend/)(System::SharedPtr\<Aspose::Words::Notes::Footnote\>) | يتم استدعاؤه عندما ينتهي تعداد نص الحاشية السفلية أو الحاشية الختامية. |
| virtual [VisitFootnoteStart](./visitfootnotestart/)(System::SharedPtr\<Aspose::Words::Notes::Footnote\>) | يتم استدعاؤه عندما يبدأ تعداد نص الحاشية السفلية أو الحاشية الختامية. |
| virtual [VisitFormField](./visitformfield/)(System::SharedPtr\<Aspose::Words::Fields::FormField\>) | يتم استدعاؤه عندما يتم العثور على حقل نموذج في المستند. |
| virtual [VisitGlossaryDocumentEnd](./visitglossarydocumentend/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>) | يتم استدعاؤه عندما ينتهي تعداد مستند المسرد. |
| virtual [VisitGlossaryDocumentStart](./visitglossarydocumentstart/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>) | يتم استدعاؤه عندما يبدأ تعداد مستند المسرد. |
| virtual [VisitGroupShapeEnd](./visitgroupshapeend/)(System::SharedPtr\<Aspose::Words::Drawing::GroupShape\>) | يتم استدعاؤه عندما ينتهي تعداد شكل مجموعة. |
| virtual [VisitGroupShapeStart](./visitgroupshapestart/)(System::SharedPtr\<Aspose::Words::Drawing::GroupShape\>) | يتم استدعاؤه عندما يبدأ تعداد شكل مجموعة. |
| virtual [VisitHeaderFooterEnd](./visitheaderfooterend/)(System::SharedPtr\<Aspose::Words::HeaderFooter\>) | يتم استدعاؤه عندما ينتهي تعداد رأس أو تذييل في قسم. |
| virtual [VisitHeaderFooterStart](./visitheaderfooterstart/)(System::SharedPtr\<Aspose::Words::HeaderFooter\>) | يتم استدعاؤه عندما يبدأ تعداد رأس أو تذييل في قسم. |
| virtual [VisitOfficeMathEnd](./visitofficemathend/)(System::SharedPtr\<Aspose::Words::Math::OfficeMath\>) | يتم استدعاؤه عندما ينتهي تعداد كائن Office [Math](../../aspose.words.math/). |
| virtual [VisitOfficeMathStart](./visitofficemathstart/)(System::SharedPtr\<Aspose::Words::Math::OfficeMath\>) | يتم استدعاؤه عندما يبدأ تعداد كائن Office [Math](../../aspose.words.math/). |
| virtual [VisitParagraphEnd](./visitparagraphend/)(System::SharedPtr\<Aspose::Words::Paragraph\>) | يتم استدعاؤه عندما ينتهي تعداد فقرة. |
| virtual [VisitParagraphStart](./visitparagraphstart/)(System::SharedPtr\<Aspose::Words::Paragraph\>) | يتم استدعاؤه عندما يبدأ تعداد فقرة. |
| virtual [VisitRowEnd](./visitrowend/)(System::SharedPtr\<Aspose::Words::Tables::Row\>) | يتم استدعاؤه عندما ينتهي تعداد صف جدول. |
| virtual [VisitRowStart](./visitrowstart/)(System::SharedPtr\<Aspose::Words::Tables::Row\>) | يتم استدعاؤه عندما يبدأ تعداد صف جدول. |
| virtual [VisitRun](./visitrun/)(System::SharedPtr\<Aspose::Words::Run\>) | يتم استدعاؤه عندما يتم العثور على مجموعة نص في الـ. |
| virtual [VisitSectionEnd](./visitsectionend/)(System::SharedPtr\<Aspose::Words::Section\>) | يتم استدعاؤه عندما ينتهي تعداد قسم. |
| virtual [VisitSectionStart](./visitsectionstart/)(System::SharedPtr\<Aspose::Words::Section\>) | يتم استدعاؤه عندما يبدأ تعداد قسم. |
| virtual [VisitShapeEnd](./visitshapeend/)(System::SharedPtr\<Aspose::Words::Drawing::Shape\>) | يتم استدعاؤه عندما ينتهي تعداد شكل. |
| virtual [VisitShapeStart](./visitshapestart/)(System::SharedPtr\<Aspose::Words::Drawing::Shape\>) | يتم استدعاؤه عندما يبدأ تعداد شكل. |
| virtual [VisitSmartTagEnd](./visitsmarttagend/)(System::SharedPtr\<Aspose::Words::Markup::SmartTag\>) | يتم استدعاؤه عندما ينتهي تعداد علامة ذكية. |
| virtual [VisitSmartTagStart](./visitsmarttagstart/)(System::SharedPtr\<Aspose::Words::Markup::SmartTag\>) | يتم استدعاؤه عندما يبدأ تعداد علامة ذكية. |
| virtual [VisitSpecialChar](./visitspecialchar/)(System::SharedPtr\<Aspose::Words::SpecialChar\>) | يتم استدعاؤه عندما يتم العثور على عقدة [SpecialChar](../specialchar/) في المستند. |
| virtual [VisitStructuredDocumentTagEnd](./visitstructureddocumenttagend/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>) | يتم استدعاؤه عندما ينتهي تعداد علامة مستند منسقة. |
| virtual [VisitStructuredDocumentTagRangeEnd](./visitstructureddocumenttagrangeend/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTagRangeEnd\>) | يتم استدعاؤه عند مواجهة StructuredDocumentTagRangeEnd. |
| virtual [VisitStructuredDocumentTagRangeStart](./visitstructureddocumenttagrangestart/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTagRangeStart\>) | يتم استدعاؤه عند مواجهة StructuredDocumentTagRangeStart. |
| virtual [VisitStructuredDocumentTagStart](./visitstructureddocumenttagstart/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>) | يتم استدعاؤه عندما يبدأ تعداد علامة مستند منسقة. |
| virtual [VisitSubDocument](./visitsubdocument/)(System::SharedPtr\<Aspose::Words::SubDocument\>) | يتم استدعاؤه عند مواجهة مستند فرعي. |
| virtual [VisitTableEnd](./visittableend/)(System::SharedPtr\<Aspose::Words::Tables::Table\>) | يتم استدعاؤه عندما ينتهي تعداد جدول. |
| virtual [VisitTableStart](./visittablestart/)(System::SharedPtr\<Aspose::Words::Tables::Table\>) | يتم استدعاؤه عندما يبدأ تعداد جدول. |
## ملاحظات


مع [DocumentVisitor](./) يمكنك تعريف وتنفيذ عمليات مخصصة تتطلب تعداد شجرة المستند.

على سبيل المثال، يستخدم Aspose.Words [DocumentVisitor](./) داخليًا لحفظ [Document](../document/) بصيغ مختلفة ولعمليات أخرى مثل العثور على الحقول أو الإشارات المرجعية ضمن جزء من المستند.

لاستخدام [DocumentVisitor](./):

1. أنشئ فئة مشتقة من [DocumentVisitor](./).
1. قم بإعادة تعريف وتوفير تنفيذ لبعض أو جميع طرق VisitXXX لتنفيذ بعض العمليات المخصصة.
1. استدعِ [Node.Accept](../node/accept/) على الـ [Node](../node/) الذي تريد بدء التعداد منه.



[DocumentVisitor](./) provides default implementations for all of the VisitXXX methods to make it easier to create new document visitors as only the methods required for the particular visitor need to be overridden. It is not necessary to override all of the visitor methods.

لمزيد من المعلومات، راجع نمط التصميم Visitor.
## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
