---
title: "Aspose::Words::Fields::FieldStart::get_FieldData méthode"
linktitle: "get_FieldData"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldStart::get_FieldData méthode. Obtient les données personnalisées du champ qui sont associées au champ en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.fields/fieldstart/get_fielddata/
---
## FieldStart::get_FieldData method


Obtient les données de champ personnalisées associées au champ.

```cpp
const System::ArrayPtr<uint8_t> & Aspose::Words::Fields::FieldStart::get_FieldData() const
```


## Exemples



Montre comment obtenir les données associées au champ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Field sample - Field with data.docx");

System::SharedPtr<Aspose::Words::Fields::Field> field = doc->get_Range()->get_Fields()->idx_get(2);
std::cout << System::Text::Encoding::get_Default()->GetString(field->get_Start()->get_FieldData()) << std::endl;
```

## Voir aussi

* Class [FieldStart](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
