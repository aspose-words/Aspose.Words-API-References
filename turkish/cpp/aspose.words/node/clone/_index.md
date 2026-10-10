---
title: "Aspose::Words::Node::Clone yöntemi"
linktitle: "Clone"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Node::Clone yöntemi. C++'da düğümün bir kopyasını oluşturur."
type: docs
weight: 4000
url: /tr/cpp/aspose.words/node/clone/
---
## Node::Clone method


Düğümün bir kopyasını oluşturur.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::Clone(bool isCloneChildren)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| isCloneChildren | bool | Belirtilen düğümün alt ağacını yinelemeli olarak kopyalamak için True; yalnızca düğümü kopyalamak için false. |

### ReturnValue

Kopyalanan düğüm.
## Açıklamalar


Bu yöntem, düğümler için bir kopya yapıcı görevi görür. Kopyalanan düğümün ebeveyni yoktur, ancak orijinal düğümle aynı belgeye aittir.

Bu yöntem her zaman düğümün derin bir kopyasını oluşturur. *isCloneChildren* parametresi, tüm alt düğümlerin de kopyalanıp kopyalanmayacağını belirtir.

## Örnekler



Bir birleşik düğümün nasıl kopyalanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// Aşağıda bir birleşik düğümün kopyalanmasının iki yolu verilmiştir.
// 1 -  Bir düğümün bir kopyasını oluştur ve aynı zamanda onun tüm alt düğümlerinin de bir kopyasını oluştur.
System::SharedPtr<Aspose::Words::Node> cloneWithChildren = System::ExplicitCast<Aspose::Words::Node>(para)->Clone(true);

ASSERT_TRUE((System::ExplicitCast<Aspose::Words::CompositeNode>(cloneWithChildren))->get_HasChildNodes());
ASSERT_EQ(u"Hello world!", cloneWithChildren->GetText().Trim());

// 2 -  Bir düğümün yalnızca kendisinin bir kopyasını, alt düğüm olmadan oluştur.
System::SharedPtr<Aspose::Words::Node> cloneWithoutChildren = System::ExplicitCast<Aspose::Words::Node>(para)->Clone(false);

ASSERT_FALSE((System::ExplicitCast<Aspose::Words::CompositeNode>(cloneWithoutChildren))->get_HasChildNodes());
ASSERT_EQ(System::String::Empty, cloneWithoutChildren->GetText().Trim());
```

## Ayrıca Bakınız

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
