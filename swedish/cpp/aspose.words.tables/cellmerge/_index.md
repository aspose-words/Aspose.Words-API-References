---
title: "Aspose::Words::Tables::CellMerge enum"
linktitle: "CellMerge"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::CellMerge enum. Anger hur en cell i en tabell slås samman med andra celler i C++."
type: docs
weight: 11000
url: /sv/cpp/aspose.words.tables/cellmerge/
---
## CellMerge enum


Anger hur en cell i en tabell slås samman med andra celler.

```cpp
enum class CellMerge
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| None | 0 | Cellen är inte sammanslagen. |
| Första | 1 | Cellen är den första cellen i ett intervall av sammanslagna celler. |
| Föregående | 2 | Cellen är sammanslagen med den föregående cellen horisontellt eller vertikalt. |


## Exempel



Visar hur man slår samman tabellceller vertikalt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga en cell i den första kolumnen i den första raden.
// Denna cell kommer att vara den första i ett intervall av vertikalt sammanslagna celler.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::First);
builder->Write(u"Text in merged cells.");

// Infoga en cell i den andra kolumnen i den första raden, avsluta sedan raden.
// Konfigurera också byggaren för att inaktivera vertikal sammanslagning i skapade celler.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::None);
builder->Write(u"Text in unmerged cell.");
builder->EndRow();

// Infoga en cell i den första kolumnen i den andra raden.
// Istället för att lägga till textinnehåll kommer vi att slå samman den här cellen med den första cellen som vi lade till direkt ovanför.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::Previous);

// Infoga en annan oberoende cell i den andra kolumnen i den andra raden.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::None);
builder->Write(u"Text in unmerged cell.");
builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"CellFormat.VerticalMerge.docx");
```


Visar hur man slår samman tabellceller horisontellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga en cell i den första kolumnen i den första raden.
// Denna cell kommer att vara den första i ett intervall av horisontellt sammanslagna celler.
builder->InsertCell();
builder->get_CellFormat()->set_HorizontalMerge(Aspose::Words::Tables::CellMerge::First);
builder->Write(u"Text in merged cells.");

// Infoga en cell i den andra kolumnen i den första raden. Istället för att lägga till textinnehåll,
// kommer vi att slå samman den här cellen med den första cellen som vi lade till direkt till vänster.
builder->InsertCell();
builder->get_CellFormat()->set_HorizontalMerge(Aspose::Words::Tables::CellMerge::Previous);
builder->EndRow();

// Infoga två ytterligare osammanslagna celler till den andra raden.
builder->get_CellFormat()->set_HorizontalMerge(Aspose::Words::Tables::CellMerge::None);
builder->InsertCell();
builder->Write(u"Text in unmerged cell.");
builder->InsertCell();
builder->Write(u"Text in unmerged cell.");
builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"CellFormat.HorizontalMerge.docx");
```

## Se även

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
