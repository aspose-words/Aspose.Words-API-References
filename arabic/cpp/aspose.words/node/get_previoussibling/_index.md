---
title: "طريقة Aspose::Words::Node::get_PreviousSibling"
linktitle: "get_PreviousSibling"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Node::get_PreviousSibling method. يحصل على العقدة التي تسبق هذه العقدة مباشرةً في C++."
type: docs
weight: 11000
url: /ar/cpp/aspose.words/node/get_previoussibling/
---
## Node::get_PreviousSibling method


يحصل على العقدة التي تسبق هذه العقدة مباشرةً.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::get_PreviousSibling()
```


## أمثلة



يوضح كيفية استخدام طرق [Node](../) و[CompositeNode](../../compositenode/) لإزالة قسم قبل القسم الأخير في المستند.
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

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
