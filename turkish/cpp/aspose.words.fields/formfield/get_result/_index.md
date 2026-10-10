---
title: "Aspose::Words::Fields::FormField::get_Result metodu"
linktitle: "get_Result"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FormField::get_Result metodu. Bu form alanının sonucunu temsil eden bir dizeyi alır veya ayarlar (C++)."
type: docs
weight: 19000
url: /tr/cpp/aspose.words.fields/formfield/get_result/
---
## FormField::get_Result method


Bu form alanının sonucunu temsil eden bir dizeyi alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FormField::get_Result()
```

## Açıklamalar


Metin form alanı için sonuç, alanda bulunan metindir.

Onay kutusu form alanı için sonuç, işaretli veya işaretsiz olduğunu göstermek üzere \"1\" veya \"0\" olabilir.

Açılır menü form alanı için sonuç, açılır menüde seçilen dizedir.

Metin form alanı için [Result](./) ayarlamak, [TextInputFormat](../get_textinputformat/) içinde belirtilen metin biçimini uygulamaz. Bir değer ayarlamak ve biçimi uygulamak istiyorsanız, [SetTextInputValue()](../) metodunu kullanın.

Metin form alanı için *value* **null** ise [TextInputDefault](../get_textinputdefault/) değeri uygulanır.

## Örnekler



Bir combo kutusunun nasıl ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Please select a fruit: ");

// Kullanıcının bir dizi dizeden bir seçenek seçmesine izin veren bir combo kutusu ekleyin.
System::SharedPtr<Aspose::Words::Fields::FormField> comboBox = builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"Apple", u"Banana", u"Cherry"}), 0);

ASSERT_EQ(u"MyComboBox", comboBox->get_Name());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldFormDropDown, comboBox->get_Type());
ASSERT_EQ(u"Apple", comboBox->get_Result());

// Form alanı, bir "select" HTML etiketi şeklinde görünecek.
doc->Save(get_ArtifactsDir() + u"FormFields.Create.html");
```

## Ayrıca Bakınız

* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
