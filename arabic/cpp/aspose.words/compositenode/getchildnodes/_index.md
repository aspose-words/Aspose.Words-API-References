---
title: "طريقة Aspose::Words::CompositeNode::GetChildNodes"
linktitle: "GetChildNodes"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::CompositeNode::GetChildNodes. تُرجع مجموعة حية من العقد الفرعية التي تطابق النوع المحدد في C++."
type: docs
weight: 10000
url: /ar/cpp/aspose.words/compositenode/getchildnodes/
---
## CompositeNode::GetChildNodes method


يعيد مجموعة حية من العقد الفرعية التي تطابق النوع المحدد.

```cpp
System::SharedPtr<Aspose::Words::NodeCollection> Aspose::Words::CompositeNode::GetChildNodes(Aspose::Words::NodeType nodeType, bool isDeep)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| nodeType | Aspose::Words::NodeType | يحدد نوع العقد التي سيتم اختيارها. |
| isDeep | bool | **true** لتحديد جميع العقد الفرعية بشكل متكرر؛ **false** لتحديد فقط بين الأطفال المباشرين. |

### ReturnValue

مجموعة حية من العقد الفرعية من النوع المحدد.
## ملاحظات


المجموعة التي تُرجعها هذه الطريقة دائمًا حية.

المجموعة الحية تكون دائمًا متزامنة مع المستند. على سبيل المثال، إذا قمت بتحديد جميع الأقسام في مستند وتقوم بالتعداد عبر المجموعة بحذف الأقسام، يتم إزالة القسم من المجموعة فورًا عندما يُحذف من المستند.

## أمثلة



يوضح كيفية طباعة جميع تعليقات المستند وردودها.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Comments.docx");

System::SharedPtr<Aspose::Words::NodeCollection> comments = doc->GetChildNodes(Aspose::Words::NodeType::Comment, true);

// إذا لم يكن للتعليق سلف، فهو تعليق "عالي المستوى" وليس تعليقًا من نوع الرد.
// اطبع جميع التعليقات عالية المستوى مع أي ردود قد تكون لها.
for (auto&& comment : comments->LINQ_OfType<System::SharedPtr<Aspose::Words::Comment> >()->LINQ_Where(static_cast<System::Func<System::SharedPtr<Aspose::Words::Comment>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Comment> c)>>([](System::SharedPtr<Aspose::Words::Comment> c) -> bool
{
    return c->get_Ancestor() == nullptr;
})))->LINQ_ToList())
{
    std::cout << "Top-level comment:" << std::endl;
    std::cout << System::String::Format(u"\t\"{0}\", by {1}", comment->GetText().Trim(), comment->get_Author()) << std::endl;
    std::cout << System::String::Format(u"Has {0} replies", comment->get_Replies()->get_Count()) << std::endl;
    for (auto&& commentReply : System::IterateOver<Aspose::Words::Comment>(comment->get_Replies()))
    {
        std::cout << System::String::Format(u"\t\"{0}\", by {1}", commentReply->GetText().Trim(), commentReply->get_Author()) << std::endl;
    }
    std::cout << std::endl;
}
```


يوضح كيفية استخراج الصور من مستند، وحفظها على نظام الملفات المحلي كملفات منفصلة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// احصل على مجموعة الأشكال من المستند،
// واحفظ بيانات الصورة لكل شكل يحتوي على صورة كملف على نظام الملفات المحلي.
System::SharedPtr<Aspose::Words::NodeCollection> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true);

ASSERT_EQ(9, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> s)>>([](System::SharedPtr<Aspose::Words::Node> s) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Drawing::Shape>(s))->get_HasImage();
}))));

int32_t imageIndex = 0;
for (auto&& shape : System::IterateOver(shapes->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()))
{
    if (shape->get_HasImage())
    {
        // قد تحتوي بيانات الصور للأشكال على صور بعدة تنسيقات صورة محتملة.
        // يمكننا تحديد امتداد الملف لكل صورة تلقائيًا بناءً على تنسيقها.
        System::String imageFileName = System::String::Format(u"File.ExtractImages.{0}{1}", imageIndex, Aspose::Words::FileFormatUtil::ImageTypeToExtension(shape->get_ImageData()->get_ImageType()));
        shape->get_ImageData()->Save(get_ArtifactsDir() + imageFileName);
        imageIndex++;
    }
}
```


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


يوضح كيفية إضافة وتحديث وحذف العقد الفرعية في مجموعة الأطفال لـ [CompositeNode](../).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// المستند الفارغ، بشكل افتراضي، يحتوي على فقرة واحدة.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());

// العقد المركبة مثل فقرتنا يمكنها احتواء عقد مركبة أخرى وعقد داخلية كعناصر فرعية.
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
auto paragraphText = System::MakeObject<Aspose::Words::Run>(doc, u"Initial text. ");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(paragraphText);

// أنشئ ثلاث عقد تشغيل إضافية.
auto run1 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 1. ");
auto run2 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 2. ");
auto run3 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 3. ");

// لن يعرض جسم المستند هذه المقاطع حتى نقوم بإدراجها في عقدة مركبة
// التي هي نفسها جزء من شجرة عقد المستند، كما فعلنا مع المقطع الأول.
// يمكننا تحديد أين تظهر محتويات النص للعقد التي نقوم بإدراجها
// تظهر في المستند عن طريق تحديد موقع الإدراج بالنسبة لعقدة أخرى في الفقرة.
ASSERT_EQ(u"Initial text.", paragraph->GetText().Trim());

// أدرج المقطع الثاني في الفقرة أمام المقطع الأول.
paragraph->InsertBefore<System::SharedPtr<Aspose::Words::Run>>(run2, paragraphText);

ASSERT_EQ(u"Run 2. Initial text.", paragraph->GetText().Trim());

// أدرج المقطع الثالث بعد المقطع الأول.
paragraph->InsertAfter<System::SharedPtr<Aspose::Words::Run>>(run3, paragraphText);

ASSERT_EQ(u"Run 2. Initial text. Run 3.", paragraph->GetText().Trim());

// أدرج المقطع الأول في بداية مجموعة العقد الفرعية للفقرة.
paragraph->PrependChild<System::SharedPtr<Aspose::Words::Run>>(run1);

ASSERT_EQ(u"Run 1. Run 2. Initial text. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(4, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// يمكننا تعديل محتويات المقطع عن طريق تحرير وحذف العقد الفرعية الموجودة.
(System::ExplicitCast<Aspose::Words::Run>(paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->idx_get(1)))->set_Text(u"Updated run 2. ");
paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->Remove(paragraphText);

ASSERT_EQ(u"Run 1. Updated run 2. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(3, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
```

## انظر أيضًا

* Class [NodeCollection](../../nodecollection/)
* Enum [NodeType](../../nodetype/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
