---
title: "Aspose::Words::HeightRule enum"
linktitle: "HeightRule"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::HeightRule enum. Anger regeln för att bestämma höjden på ett objekt i C++."
type: docs
weight: 91000
url: /sv/cpp/aspose.words/heightrule/
---
## HeightRule enum


Anger regeln för att bestämma höjden på ett objekt.

```cpp
enum class HeightRule
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| AtLeast | 0 | Höjden kommer att vara minst den angivna höjden i punkter. Den kommer att växa, om det behövs, för att rymma all text i ett objekt. |
| Exactly | 1 | Höjden anges exakt i punkter. Observera att om texten inte får plats i objektet med denna höjd, kommer den att trunkeras. |
| Auto | 2 | Höjden kommer automatiskt att växa för att rymma all text i ett objekt. |


## Exempel



Visar hur man formaterar rader med en dokumentbyggare.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");

// Starta en andra rad och konfigurera sedan dess höjd. Byggaren kommer att tillämpa dessa inställningar på
// dess aktuella rad, samt alla nya rader den skapar därefter.
builder->EndRow();

System::SharedPtr<Aspose::Words::Tables::RowFormat> rowFormat = builder->get_RowFormat();
rowFormat->set_Height(100);
rowFormat->set_HeightRule(Aspose::Words::HeightRule::Exactly);

builder->InsertCell();
builder->Write(u"Row 2, cell 1.");
builder->EndTable();

// Den första raden påverkades inte av omkonfigurationen av utfyllnad och behåller fortfarande standardvärdena.
ASPOSE_ASSERT_EQ(0.0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());

ASPOSE_ASSERT_EQ(100.0, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetRowFormatting.docx");
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
