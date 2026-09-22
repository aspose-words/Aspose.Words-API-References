---
title: "طريقة Aspose::Words::Node::NextPreOrder"
linktitle: "NextPreOrder"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Node::NextPreOrder. تحصل على العقدة التالية وفقًا لخوارزمية pre-order في C++."
type: docs
weight: 18000
url: /ar/cpp/aspose.words/node/nextpreorder/
---
## Node::NextPreOrder method


يحصل على العقدة التالية وفقًا لخوارزمية عبور الشجرة بترتيب ما قبل الترتيب.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::NextPreOrder(const System::SharedPtr<Aspose::Words::Node> &rootNode)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| rootNode | const System::SharedPtr\<Aspose::Words::Node\>\& | العقدة العليا (الحد) للتنقل. |

### ReturnValue

العقدة التالية بترتيب ما قبل الترتيب. تكون Null إذا تم الوصول إلى *rootNode*.

## أمثلة



يظهر كيفية استعراض شجرة عقد المستند باستخدام خوارزمية pre-order، وحذف أي شكل يُصادف يحتوي على صورة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

ASSERT_EQ(9, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_HasImage();
}))));

System::SharedPtr<Aspose::Words::Node> curNode = doc;
while (curNode != nullptr)
{
    System::SharedPtr<Aspose::Words::Node> nextNode = curNode->NextPreOrder(doc);

    if (curNode->PreviousPreOrder(doc) != nullptr && nextNode != nullptr)
    {
        ASPOSE_ASSERT_EQ(curNode, nextNode->PreviousPreOrder(doc));
    }

    if (curNode->get_NodeType() == Aspose::Words::NodeType::Shape && (System::ExplicitCast<Aspose::Words::Drawing::Shape>(curNode))->get_HasImage())
    {
        curNode->Remove();
    }

    curNode = nextNode;
}

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_HasImage();
}))));
```

## انظر أيضًا

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
