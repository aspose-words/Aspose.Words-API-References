---
title: "طريقة Aspose::Words::Node::get_NodeType"
linktitle: "get_NodeType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Node::get_NodeType. تحصل على نوع هذه العقدة في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words/node/get_nodetype/
---
## Node::get_NodeType method


يحصل على نوع هذه العقدة.

```cpp
virtual Aspose::Words::NodeType Aspose::Words::Node::get_NodeType() const =0
```


## أمثلة



يظهر كيفية إزالة جميع العقد الفرعية من نوع معين من عقدة مركبة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

ASSERT_EQ(2, doc->GetChildNodes(Aspose::Words::NodeType::Table, true)->get_Count());

System::SharedPtr<Aspose::Words::Node> curNode = doc->get_FirstSection()->get_Body()->get_FirstChild();

while (curNode != nullptr)
{
    // احفظ العقدة الشقيقة التالية كمتغير في حال أردنا الانتقال إليها بعد حذف هذه العقدة.
    System::SharedPtr<Aspose::Words::Node> nextNode = curNode->get_NextSibling();

    // يمكن لجسم القسم أن يحتوي على عقد الفقرة والجدول.
    // إذا كانت العقدة جدولًا، قم بإزالتها من الأصل.
    if (curNode->get_NodeType() == Aspose::Words::NodeType::Table)
    {
        curNode->Remove();
    }

    curNode = nextNode;
}

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Table, true)->get_Count());
```


يوضح كيفية استخدام خاصية NextSibling للعقدة لتعداد الأطفال المباشرين لها.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

for (System::SharedPtr<Aspose::Words::Node> node = doc->get_FirstSection()->get_Body()->get_FirstChild(); node != nullptr; node = node->get_NextSibling())
{
    std::cout << std::endl;
    std::cout << System::String::Format(u"Node type: {0}", Aspose::Words::Node::NodeTypeToString(node->get_NodeType())) << std::endl;

    System::String contents = node->GetText().Trim();
    std::cout << (contents == System::String::Empty ? u"This node contains no text" : System::String::Format(u"Contents: \"{0}\"", node->GetText().Trim())) << std::endl;
}
```

## انظر أيضًا

* Enum [NodeType](../../nodetype/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
