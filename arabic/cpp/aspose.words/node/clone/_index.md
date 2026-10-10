---
title: "طريقة Aspose::Words::Node::Clone"
linktitle: "Clone"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Node::Clone. تنشئ نسخة مكررة من العقدة في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/node/clone/
---
## Node::Clone method


ينشئ نسخة مكررة من العقدة.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::Clone(bool isCloneChildren)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| isCloneChildren | bool | True لاستنساخ الشجرة الفرعية تحت العقدة المحددة بشكل متكرر؛ false لاستنساخ العقدة نفسها فقط. |

### ReturnValue

العقدة المستنسخة.
## ملاحظات


هذه الطريقة تعمل كمنشئ نسخة للعقد. العقدة المستنسخة لا تملك أبًا، لكنها تنتمي إلى نفس المستند مثل العقدة الأصلية.

هذه الطريقة دائمًا تقوم بنسخة عميقة من العقدة. يحدد المعامل *isCloneChildren* ما إذا كان يجب نسخ جميع العقد الفرعية أيضًا.

## أمثلة



يظهر كيفية استنساخ عقدة مركبة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// فيما يلي طريقتان لاستنساخ عقدة مركبة.
// 1 -  إنشاء نسخة من عقدة، وإنشاء نسخة من كل عقدة فرعية لها أيضًا.
System::SharedPtr<Aspose::Words::Node> cloneWithChildren = System::ExplicitCast<Aspose::Words::Node>(para)->Clone(true);

ASSERT_TRUE((System::ExplicitCast<Aspose::Words::CompositeNode>(cloneWithChildren))->get_HasChildNodes());
ASSERT_EQ(u"Hello world!", cloneWithChildren->GetText().Trim());

// 2 -  إنشاء نسخة من عقدة بمفردها دون أي عقد فرعية.
System::SharedPtr<Aspose::Words::Node> cloneWithoutChildren = System::ExplicitCast<Aspose::Words::Node>(para)->Clone(false);

ASSERT_FALSE((System::ExplicitCast<Aspose::Words::CompositeNode>(cloneWithoutChildren))->get_HasChildNodes());
ASSERT_EQ(System::String::Empty, cloneWithoutChildren->GetText().Trim());
```

## انظر أيضًا

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
