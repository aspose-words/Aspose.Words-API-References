---
title: "Aspose::Words::CompositeNode::IndexOf yöntemi"
linktitle: "IndexOf"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::CompositeNode::IndexOf yöntemi. Belirtilen alt düğümün, alt düğüm dizisindeki indeksini C++'de döndürür."
type: docs
weight: 14000
url: /tr/cpp/aspose.words/compositenode/indexof/
---
## CompositeNode::IndexOf method


Belirtilen alt düğümün alt düğüm dizisindeki indeksini döndürür.

```cpp
int32_t Aspose::Words::CompositeNode::IndexOf(const System::SharedPtr<Aspose::Words::Node> &child)
```


## Örnekler



Bir alt düğümün ebeveyninden indeksinin nasıl alınacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

System::SharedPtr<Aspose::Words::Body> body = doc->get_FirstSection()->get_Body();

// İlk bölümün gövdesindeki son paragrafın indeksini al.
ASSERT_EQ(24, body->GetChildNodes(Aspose::Words::NodeType::Any, false)->IndexOf(body->get_LastParagraph()));
```

## Ayrıca Bakınız

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
