---
title: "Aspose::Words::Fields::FormField::get_Name yöntemi"
linktitle: "get_Name"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FormField::get_Name yöntemi. C++'ta form alanı adını alır veya ayarlar."
type: docs
weight: 15000
url: /tr/cpp/aspose.words.fields/formfield/get_name/
---
## FormField::get_Name method


Form alanı adını alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FormField::get_Name()
```


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
