---
title: "Aspose::Words::Fields::FieldCreateDate::get_UseSakaEraCalendar méthode"
linktitle: "get_UseSakaEraCalendar"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldCreateDate::get_UseSakaEraCalendar méthode. Obtient ou définit si le calendrier Saka Era doit être utilisé en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.fields/fieldcreatedate/get_usesakaeracalendar/
---
## FieldCreateDate::get_UseSakaEraCalendar method


Obtient ou définit si l’on doit utiliser le calendrier de l’ère Saka.

```cpp
bool Aspose::Words::Fields::FieldCreateDate::get_UseSakaEraCalendar() override
```


## Exemples



Montre comment utiliser le champ CREATEDATE pour afficher la date/heure de création du document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u" Date this document was created:");

// Nous pouvons utiliser le champ CREATEDATE pour afficher la date et l’heure de création du document.
// Ci-dessous, trois types de calendriers différents selon lesquels le champ CREATEDATE peut afficher la date/heure.
// 1 -  Calendrier lunaire islamique :
builder->Write(u"According to the Lunar Calendar - ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldCreateDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCreateDate, true));
field->set_UseLunarCalendar(true);

ASSERT_EQ(u" CREATEDATE  \\h", field->GetFieldCode());

// 2 -  Calendrier Umm al-Qura :
builder->Write(u"\nAccording to the Umm al-Qura Calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldCreateDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCreateDate, true));
field->set_UseUmAlQuraCalendar(true);

ASSERT_EQ(u" CREATEDATE  \\u", field->GetFieldCode());

// 3 -  Calendrier national indien :
builder->Write(u"\nAccording to the Indian National Calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldCreateDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCreateDate, true));
field->set_UseSakaEraCalendar(true);

ASSERT_EQ(u" CREATEDATE  \\s", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.CREATEDATE.docx");
```

## Voir aussi

* Class [FieldCreateDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
