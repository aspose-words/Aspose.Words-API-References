---
title: "Aspose::Words::DocumentVisitor sınıfı"
linktitle: "DocumentVisitor"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentVisitor sınıfı. Özel belge ziyaretçileri için temel sınıf. Daha fazla bilgi için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 23000
url: /tr/cpp/aspose.words/documentvisitor/
---
## DocumentVisitor class


Özel belge ziyaretçileri için temel sınıftır. Daha fazla bilgi edinmek için [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) dokümantasyon makalesini ziyaret edin.

```cpp
class DocumentVisitor : public virtual System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| virtual [VisitAbsolutePositionTab](./visitabsolutepositiontab/)(System::SharedPtr\<Aspose::Words::AbsolutePositionTab\>) | Belgede bir [AbsolutePositionTab](../absolutepositiontab/) düğümüyle karşılaşıldığında çağrılır. |
| virtual [VisitBodyEnd](./visitbodyend/)(System::SharedPtr\<Aspose::Words::Body\>) | Bir bölümdeki ana metin hikayesinin sayımı bittiğinde çağrılır. |
| virtual [VisitBodyStart](./visitbodystart/)(System::SharedPtr\<Aspose::Words::Body\>) | Bir bölümdeki ana metin hikayesinin sayımı başladığında çağrılır. |
| virtual [VisitBookmarkEnd](./visitbookmarkend/)(System::SharedPtr\<Aspose::Words::BookmarkEnd\>) | Belgede bir yer iminin sonuyla karşılaşıldığında çağrılır. |
| virtual [VisitBookmarkStart](./visitbookmarkstart/)(System::SharedPtr\<Aspose::Words::BookmarkStart\>) | Belgede bir yer iminin başlangıcıyla karşılaşıldığında çağrılır. |
| virtual [VisitBuildingBlockEnd](./visitbuildingblockend/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::BuildingBlock\>) | Bir yapı bloğunun sayımı bittiğinde çağrılır. |
| virtual [VisitBuildingBlockStart](./visitbuildingblockstart/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::BuildingBlock\>) | Bir yapı bloğunun sayımı başladığında çağrılır. |
| virtual [VisitCellEnd](./visitcellend/)(System::SharedPtr\<Aspose::Words::Tables::Cell\>) | Bir tablo hücresinin sayımı bittiğinde çağrılır. |
| virtual [VisitCellStart](./visitcellstart/)(System::SharedPtr\<Aspose::Words::Tables::Cell\>) | Bir tablo hücresinin sayımı başladığında çağrılır. |
| virtual [VisitCommentEnd](./visitcommentend/)(System::SharedPtr\<Aspose::Words::Comment\>) | Bir yorum metninin sayımı bittiğinde çağrılır. |
| virtual [VisitCommentRangeEnd](./visitcommentrangeend/)(System::SharedPtr\<Aspose::Words::CommentRangeEnd\>) | Yorumlanmış bir metin aralığının sonuyla karşılaşıldığında çağrılır. |
| virtual [VisitCommentRangeStart](./visitcommentrangestart/)(System::SharedPtr\<Aspose::Words::CommentRangeStart\>) | Yorumlanmış bir metin aralığının başlangıcıyla karşılaşıldığında çağrılır. |
| virtual [VisitCommentStart](./visitcommentstart/)(System::SharedPtr\<Aspose::Words::Comment\>) | Bir yorum metninin sayımı başladığında çağrılır. |
| virtual [VisitDocumentEnd](./visitdocumentend/)(System::SharedPtr\<Aspose::Words::Document\>) | Belgenin sayımı tamamlandığında çağrılır. |
| virtual [VisitDocumentStart](./visitdocumentstart/)(System::SharedPtr\<Aspose::Words::Document\>) | Belgenin sayımı başladığında çağrılır. |
| virtual [VisitEditableRangeEnd](./visiteditablerangeend/)(System::SharedPtr\<Aspose::Words::EditableRangeEnd\>) | Belgede düzenlenebilir bir aralığın sonuyla karşılaşıldığında çağrılır. |
| virtual [VisitEditableRangeStart](./visiteditablerangestart/)(System::SharedPtr\<Aspose::Words::EditableRangeStart\>) | Belgede düzenlenebilir bir aralığın başlangıcıyla karşılaşıldığında çağrılır. |
| virtual [VisitFieldEnd](./visitfieldend/)(System::SharedPtr\<Aspose::Words::Fields::FieldEnd\>) | Belgede bir alan bittiğinde çağrılır. |
| virtual [VisitFieldSeparator](./visitfieldseparator/)(System::SharedPtr\<Aspose::Words::Fields::FieldSeparator\>) | Belge içinde bir alan ayırıcıyla karşılaşıldığında çağrılır. |
| virtual [VisitFieldStart](./visitfieldstart/)(System::SharedPtr\<Aspose::Words::Fields::FieldStart\>) | Belge içinde bir alan başladığında çağrılır. |
| virtual [VisitFootnoteEnd](./visitfootnoteend/)(System::SharedPtr\<Aspose::Words::Notes::Footnote\>) | Dipnot veya sonnot metninin numaralandırması bittiğinde çağrılır. |
| virtual [VisitFootnoteStart](./visitfootnotestart/)(System::SharedPtr\<Aspose::Words::Notes::Footnote\>) | Dipnot veya sonnot metninin numaralandırması başladığında çağrılır. |
| virtual [VisitFormField](./visitformfield/)(System::SharedPtr\<Aspose::Words::Fields::FormField\>) | Belge içinde bir form alanıyla karşılaşıldığında çağrılır. |
| virtual [VisitGlossaryDocumentEnd](./visitglossarydocumentend/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>) | Sözlük belgesinin numaralandırması bittiğinde çağrılır. |
| virtual [VisitGlossaryDocumentStart](./visitglossarydocumentstart/)(System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>) | Sözlük belgesinin numaralandırması başladığında çağrılır. |
| virtual [VisitGroupShapeEnd](./visitgroupshapeend/)(System::SharedPtr\<Aspose::Words::Drawing::GroupShape\>) | Grup şeklinin numaralandırması bittiğinde çağrılır. |
| virtual [VisitGroupShapeStart](./visitgroupshapestart/)(System::SharedPtr\<Aspose::Words::Drawing::GroupShape\>) | Grup şeklinin numaralandırması başladığında çağrılır. |
| virtual [VisitHeaderFooterEnd](./visitheaderfooterend/)(System::SharedPtr\<Aspose::Words::HeaderFooter\>) | Bir bölümdeki üstbilgi veya altbilginin numaralandırması bittiğinde çağrılır. |
| virtual [VisitHeaderFooterStart](./visitheaderfooterstart/)(System::SharedPtr\<Aspose::Words::HeaderFooter\>) | Bir bölümdeki üstbilgi veya altbilginin numaralandırması başladığında çağrılır. |
| virtual [VisitOfficeMathEnd](./visitofficemathend/)(System::SharedPtr\<Aspose::Words::Math::OfficeMath\>) | Office [Math](../../aspose.words.math/) nesnesinin numaralandırması bittiğinde çağrılır. |
| virtual [VisitOfficeMathStart](./visitofficemathstart/)(System::SharedPtr\<Aspose::Words::Math::OfficeMath\>) | Office [Math](../../aspose.words.math/) nesnesinin numaralandırması başladığında çağrılır. |
| virtual [VisitParagraphEnd](./visitparagraphend/)(System::SharedPtr\<Aspose::Words::Paragraph\>) | Paragrafın numaralandırması bittiğinde çağrılır. |
| virtual [VisitParagraphStart](./visitparagraphstart/)(System::SharedPtr\<Aspose::Words::Paragraph\>) | Paragrafın numaralandırması başladığında çağrılır. |
| virtual [VisitRowEnd](./visitrowend/)(System::SharedPtr\<Aspose::Words::Tables::Row\>) | Tablo satırının numaralandırması bittiğinde çağrılır. |
| virtual [VisitRowStart](./visitrowstart/)(System::SharedPtr\<Aspose::Words::Tables::Row\>) | Tablo satırının numaralandırması başladığında çağrılır. |
| virtual [VisitRun](./visitrun/)(System::SharedPtr\<Aspose::Words::Run\>) | Belge içinde bir metin yürütmesiyle karşılaşıldığında çağrılır. |
| virtual [VisitSectionEnd](./visitsectionend/)(System::SharedPtr\<Aspose::Words::Section\>) | Bölümün numaralandırması bittiğinde çağrılır. |
| virtual [VisitSectionStart](./visitsectionstart/)(System::SharedPtr\<Aspose::Words::Section\>) | Bölümün numaralandırması başladığında çağrılır. |
| virtual [VisitShapeEnd](./visitshapeend/)(System::SharedPtr\<Aspose::Words::Drawing::Shape\>) | Şeklin numaralandırması bittiğinde çağrılır. |
| virtual [VisitShapeStart](./visitshapestart/)(System::SharedPtr\<Aspose::Words::Drawing::Shape\>) | Şeklin numaralandırması başladığında çağrılır. |
| virtual [VisitSmartTagEnd](./visitsmarttagend/)(System::SharedPtr\<Aspose::Words::Markup::SmartTag\>) | Akıllı etiketin numaralandırması bittiğinde çağrılır. |
| virtual [VisitSmartTagStart](./visitsmarttagstart/)(System::SharedPtr\<Aspose::Words::Markup::SmartTag\>) | Akıllı etiketin numaralandırması başladığında çağrılır. |
| virtual [VisitSpecialChar](./visitspecialchar/)(System::SharedPtr\<Aspose::Words::SpecialChar\>) | Belge içinde bir [SpecialChar](../specialchar/) düğümüyle karşılaşıldığında çağrılır. |
| virtual [VisitStructuredDocumentTagEnd](./visitstructureddocumenttagend/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>) | Yapılandırılmış belge etiketi yinelemesi sona erdiğinde çağrılır. |
| virtual [VisitStructuredDocumentTagRangeEnd](./visitstructureddocumenttagrangeend/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTagRangeEnd\>) | Bir StructuredDocumentTagRangeEnd ile karşılaşıldığında çağrılır. |
| virtual [VisitStructuredDocumentTagRangeStart](./visitstructureddocumenttagrangestart/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTagRangeStart\>) | Bir StructuredDocumentTagRangeStart ile karşılaşıldığında çağrılır. |
| virtual [VisitStructuredDocumentTagStart](./visitstructureddocumenttagstart/)(System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>) | Yapılandırılmış belge etiketi yinelemesi başlatıldığında çağrılır. |
| virtual [VisitSubDocument](./visitsubdocument/)(System::SharedPtr\<Aspose::Words::SubDocument\>) | Bir alt belge ile karşılaşıldığında çağrılır. |
| virtual [VisitTableEnd](./visittableend/)(System::SharedPtr\<Aspose::Words::Tables::Table\>) | Bir tablonun yinelemesi sona erdiğinde çağrılır. |
| virtual [VisitTableStart](./visittablestart/)(System::SharedPtr\<Aspose::Words::Tables::Table\>) | Bir tablonun yinelemesi başlatıldığında çağrılır. |
## Açıklamalar


[DocumentVisitor](./) ile belge ağacında yineleme gerektiren özel işlemleri tanımlayabilir ve çalıştırabilirsiniz.

Örneğin, Aspose.Words, çeşitli formatlarda [Document](../document/) kaydetmek ve bir belge parçası üzerinde alanları veya yer imlerini bulmak gibi diğer işlemler için dahili olarak [DocumentVisitor](./) kullanır.

[DocumentVisitor](./) kullanmak için:

1. [DocumentVisitor](./) türetilen bir sınıf oluşturun.
1. Bazı veya tüm VisitXXX yöntemlerini geçersiz kılarak ve uygulayarak özel işlemler gerçekleştirin.
1. Yinelemeyi başlatmak istediğiniz [Node](../node/) üzerinde [Node.Accept](../node/accept/) yöntemini çağırın.



[DocumentVisitor](./) provides default implementations for all of the VisitXXX methods to make it easier to create new document visitors as only the methods required for the particular visitor need to be overridden. It is not necessary to override all of the visitor methods.

Daha fazla bilgi için Visitor tasarım desenine bakın.
## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
