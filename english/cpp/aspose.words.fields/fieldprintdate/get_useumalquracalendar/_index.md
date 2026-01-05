---
title: Aspose::Words::Fields::FieldPrintDate::get_UseUmAlQuraCalendar method
linktitle: get_UseUmAlQuraCalendar
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldPrintDate::get_UseUmAlQuraCalendar method. Gets or sets whether to use the Um-al-Qura calendar in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.fields/fieldprintdate/get_useumalquracalendar/
---
## FieldPrintDate::get_UseUmAlQuraCalendar method


Gets or sets whether to use the Um-al-Qura calendar.

```cpp
bool Aspose::Words::Fields::FieldPrintDate::get_UseUmAlQuraCalendar() override
```


## Examples



Shows read PRINTDATE fields. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Field sample - PRINTDATE.docx");

// When a document is printed by a printer or printed as a PDF (but not exported to PDF),
// PRINTDATE fields will display the print operation's date/time.
// If no printing has taken place, these fields will display "0/0/0000".
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(0));

ASSERT_EQ(u"3/25/2020 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE ", field->GetFieldCode());

// Below are three different calendar types according to which the PRINTDATE field
// can display the date and time of the last printing operation.
// 1 -  Islamic Lunar Calendar:
field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(1));

ASSERT_TRUE(field->get_UseLunarCalendar());
ASSERT_EQ(u"8/1/1441 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\h", field->GetFieldCode());

field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(2));

// 2 -  Umm al-Qura calendar:
ASSERT_TRUE(field->get_UseUmAlQuraCalendar());
ASSERT_EQ(u"8/1/1441 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\u", field->GetFieldCode());

field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(3));

// 3 -  Indian National Calendar:
ASSERT_TRUE(field->get_UseSakaEraCalendar());
ASSERT_EQ(u"1/5/1942 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\s", field->GetFieldCode());
```

## See Also

* Class [FieldPrintDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
