---
title: "Aspose::Words::Fields::FieldPrintDate::get_UseSakaEraCalendar méthode"
linktitle: "get_UseSakaEraCalendar"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldPrintDate::get_UseSakaEraCalendar méthode. Obtient ou définit si le calendrier Saka Era doit être utilisé en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.fields/fieldprintdate/get_usesakaeracalendar/
---
## FieldPrintDate::get_UseSakaEraCalendar method


Obtient ou définit si l’on doit utiliser le calendrier de l’ère Saka.

```cpp
bool Aspose::Words::Fields::FieldPrintDate::get_UseSakaEraCalendar() override
```


## Exemples



Affiche les champs PRINTDATE lus.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Field sample - PRINTDATE.docx");

// Lorsqu'un document est imprimé par une imprimante ou imprimé en PDF (mais pas exporté en PDF),
// Les champs PRINTDATE afficheront la date/heure de l'opération d'impression.
// Si aucune impression n'a eu lieu, ces champs afficheront "0/0/0000".
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(0));

ASSERT_EQ(u"3/25/2020 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE ", field->GetFieldCode());

// Ci-dessous, trois types de calendriers différents selon lesquels le champ PRINTDATE
// peut afficher la date et l'heure de la dernière opération d'impression.
// 1 -  Calendrier lunaire islamique :
field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(1));

ASSERT_TRUE(field->get_UseLunarCalendar());
ASSERT_EQ(u"8/1/1441 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\h", field->GetFieldCode());

field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(2));

// 2 -  Calendrier Umm al-Qura :
ASSERT_TRUE(field->get_UseUmAlQuraCalendar());
ASSERT_EQ(u"8/1/1441 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\u", field->GetFieldCode());

field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(3));

// 3 -  Calendrier national indien :
ASSERT_TRUE(field->get_UseSakaEraCalendar());
ASSERT_EQ(u"1/5/1942 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\s", field->GetFieldCode());
```

## Voir aussi

* Class [FieldPrintDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
