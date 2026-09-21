---
title: "Aspose::Words::Tables::Cell::EnsureMinimum metod"
linktitle: "EnsureMinimum"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::Cell::EnsureMinimum metod. Om det sista barnet inte är ett stycke skapas och läggs ett tomt stycke till i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.tables/cell/ensureminimum/
---
## Cell::EnsureMinimum method


Om den sista underordnade inte är ett stycke, skapas och läggs ett tomt stycke till.

```cpp
void Aspose::Words::Tables::Cell::EnsureMinimum()
```


## Exempel



Visar hur man säkerställer att en cellnod innehåller de noder vi behöver för att börja lägga till innehåll i den.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);
auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);
auto cell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
row->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(cell);

// Celler kan innehålla stycken med typiska element såsom run‑objekt, former och till och med andra tabeller.
// Vår nya cell har inga stycken, och vi kan inte lägga till innehåll såsom run‑ och form‑noder förrän den har det.
ASSERT_EQ(0, cell->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Att anropa "EnsureMinimum"‑metoden på en cell kommer att säkerställa att
// cellen har minst ett tomt stycke, vilket vi sedan kan lägga till innehåll i.
cell->EnsureMinimum();
cell->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## Se även

* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
