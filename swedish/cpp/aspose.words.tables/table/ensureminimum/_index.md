---
title: "Aspose::Words::Tables::Table::EnsureMinimum metod"
linktitle: "EnsureMinimum"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::Table::EnsureMinimum metod. Om tabellen inte har några rader skapar och lägger till en Row i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words.tables/table/ensureminimum/
---
## Table::EnsureMinimum method


Om tabellen inte har några rader skapar och lägger till en [Row](../../row/).

```cpp
void Aspose::Words::Tables::Table::EnsureMinimum()
```


## Exempel



Visar hur man säkerställer att en tabellnod innehåller de noder vi behöver för att lägga till innehåll.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);

// Tabeller innehåller rader, som innehåller celler, som kan innehålla stycken
// med typiska element som körningar, former och till och med andra tabeller.
// Vår nya tabell har ingen av dessa noder, och vi kan inte lägga till innehåll i den förrän den har dem.
ASSERT_EQ(0, table->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Att anropa metoden "EnsureMinimum" på en tabell kommer att säkerställa att
// tabellen har minst en rad och en cell med ett tomt stycke.
table->EnsureMinimum();
table->get_FirstRow()->get_FirstCell()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## Se även

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
