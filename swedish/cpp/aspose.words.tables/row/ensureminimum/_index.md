---
title: "Aspose::Words::Tables::Row::EnsureMinimum metod"
linktitle: "EnsureMinimum"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::Row::EnsureMinimum‑metod. Om raden inte har några celler skapas och läggs en cell till i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.tables/row/ensureminimum/
---
## Row::EnsureMinimum method


Om [Row](../) inte har några celler skapas och läggs en [Cell](../../cell/) till.

```cpp
void Aspose::Words::Tables::Row::EnsureMinimum()
```


## Exempel



Visar hur man säkerställer att en radnod innehåller de noder som behövs för att börja lägga till innehåll i den.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);
auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);

// Rader innehåller celler, som i sin tur innehåller stycken med typiska element såsom run‑objekt, former och till och med andra tabeller.
// Vår nya rad har ingen av dessa noder, och vi kan inte lägga till innehåll i den förrän den har dem.
ASSERT_EQ(0, row->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Att anropa metoden "EnsureMinimum" på en tabell kommer att säkerställa att
// Tabellen har minst en cell med ett tomt stycke.
row->EnsureMinimum();
row->get_FirstCell()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## Se även

* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
