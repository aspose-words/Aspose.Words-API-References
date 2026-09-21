---
title: "Aspose::Words::Tables::CellFormat::ClearFormatting metod"
linktitle: "ClearFormatting"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::CellFormat::ClearFormatting method. Återställer till standardformatering för cellen. Ändrar inte cellens bredd i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.tables/cellformat/clearformatting/
---
## CellFormat::ClearFormatting method


Återställer till standardformatering för cellen. Ändrar inte cellens bredd.

```cpp
void Aspose::Words::Tables::CellFormat::ClearFormatting()
```


## Exempel



Visar hur man kombinerar raderna från två tabeller till en.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

// Nedan följer två sätt att hämta en tabell från ett dokument.
// 1 -  Från "Tables"-samlingen i en Body-nod:
System::SharedPtr<Aspose::Words::Tables::Table> firstTable = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// 2 -  Med hjälp av "GetChild"-metoden:
auto secondTable = System::ExplicitCast<Aspose::Words::Tables::Table>(doc->GetChild(Aspose::Words::NodeType::Table, 1, true));

// Lägg till alla rader från den aktuella tabellen till nästa.
while (secondTable->get_HasChildNodes())
{
    firstTable->get_Rows()->Add(secondTable->get_FirstRow());
}

// Ta bort den tomma tabellbehållaren.
secondTable->Remove();

doc->Save(get_ArtifactsDir() + u"Table.CombineTables.docx");
```

## Se även

* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
