---
title: "Aspose::Words::Fields::Field::get_LocaleId méthode"
linktitle: "get_LocaleId"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::Field::get_LocaleId méthode. Obtient ou définit le LCID du champ en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words.fields/field/get_localeid/
---
## Field::get_LocaleId method


Obtient ou définit le LCID du champ.

```cpp
int32_t Aspose::Words::Fields::Field::get_LocaleId()
```


## Exemples



Montre comment insérer un champ et travailler avec son paramètre régional.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez un champ DATE, puis affichez la date qu'il affichera.
// La culture actuelle de votre thread détermine le format de la date.
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE");
std::cout << System::String::Format(u"Today's date, as displayed in the \"{0}\" culture: {1}", System::Globalization::CultureInfo::get_CurrentCulture()->get_EnglishName(), field->get_Result()) << std::endl;

ASSERT_EQ(1033, field->get_LocaleId());

// Modifier la culture de notre thread affectera le résultat du champ DATE.
// Une autre façon de faire afficher une date dans une culture différente par le champ DATE est d'utiliser sa propriété LocaleId.
// Cette méthode nous permet d'éviter de changer la culture du thread pour obtenir cet effet.
doc->get_FieldOptions()->set_FieldUpdateCultureSource(Aspose::Words::Fields::FieldUpdateCultureSource::FieldCode);
auto de = System::MakeObject<System::Globalization::CultureInfo>(u"de-DE");
field->set_LocaleId(de->get_LCID());
field->Update();

std::cout << System::String::Format(u"Today's date, as displayed according to the \"{0}\" culture: {1}", System::Globalization::CultureInfo::GetCultureInfo(field->get_LocaleId())->get_EnglishName(), field->get_Result()) << std::endl;
```

## Voir aussi

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
