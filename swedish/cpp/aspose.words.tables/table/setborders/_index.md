---
title: "Aspose::Words::Tables::Table::SetBorders metod"
linktitle: "SetBorders"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::Table::SetBorders metod. Ställer in alla tabellramar till den angivna linjestilen, bredden och färgen i C++."
type: docs
weight: 69000
url: /sv/cpp/aspose.words.tables/table/setborders/
---
## Table::SetBorders method


Sätter alla tabellramar till den angivna linjestilen, bredden och färgen.

```cpp
void Aspose::Words::Tables::Table::SetBorders(Aspose::Words::LineStyle lineStyle, double lineWidth, System::Drawing::Color color)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| lineStyle | Aspose::Words::LineStyle | Linjestilen att tillämpa. |
| lineWidth | double | Linjebredden att ange (i punkter). |
| color | System::Drawing::Color | Färgen att använda för ramen. |

## Exempel



Visar hur man applicerar kant- och skuggningsfärg när man bygger en tabell.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Starta en tabell och ange en standardfärg/-tjocklek för dess kanter.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
table->SetBorders(Aspose::Words::LineStyle::Single, 2.0, System::Drawing::Color::get_Black());

// Skapa en rad med två celler med olika bakgrundsfärger.
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightSkyBlue());
builder->Writeln(u"Row 1, Cell 1.");
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());
builder->Writeln(u"Row 1, Cell 2.");
builder->EndRow();

// Återställ cellformatering för att inaktivera bakgrundsfärgerna
// ange en anpassad kanttjocklek för alla nya celler som skapas av byggaren,
// bygg sedan en andra rad.
builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->get_Borders()->get_Left()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Right()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Top()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Bottom()->set_LineWidth(4.0);

builder->InsertCell();
builder->Writeln(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Writeln(u"Row 2, Cell 2.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.TableBordersAndShading.docx");
```


Visar hur man formaterar alla tabellens ramar på en gång.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Rensa alla befintliga ramar från tabellen.
table->ClearBorders();

// Ställ in en enda grön linje som både yttre och inre ram för den här tabellen.
table->SetBorders(Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Table.SetBorders.docx");
```

## Se även

* Enum [LineStyle](../../../aspose.words/linestyle/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
