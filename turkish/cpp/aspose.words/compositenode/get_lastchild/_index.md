---
title: "Aspose::Words::CompositeNode::get_LastChild metodu"
linktitle: "get_LastChild"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::CompositeNode::get_LastChild metodu. C++'da düğümün son çocuğunu alır."
type: docs
weight: 8000
url: /tr/cpp/aspose.words/compositenode/get_lastchild/
---
## CompositeNode::get_LastChild method


Düğümün son çocuğunu alır.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::CompositeNode::get_LastChild() const
```


## Örnekler



Belgedeki son bölümden önce bir bölümü kaldırmak için [Node](../../node/) ve [CompositeNode](../) yöntemlerinin nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Section 1 text.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakContinuous);
builder->Writeln(u"Section 2 text.");

// Her iki bölüm de birbirinin kardeşidir.
auto lastSection = System::ExplicitCast<Aspose::Words::Section>(doc->get_LastChild());
auto firstSection = System::ExplicitCast<Aspose::Words::Section>(lastSection->get_PreviousSibling());

// Bir bölümün, başka bir bölümle olan kardeş ilişkisine dayanarak kaldırılması.
if (lastSection->get_PreviousSibling() != nullptr)
{
    doc->RemoveChild<System::SharedPtr<Aspose::Words::Section>>(firstSection);
}

// Kaldırdığımız bölüm ilk olanıydı, böylece belge sadece ikinci bölümle kaldı.
ASSERT_EQ(u"Section 2 text.", doc->GetText().Trim());
```

## Ayrıca Bakınız

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
