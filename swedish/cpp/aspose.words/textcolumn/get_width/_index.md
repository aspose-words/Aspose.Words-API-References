---
title: "Aspose::Words::TextColumn::get_Width metod"
linktitle: "get_Width"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::TextColumn::get_Width metod. Hämtar eller anger bredden på textkolumnen i punkter i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words/textcolumn/get_width/
---
## TextColumn::get_Width method


Hämtar eller anger bredden på textkolumnen i punkter.

```cpp
double Aspose::Words::TextColumn::get_Width()
```


## Exempel



Visar hur man skapar ojämnt fördelade kolumner.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();

System::SharedPtr<Aspose::Words::TextColumnCollection> columns = pageSetup->get_TextColumns();
columns->set_EvenlySpaced(false);
columns->SetCount(2);

// Bestäm mängden utrymme som vi har tillgängligt för att arrangera kolumner.
double contentWidth = pageSetup->get_PageWidth() - pageSetup->get_LeftMargin() - pageSetup->get_RightMargin();

ASSERT_NEAR(470.30, contentWidth, 0.01);

// Ställ in den första kolumnen så att den är smal.
System::SharedPtr<Aspose::Words::TextColumn> column = columns->idx_get(0);
column->set_Width(100);
column->set_SpaceAfter(20);

// Ställ in den andra kolumnen så att den tar resten av det tillgängliga utrymmet inom sidans marginaler.
column = columns->idx_get(1);
column->set_Width(contentWidth - column->get_Width() - column->get_SpaceAfter());

builder->Writeln(u"Narrow column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Wide column 2.");

doc->Save(get_ArtifactsDir() + u"PageSetup.CustomColumnWidth.docx");
```

## Se även

* Class [TextColumn](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
