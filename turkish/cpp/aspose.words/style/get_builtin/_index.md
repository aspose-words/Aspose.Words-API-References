---
title: "Aspose::Words::Style::get_BuiltIn yöntemi"
linktitle: "get_BuiltIn"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Style::get_BuiltIn yöntemi. Stil, MS Word'deki yerleşik stillerden biri ise C++'ta True döner."
type: docs
weight: 6000
url: /tr/cpp/aspose.words/style/get_builtin/
---
## Style::get_BuiltIn method


Bu stil MS Word'deki yerleşik stillerden biri ise doğru.

```cpp
bool Aspose::Words::Style::get_BuiltIn()
```


## Örnekler



Özel stilleri yerleşik stillerden nasıl ayırt edeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Microsoft Word kullanarak veya programlı olarak Aspose.Words ile bir belge oluşturduğumuzda,
// belge, görünümünü değiştirmek için metnine uygulayabileceği bir stil koleksiyonu ile gelir.
// Bu yerleşik stillere belgenin "Styles" koleksiyonu aracılığıyla erişebiliriz.
// Bu stillerin tümü "BuiltIn" bayrağının "true" olarak ayarlandığını gösterir.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->idx_get(u"Emphasis");

ASSERT_TRUE(style->get_BuiltIn());

// Özel bir stil oluşturun ve koleksiyona ekleyin.
// Bu gibi özel stillerin "BuiltIn" bayrağı "false" olarak ayarlanır.
style = doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyStyle");
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());
style->get_Font()->set_Name(u"Courier New");

ASSERT_FALSE(style->get_BuiltIn());
```

## Ayrıca Bakınız

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
