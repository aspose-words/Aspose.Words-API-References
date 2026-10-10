---
title: "Aspose::Words::Tables::PreferredWidthType enum"
linktitle: "PreferredWidthType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::PreferredWidthType enum. Anger enheten för mätning av den föredragna bredden för en tabell eller cell i C++."
type: docs
weight: 13000
url: /sv/cpp/aspose.words.tables/preferredwidthtype/
---
## PreferredWidthType enum


Anger måttenheten för den föredragna bredden på en tabell eller cell.

```cpp
enum class PreferredWidthType
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Auto | 1 | Den föredragna bredden är inte specificerad. Den faktiska bredden på tabellen eller cellen är antingen specificerad med den explicita bredden eller kommer att bestämmas automatiskt av tabellens layoutalgoritm när tabellen visas, beroende på inställningen för automatisk anpassning av tabellen. |
| Percent | 2 | Mät den aktuella objektbredden med en angiven procentsats. |
| Punkter | 3 | Mät den aktuella objektbredden med ett angivet antal punkter (1/72 tum). |


## Exempel



Visar hur man verifierar den föredragna breddtypen och värdet för en tabellcell.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Cell> firstCell = table->get_FirstRow()->get_FirstCell();

ASSERT_EQ(Aspose::Words::Tables::PreferredWidthType::Percent, firstCell->get_CellFormat()->get_PreferredWidth()->get_Type());
ASPOSE_ASSERT_EQ(11.16, firstCell->get_CellFormat()->get_PreferredWidth()->get_Value());
```

## Se även

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
