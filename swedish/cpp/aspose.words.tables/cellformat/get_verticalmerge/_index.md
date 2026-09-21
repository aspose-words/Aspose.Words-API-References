---
title: "Aspose::Words::Tables::CellFormat::get_VerticalMerge metod"
linktitle: "get_VerticalMerge"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::CellFormat::get_VerticalMerge metod. Anger hur cellen slås samman med andra celler vertikalt i C++."
type: docs
weight: 14000
url: /sv/cpp/aspose.words.tables/cellformat/get_verticalmerge/
---
## CellFormat::get_VerticalMerge method


Anger hur cellen slås samman med andra celler vertikalt.

```cpp
Aspose::Words::Tables::CellMerge Aspose::Words::Tables::CellFormat::get_VerticalMerge()
```

## Anmärkningar


Celler kan endast slås samman vertikalt om deras vänstra och högra gränser är identiska.

När celler slås samman vertikalt konsolideras visningsområdena för de sammanslagna cellerna. Det konsoliderade området används för att visa innehållet i den första vertikalt sammanslagna cellen och alla andra vertikalt sammanslagna celler måste vara tomma.

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

## Se även

* Enum [CellMerge](../../cellmerge/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
