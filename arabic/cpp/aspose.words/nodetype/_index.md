---
title: "تعداد Aspose::Words::NodeType"
linktitle: "NodeType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "تعداد Aspose::Words::NodeType. يحدد نوع عقدة مستند Word في C++."
type: docs
weight: 102000
url: /ar/cpp/aspose.words/nodetype/
---
## NodeType enum


يحدد نوع عقدة مستند Word.

```cpp
enum class NodeType
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| أي | 0 | يشير إلى جميع أنواع العقد. يسمح باختيار جميع العناصر الفرعية. |
| Document | 1 | كائن [Document](../document/) الذي، باعتباره جذر شجرة المستند، يوفر الوصول إلى مستند Word بالكامل. يمكن لعقدة [Document](../document/) أن تحتوي على عقد [Section](../section/). |
| Section | 2 | كائن [Section](../section/) الذي يتطابق مع قسم واحد في مستند Word. يمكن لعقدة [Section](../section/) أن تحتوي على عقد [Body](../body/) و[HeaderFooter](../headerfooter/). |
| Body | 3 | كائن [Body](../body/) الذي يحتوي على النص الرئيسي للقسم (قصة النص الرئيسي). يمكن لعقدة [Body](../body/) أن تحتوي على عقد [Paragraph](../paragraph/) و[Table](../../aspose.words.tables/table/). |
| HeaderFooter | 4 | كائن [HeaderFooter](../headerfooter/) الذي يحتوي على نص رأس أو تذييل معين داخل قسم. يمكن لعقدة [HeaderFooter](../headerfooter/) أن تحتوي على عقد [Paragraph](../paragraph/) و[Table](../../aspose.words.tables/table/). |
| Table | 5 | كائن [Table](../../aspose.words.tables/table/) الذي يمثل جدولًا في مستند Word. يمكن لعقدة [Table](../../aspose.words.tables/table/) أن تحتوي على عقد [Row](../../aspose.words.tables/row/). |
| Row | 6 | صف من جدول. يمكن لعقدة [Row](../../aspose.words.tables/row/) أن تحتوي على عقد [Cell](../../aspose.words.tables/cell/). |
| Cell | 7 | خلية من صف جدول. يمكن لعقدة [Cell](../../aspose.words.tables/cell/) أن تحتوي على عقد [Paragraph](../paragraph/) و[Table](../../aspose.words.tables/table/). |
| Paragraph | 8 | فقرة نصية. عقدة [Paragraph](../paragraph/) هي حاوية لعناصر المستوى الداخلي [Run](../run/)، [FieldStart](../../aspose.words.fields/fieldstart/)، [FieldSeparator](../../aspose.words.fields/fieldseparator/)، [FieldEnd](../../aspose.words.fields/fieldend/)، [FormField](../../aspose.words.fields/formfield/)، [Shape](../../aspose.words.drawing/shape/)، [GroupShape](../../aspose.words.drawing/groupshape/)، [Footnote](../../aspose.words.notes/footnote/)، [Comment](../comment/)، [SpecialChar](../specialchar/)، بالإضافة إلى [BookmarkStart](../bookmarkstart/) و[BookmarkEnd](../bookmarkend/). |
| BookmarkStart | 9 | بداية علامة إشارة مرجعية. |
| BookmarkEnd | 10 | نهاية علامة إشارة مرجعية. |
| EditableRangeStart | 11 | بداية نطاق قابل للتحرير. |
| EditableRangeEnd | 12 | نهاية نطاق قابل للتحرير. |
| MoveFromRangeStart | 13 | بداية نطاق MoveFrom. |
| MoveFromRangeEnd | 14 | نهاية نطاق MoveFrom. |
| MoveToRangeStart | 15 | بداية نطاق MoveTo. |
| MoveToRangeEnd | 16 | نهاية نطاق MoveTo. |
| GroupShape | 17 | مجموعة من الأشكال، الصور، كائنات OLE أو مجموعات أشكال أخرى. يمكن لعقدة [GroupShape](../../aspose.words.drawing/groupshape/) أن تحتوي على عقد أخرى من نوع [Shape](../../aspose.words.drawing/shape/) و[GroupShape](../../aspose.words.drawing/groupshape/). |
| Shape | 18 | كائن رسم، مثل شكل OfficeArt أو صورة أو كائن OLE. يمكن لعقدة [Shape](../../aspose.words.drawing/shape/) أن تحتوي على [Paragraph](../paragraph/) و[Table](../../aspose.words.tables/table/). |
| Comment | 19 | تعليق في مستند Word. يمكن لعقدة [Comment](../comment/) أن تحتوي على [Paragraph](../paragraph/) و[Table](../../aspose.words.tables/table/). |
| Footnote | 20 | حاشية سفلية أو هوامش نهائية في مستند Word. يمكن لعقدة [Footnote](../../aspose.words.notes/footnote/) أن تحتوي على [Paragraph](../paragraph/) و[Table](../../aspose.words.tables/table/). |
| Run | 21 | مقاطع نصية. |
| FieldStart | 22 | حرف خاص يحدد بداية حقل Word. |
| FieldSeparator | 23 | حرف خاص يفصل بين شفرة الحقل ونتيجته. |
| FieldEnd | 24 | حرف خاص يحدد نهاية حقل Word. |
| FormField | 25 | حقل نموذج. |
| SpecialChar | 26 | حرف خاص ليس من الأنواع المحددة الأخرى للأحرف الخاصة. |
| SmartTag | 27 | علامة ذكية حول بنية واحدة أو أكثر مضمّنة (مقاطع، صور، حقول، إلخ) داخل فقرة. |
| StructuredDocumentTag | 28 | يسمح بتعريف معلومات مخصصة للعميل وطريقة عرضها. |
| StructuredDocumentTagRangeStart | 29 | بداية علامة مستند منظم **ranged** التي تقبل محتوى متعدد الأقسام. |
| StructuredDocumentTagRangeEnd | 30 | نهاية علامة مستند منظم **ranged** التي تقبل محتوى متعدد الأقسام. |
| GlossaryDocument | 31 | مستند مسرد داخل المستند الرئيسي. |
| BuildingBlock | 32 | كتلة بناء داخل مستند مسرد (مثال: مدخل مستند مسرد). |
| CommentRangeStart | 33 | عقدة علامة تمثل بداية نطاق مُعلق. |
| CommentRangeEnd | 34 | عقدة علامة تمثل نهاية نطاق مُعلق. |
| OfficeMath | 35 | كائن Office [Math](../../aspose.words.math/). يمكن أن يكون معادلة أو دالة أو مصفوفة أو أحد الكائنات الرياضية الأخرى. يمكن أن يكون مجموعة من الكائنات الرياضية ويمكن أيضًا أن يحتوي على بعض الكائنات غير الرياضية مثل مقاطع النص. |
| SubDocument | 36 | عقدة مستند فرعي هي رابط إلى مستند آخر. |
| System | 37 | محجوز للاستخدام الداخلي من قبل [Aspose.Words](../). |
| Null | 38 | محجوز للاستخدام الداخلي من قبل [Aspose.Words](../). |


## أمثلة



يظهر كيفية التنقل عبر مجموعة العقد الفرعية لعقدة مركبة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// أضف تشغيلين وشكلاً واحدًا كعقد فرعية إلى الفقرة الأولى في هذا المستند.
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world! "));

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
// لاحظ أن 'CustomNodeId' لا يتم حفظه في ملف إخراج ويوجوده فقط خلال عمر العقدة.
shape->set_CustomNodeId(100);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello again!"));

// تكرار عبر مجموعة الأطفال الفوريين للفقرة،
// وطباعة أي تشغيلات أو أشكال نجدها بداخلها.
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

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
