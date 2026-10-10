---
title: "Aspose::Words::Tables::CellFormat::get_HorizontalMerge metod"
linktitle: "get_HorizontalMerge"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::CellFormat::get_HorizontalMerge metod. Anger hur cellen slås samman horisontellt med andra celler i raden i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.tables/cellformat/get_horizontalmerge/
---
## CellFormat::get_HorizontalMerge method


Anger hur cellen slås samman horisontellt med andra celler i raden.

```cpp
Aspose::Words::Tables::CellMerge Aspose::Words::Tables::CellFormat::get_HorizontalMerge()
```


## Exempel



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

* Enum [CellMerge](../../cellmerge/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
