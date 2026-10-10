---
title: "Aspose::Words::Section::DeleteHeaderFooterShapes yöntemi"
linktitle: "DeleteHeaderFooterShapes"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Section::DeleteHeaderFooterShapes yöntemi. Bu bölümün başlık ve altbilgilerindeki tüm şekilleri (çizim nesneleri) C++'ta siler."
type: docs
weight: 8000
url: /tr/cpp/aspose.words/section/deleteheaderfootershapes/
---
## Section::DeleteHeaderFooterShapes method


Bu bölümün üstbilgi ve altbilgilerindeki tüm şekilleri (çizim nesneleri) siler.

```cpp
void Aspose::Words::Section::DeleteHeaderFooterShapes()
```


## Örnekler



Bir bölümdeki tüm başlık ve altbilgilerden tüm şekilleri nasıl kaldırılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir şekil içeren birincil bir başlık oluştur.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 100);

// Bir resim içeren birincil bir altbilgi oluştur.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->InsertImage(get_ImageDir() + u"Logo icon.ico");

ASSERT_EQ(1, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
ASSERT_EQ(1, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());

// İlk bölümdeki başlık ve altbilgilerden tüm şekilleri kaldır.
doc->get_FirstSection()->DeleteHeaderFooterShapes();

ASSERT_EQ(0, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
ASSERT_EQ(0, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
```

## Ayrıca Bakınız

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
