---
title: "Aspose::Words::Node::get_PreviousSibling yöntemi"
linktitle: "get_PreviousSibling"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Node::get_PreviousSibling yöntemi. Bu düğümden hemen önce gelen düğümü C++'da alır."
type: docs
weight: 11000
url: /tr/cpp/aspose.words/node/get_previoussibling/
---
## Node::get_PreviousSibling method


Bu düğümden hemen önce gelen düğümü alır.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::get_PreviousSibling()
```


## Örnekler



Belge içinde son bölümden önce bir bölümü kaldırmak için [Node](../) ve [CompositeNode](../../compositenode/) yöntemlerinin nasıl kullanılacağını gösterir.
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

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
