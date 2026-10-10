---
title: "طريقة Aspose::Words::CompositeNode::get_LastChild"
linktitle: "get_LastChild"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::CompositeNode::get_LastChild. تحصل على الطفل الأخير للعقدة في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words/compositenode/get_lastchild/
---
## CompositeNode::get_LastChild method


يحصل على الطفل الأخير للعقدة.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::CompositeNode::get_LastChild() const
```


## أمثلة



يظهر كيفية استخدام طرق [Node](../../node/) و[CompositeNode](../) لإزالة قسم قبل القسم الأخير في المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Section 1 text.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakContinuous);
builder->Writeln(u"Section 2 text.");

// كلا القسمين هما أشقاء لبعضهما البعض.
auto lastSection = System::ExplicitCast<Aspose::Words::Section>(doc->get_LastChild());
auto firstSection = System::ExplicitCast<Aspose::Words::Section>(lastSection->get_PreviousSibling());

// إزالة قسم بناءً على علاقة الأخوة مع قسم آخر.
if (lastSection->get_PreviousSibling() != nullptr)
{
    doc->RemoveChild<System::SharedPtr<Aspose::Words::Section>>(firstSection);
}

// القسم الذي أزلناه كان الأول، مما ترك المستند يحتوي فقط على الثاني.
ASSERT_EQ(u"Section 2 text.", doc->GetText().Trim());
```

## انظر أيضًا

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
