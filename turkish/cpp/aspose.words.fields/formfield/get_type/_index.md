---
title: "Aspose::Words::Fields::FormField::get_Type yöntemi"
linktitle: "get_Type"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FormField::get_Type yöntemi. Form alanı tipini C++'ta döndürür."
type: docs
weight: 24000
url: /tr/cpp/aspose.words.fields/formfield/get_type/
---
## FormField::get_Type method


Form alanı türünü döndürür.

```cpp
Aspose::Words::Fields::FieldType Aspose::Words::Fields::FormField::get_Type()
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

* Enum [FieldType](../../fieldtype/)
* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
