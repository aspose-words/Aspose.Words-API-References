---
title: "Aspose::Words::TextColumnCollection::get_LineBetween metod"
linktitle: "get_LineBetween"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::TextColumnCollection::get_LineBetween metod. När true, lägger till en vertikal linje mellan kolumnerna i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words/textcolumncollection/get_linebetween/
---
## TextColumnCollection::get_LineBetween method


När **true**, läggs en vertikal linje till mellan kolumnerna.

```cpp
bool Aspose::Words::TextColumnCollection::get_LineBetween()
```


## Exempel



Visar hur man separerar kolumner med en vertikal linje.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Konfigurera den aktuella sektionens PageSetup‑objekt för att dela upp texten i flera kolumner.
// Ställ in egenskapen "LineBetween" till "true" för att placera en delningslinje mellan kolumnerna.
// Ställ in egenskapen "LineBetween" till "false" för att låta utrymmet mellan kolumnerna vara tomt.
System::SharedPtr<Aspose::Words::TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->set_LineBetween(lineBetween);
columns->SetCount(3);

builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 3.");

doc->Save(get_ArtifactsDir() + u"PageSetup.VerticalLineBetweenColumns.docx");
```

## Se även

* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
