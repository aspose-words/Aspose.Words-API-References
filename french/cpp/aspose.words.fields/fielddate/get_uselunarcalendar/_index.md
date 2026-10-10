---
title: "Aspose::Words::Fields::FieldDate::get_UseLunarCalendar méthode"
linktitle: "get_UseLunarCalendar"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldDate::get_UseLunarCalendar méthode. Obtient ou définit si le calendrier lunaire Hijri ou le calendrier lunaire Hébreu doit être utilisé en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.fields/fielddate/get_uselunarcalendar/
---
## FieldDate::get_UseLunarCalendar method


Obtient ou définit si l’on doit utiliser le calendrier lunaire hijri ou le calendrier lunaire hébreu.

```cpp
bool Aspose::Words::Fields::FieldDate::get_UseLunarCalendar() override
```


## Exemples



Montre comment utiliser les champs DATE pour afficher les dates selon différents types de calendriers.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Si nous voulons que le texte du document affiche toujours la date correcte, nous pouvons utiliser un champ DATE.
// Voici trois types de calendriers culturels qu’un champ DATE peut utiliser pour afficher une date.
// 1 -  Calendrier lunaire islamique :
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseLunarCalendar(true);
ASSERT_EQ(u" DATE  \\h", field->GetFieldCode());
builder->Writeln();

// 2 -  Calendrier Umm al-Qura :
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseUmAlQuraCalendar(true);
ASSERT_EQ(u" DATE  \\u", field->GetFieldCode());
builder->Writeln();

// 3 -  Calendrier national indien :
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseSakaEraCalendar(true);
ASSERT_EQ(u" DATE  \\s", field->GetFieldCode());
builder->Writeln();

// Insérez un champ DATE et définissez son type de calendrier sur celui utilisé en dernier par l’application hôte.
// Dans Microsoft Word, le type sera celui le plus récemment utilisé dans la boîte de dialogue Insertion -> Texte -> Date et Heure.
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseLastFormat(true);
ASSERT_EQ(u" DATE  \\l", field->GetFieldCode());
builder->Writeln();

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.DATE.docx");
```

## Voir aussi

* Class [FieldDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
