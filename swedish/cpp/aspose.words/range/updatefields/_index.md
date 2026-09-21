---
title: "Aspose::Words::Range::UpdateFields metod"
linktitle: "UpdateFields"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Range::UpdateFields metod. Uppdaterar värdena för dokumentfält i detta intervall i C++."
type: docs
weight: 15000
url: /sv/cpp/aspose.words/range/updatefields/
---
## Range::UpdateFields method


Uppdaterar värdena för dokumentfält i detta område.

```cpp
void Aspose::Words::Range::UpdateFields()
```

## Anmärkningar


När du öppnar, ändrar och sedan sparar ett dokument uppdaterar inte Aspose.Words fält automatiskt, utan behåller dem intakta. Därför vill du vanligtvis anropa den här metoden innan du sparar om du har ändrat dokumentet programmässigt och vill försäkra dig om att de korrekta (beräknade) fältvärdena visas i det sparade dokumentet.

Det finns inget behov av att uppdatera fält efter att ha utfört en kopplad utskick eftersom kopplad utskick är en form av fältuppdatering och automatiskt uppdaterar alla fält i dokumentet.

Denna metod uppdaterar inte alla fälttyper. För en detaljerad lista över stödjade fälttyper, se Programmerarguiden.

Denna metod uppdaterar inte fält som är relaterade till sidlayoutalgoritmer (t.ex. PAGE, PAGES, PAGEREF). Sidlayoutrelaterade fält uppdateras när du renderar ett dokument eller anropar [UpdatePageLayout](../../document/updatepagelayout/).

För att uppdatera fält i hela dokumentet, använd [UpdateFields](../../document/updatefields/).

## Exempel



Visar hur man uppdaterar alla fält i ett intervall.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertField(u" DOCPROPERTY Category");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);
builder->InsertField(u" DOCPROPERTY Category");

// Ovanstående DOCPROPERTY-fält kommer att visa värdet för den här inbyggda dokumentegenskapen.
doc->get_BuiltInDocumentProperties()->set_Category(u"MyCategory");

// Om vi uppdaterar värdet på en dokumentegenskap måste vi uppdatera alla DOCPROPERTY-fält för att visa det.
ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// Uppdatera alla fält som finns i intervallet för det första avsnittet.
doc->get_FirstSection()->get_Range()->UpdateFields();

ASSERT_EQ(u"MyCategory", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(1)->get_Result());
```

## Se även

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
