---
title: "Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages metod"
linktitle: "get_AllowBreakAcrossPages"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::get_AllowBreakAcrossPages metod. Sant om texten i en tabellrad får delas över ett sidbryt i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.tables/rowformat/get_allowbreakacrosspages/
---
## RowFormat::get_AllowBreakAcrossPages method


Sant om texten i en tabellrad får delas över en sidbrytning.

```cpp
bool Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages()
```


## Exempel



Visar hur man inaktiverar radbrytning över sidor för varje rad i en tabell.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table spanning two pages.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Ställ in egenskapen "AllowBreakAcrossPages" till "false" för att behålla raden
// i ett stycke om en tabell sträcker sig över två sidor, vilket bryter upp längs den raden.
// Om raden är för stor för att få plats på en sida kommer Microsoft Word att flytta den till nästa sida.
// Ställ in egenskapen "AllowBreakAcrossPages" till "true" för att tillåta att raden bryts upp över två sidor.
for (auto&& row : System::IterateOver<Aspose::Words::Tables::Row>(table))
{
    row->get_RowFormat()->set_AllowBreakAcrossPages(allowBreakAcrossPages);
}

doc->Save(get_ArtifactsDir() + u"Table.AllowBreakAcrossPages.docx");
```

## Se även

* Class [RowFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
