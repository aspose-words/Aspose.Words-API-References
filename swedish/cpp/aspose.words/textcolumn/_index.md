---
title: "Aspose::Words::TextColumn klass"
linktitle: "TextColumn"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::TextColumn klass. Representerar en enskild textkolumn. TextColumn är en medlem av TextColumnCollection‑samlingen. TextColumn‑samlingen innehåller alla kolumner i ett avsnitt i ett dokument. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 70000
url: /sv/cpp/aspose.words/textcolumn/
---
## TextColumn class


Representerar en enskild textkolumn. [TextColumn](./) är en medlem av [TextColumnCollection](../textcolumncollection/)‑samlingen. [TextColumn](./)‑samlingen innehåller alla kolumner i ett avsnitt i ett dokument. För att lära dig mer, besök dokumentationsartikeln [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/).

```cpp
class TextColumn : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_SpaceAfter](./get_spaceafter/)() | Hämtar eller anger avståndet mellan denna kolumn och nästa kolumn i punkter. Krävs inte för den sista kolumnen. |
| [get_Width](./get_width/)() | Hämtar eller anger bredden på textkolumnen i punkter. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_SpaceAfter](./set_spaceafter/)(double) | Inställare för [Aspose::Words::TextColumn::get_SpaceAfter](./get_spaceafter/). |
| [set_Width](./set_width/)(double) | Inställare för [Aspose::Words::TextColumn::get_Width](./get_width/). |
| static [Type](./type/)() |  |
## Anmärkningar


[TextColumn](./) objects are only used to specify columns with custom width and spacing. If you want the columns in the document to be of equal width, set TextColumns.[EvenlySpaced](../textcolumncollection/get_evenlyspaced/) to **true**.

När en ny [TextColumn](./) skapas har den sin bredd och avstånd inställda på noll.

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
