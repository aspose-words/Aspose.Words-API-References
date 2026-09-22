---
title: "طريقة Aspose::Words::NodeCollection::idx_get"
linktitle: "idx_get"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::NodeCollection::idx_get. تسترجع عقدة في الفهرس المحدد في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words/nodecollection/idx_get/
---
## NodeCollection::idx_get method


يسترجع عقدة في الفهرس المحدد.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::NodeCollection::idx_get(int32_t index)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| index | int32_t | فهرس داخل مجموعة العقد. |
## ملاحظات


الفهرس يبدأ من الصفر.

يسمح باستخدام الفهارس السلبية وتدل على الوصول من نهاية المجموعة. على سبيل المثال -1 يعني العنصر الأخير، -2 يعني العنصر قبل الأخير، وهكذا.

إذا كان الفهرس أكبر من أو يساوي عدد العناصر في القائمة، فإن هذا يُرجع إشارة فارغة.

إذا كان الفهرس سالبًا وكانت قيمته المطلقة أكبر من عدد العناصر في القائمة، فإن هذا يُرجع إشارة فارغة.

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

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
