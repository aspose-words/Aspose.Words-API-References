---
title: "Aspose::Words::Fields::FieldSaveDate::get_UseSakaEraCalendar méthode"
linktitle: "get_UseSakaEraCalendar"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldSaveDate::get_UseSakaEraCalendar méthode. Obtient ou définit si le calendrier Saka Era doit être utilisé en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.fields/fieldsavedate/get_usesakaeracalendar/
---
## FieldSaveDate::get_UseSakaEraCalendar method


Obtient ou définit si l’on doit utiliser le calendrier de l’ère Saka.

```cpp
bool Aspose::Words::Fields::FieldSaveDate::get_UseSakaEraCalendar() override
```


## Exemples



Montre comment utiliser le champ SAVEDATE pour afficher la date/heure de la dernière opération d'enregistrement du document effectuée avec Microsoft Word.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u" Date this document was last saved:");

// Nous pouvons utiliser le champ SAVEDATE pour afficher la date et l'heure de la dernière opération d'enregistrement sur le document.
// L'opération d'enregistrement à laquelle ces champs font référence est l'enregistrement manuel dans une application telle que Microsoft Word,
// et non la méthode Save du document.
// Ci-dessous, trois types de calendriers différents selon lesquels le champ SAVEDATE peut afficher la date/heure.
// 1 -  Calendrier lunaire islamique :
builder->Write(u"According to the Lunar Calendar - ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseLunarCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\h", field->GetFieldCode());

// 2 -  Calendrier Umm al-Qura :
builder->Write(u"\nAccording to the Umm al-Qura calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseUmAlQuraCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\u", field->GetFieldCode());

// 3 -  calendrier national indien :
builder->Write(u"\nAccording to the Indian National calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseSakaEraCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\s", field->GetFieldCode());

// Les champs SAVEDATE tirent leurs valeurs de date/heure de la propriété intégrée LastSavedTime.
// La méthode Save du document ne mettra pas à jour cette valeur, mais nous pouvons toujours la mettre à jour manuellement.
doc->get_BuiltInDocumentProperties()->set_LastSavedTime(System::DateTime::get_Now());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SAVEDATE.docx");
```

## Voir aussi

* Class [FieldSaveDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
