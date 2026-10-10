---
title: "Aspose::Words::StyleCollection::get_Count method"
linktitle: "get_Count"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::StyleCollection::get_Count method. C++'ta koleksiyondaki stil sayısını alır."
type: docs
weight: 5000
url: /tr/cpp/aspose.words/stylecollection/get_count/
---
## StyleCollection::get_Count method


Koleksiyondaki stil sayısını alır.

```cpp
int32_t Aspose::Words::StyleCollection::get_Count()
```


## Örnekler



Bir belgenin stil koleksiyonuna bir [Style](../../style/) nasıl eklenir gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// Bu koleksiyona daha sonra ekleyebileceğimiz yeni stiller için varsayılan parametreleri ayarlayın.
styles->get_DefaultFont()->set_Name(u"Courier New");
// Eğer "StyleType.Paragraph" stilini eklersek, koleksiyon değerlerini uygular
// "DefaultParagraphFormat" özelliğini stilin "ParagraphFormat" özelliğine.
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// Bir stil ekleyin ve ardından varsayılan ayarları içerdiğini doğrulayın.
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## Ayrıca Bakınız

* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
