---
title: "طريقة Aspose::Words::CompositeNode::GetChild"
linktitle: "GetChild"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::CompositeNode::GetChild. تُرجع العقدة الفرعية رقم N التي تطابق النوع المحدد في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words/compositenode/getchild/
---
## CompositeNode::GetChild method


يرجع عقدة الطفل رقم N التي تطابق النوع المحدد.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::CompositeNode::GetChild(Aspose::Words::NodeType nodeType, int32_t index, bool isDeep)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| nodeType | Aspose::Words::NodeType | يحدد نوع العقدة الفرعية. |
| index | int32_t | فهرس يبدأ من الصفر للعقدة الفرعية المراد اختيارها. يُسمح أيضًا بالفهارس السالبة وتدل على الوصول من النهاية، حيث -1 يعني العقدة الأخيرة. |
| isDeep | bool | **true** لاختيار جميع العقد الفرعية بشكل متكرر؛ **false** لاختيار فقط بين الأطفال المباشرين. راجع الملاحظات لمزيد من المعلومات. |

### ReturnValue

العقدة الفرعية التي تطابق المعايير أو **null** إذا لم يتم العثور على عقدة مطابقة.
## ملاحظات


إذا كان الفهرس خارج النطاق، يتم إرجاع **null**.

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
* Enum [NodeType](../../nodetype/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
