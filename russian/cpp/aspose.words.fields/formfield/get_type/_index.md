---
title: "Aspose::Words::Fields::FormField::get_Type метод"
linktitle: "get_Type"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FormField::get_Type метод. Возвращает тип поля формы в C++."
type: docs
weight: 24000
url: /ru/cpp/aspose.words.fields/formfield/get_type/
---
## FormField::get_Type method


Возвращает тип поля формы.

```cpp
Aspose::Words::Fields::FieldType Aspose::Words::Fields::FormField::get_Type()
```


## Примеры



Показывает, как вставить комбобокс.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Please select a fruit: ");

// Вставьте комбобокс, который позволит пользователю выбрать вариант из набора строк.
System::SharedPtr<Aspose::Words::Fields::FormField> comboBox = builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"Apple", u"Banana", u"Cherry"}), 0);

ASSERT_EQ(u"MyComboBox", comboBox->get_Name());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldFormDropDown, comboBox->get_Type());
ASSERT_EQ(u"Apple", comboBox->get_Result());

// Поле формы будет отображаться в виде HTML‑тега "select".
doc->Save(get_ArtifactsDir() + u"FormFields.Create.html");
```

## См. также

* Enum [FieldType](../../fieldtype/)
* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
