---
title: "Metodo Aspose::Words::Tables::Table::SetBorders"
linktitle: "SetBorders"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Tables::Table::SetBorders. Imposta tutti i bordi della tabella allo stile di linea, larghezza e colore specificati in C++."
type: docs
weight: 69000
url: /it/cpp/aspose.words.tables/table/setborders/
---
## Table::SetBorders method


Imposta tutti i bordi della tabella allo stile di linea, larghezza e colore specificati.

```cpp
void Aspose::Words::Tables::Table::SetBorders(Aspose::Words::LineStyle lineStyle, double lineWidth, System::Drawing::Color color)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| lineStyle | Aspose::Words::LineStyle | Lo stile di linea da applicare. |
| lineWidth | double | La larghezza della linea da impostare (in punti). |
| color | System::Drawing::Color | Il colore da usare per il bordo. |

## Esempi



Mostra come applicare il colore del bordo e dell'ombreggiatura durante la creazione di una tabella.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Avvia una tabella e imposta un colore/spessore predefinito per i suoi bordi.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
table->SetBorders(Aspose::Words::LineStyle::Single, 2.0, System::Drawing::Color::get_Black());

// Crea una riga con due celle con colori di sfondo diversi.
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightSkyBlue());
builder->Writeln(u"Row 1, Cell 1.");
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());
builder->Writeln(u"Row 1, Cell 2.");
builder->EndRow();

// Reimposta la formattazione delle celle per disabilitare i colori di sfondo
// imposta uno spessore del bordo personalizzato per tutte le nuove celle create dal builder,
// quindi crea una seconda riga.
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


Mostra come formattare tutti i bordi di una tabella in una sola volta.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Rimuove tutti i bordi esistenti dalla tabella.
table->ClearBorders();

// Imposta una singola linea verde per fungere da tutti i bordi esterni e interni di questa tabella.
table->SetBorders(Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Table.SetBorders.docx");
```

## Vedi anche

* Enum [LineStyle](../../../aspose.words/linestyle/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
