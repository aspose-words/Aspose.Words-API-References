---
title: "Aspose::Words::Document::Clone yöntemi"
linktitle: "Clone"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::Clone yöntemi. C++'ta Document'in derin bir kopyasını oluşturur."
type: docs
weight: 7000
url: /tr/cpp/aspose.words/document/clone/
---
## Document::Clone method


[Document](../) öğesinin derin bir kopyasını oluşturur.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::Document::Clone()
```


### ReturnValue

Klonlanmış belge.

## Örnekler



Bir belgenin derin klonlamasını nasıl yapacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

// Klonlama, orijinal ile aynı içeriğe sahip yeni bir belge oluşturur,
// ancak orijinal belgenin her düğümünün benzersiz bir kopyasıyla.
System::SharedPtr<Aspose::Words::Document> clone = doc->Clone();

ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->GetText(), clone->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());
ASSERT_NE(System::ObjectExt::GetHashCode(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)), System::ObjectExt::GetHashCode(clone->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)));
```

## Ayrıca Bakınız

* Class [Document](../)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
