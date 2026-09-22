---
title: "Aspose::Words::CleanupOptions::get_DuplicateStyle metodu"
linktitle: "get_DuplicateStyle"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::CleanupOptions::get_DuplicateStyle metodu. Belgede yinelenen stillerin kaldırılıp kaldırılmayacağını gösteren bir bayrağı alır/ayarlar. Varsayılan değer C++'ta false'tur."
type: docs
weight: 3000
url: /tr/cpp/aspose.words/cleanupoptions/get_duplicatestyle/
---
## CleanupOptions::get_DuplicateStyle method


Belgeden yinelenen stillerin kaldırılıp kaldırılmayacağını gösteren bir bayrağı alır/ayarlar. Varsayılan değer **false**.

```cpp
bool Aspose::Words::CleanupOptions::get_DuplicateStyle() const
```


## Örnekler



Belgeden yinelenen stillerin nasıl kaldırılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Belgeye aynı özelliklere sahip iki stil ekleyin,
// ancak farklı adlarla. İkinci stil, birincinin bir kopyası olarak kabul edilir.
System::SharedPtr<Aspose::Words::Style> myStyle = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
myStyle->get_Font()->set_Size(14);
myStyle->get_Font()->set_Name(u"Courier New");
myStyle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

System::SharedPtr<Aspose::Words::Style> duplicateStyle = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle2");
duplicateStyle->get_Font()->set_Size(14);
duplicateStyle->get_Font()->set_Name(u"Courier New");
duplicateStyle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

ASSERT_EQ(6, doc->get_Styles()->get_Count());

// Her iki stili de belgedeki farklı paragraflara uygulayın.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_ParagraphFormat()->set_StyleName(myStyle->get_Name());
builder->Writeln(u"Hello world!");

builder->get_ParagraphFormat()->set_StyleName(duplicateStyle->get_Name());
builder->Writeln(u"Hello again!");

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASPOSE_ASSERT_EQ(myStyle, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Style());
ASPOSE_ASSERT_EQ(duplicateStyle, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Style());

// Bir CleanOptions nesnesi yapılandırın, ardından tüm yinelenen stilleri değiştirmek için Cleanup metodunu çağırın
// orijinaliyle ve belgeden kopyaları kaldırarak.
auto cleanupOptions = System::MakeObject<Aspose::Words::CleanupOptions>();
cleanupOptions->set_DuplicateStyle(true);

doc->Cleanup(cleanupOptions);

ASSERT_EQ(5, doc->get_Styles()->get_Count());
ASPOSE_ASSERT_EQ(myStyle, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Style());
ASPOSE_ASSERT_EQ(myStyle, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Style());
```

## Ayrıca Bakınız

* Class [CleanupOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
