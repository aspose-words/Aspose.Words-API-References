---
title: "Metodo Aspose::Words::Tables::Cell::get_CellFormat"
linktitle: "get_CellFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Tables::Cell::get_CellFormat. Fornisce l'accesso alle proprietà di formattazione della cella in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.tables/cell/get_cellformat/
---
## Cell::get_CellFormat method


Fornisce l'accesso alle proprietà di formattazione della cella.

```cpp
System::SharedPtr<Aspose::Words::Tables::CellFormat> Aspose::Words::Tables::Cell::get_CellFormat()
```


## Esempi



Mostra come modificare il formato di righe e celle in una tabella.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"City");
builder->InsertCell();
builder->Write(u"Country");
builder->EndRow();
builder->InsertCell();
builder->Write(u"London");
builder->InsertCell();
builder->Write(u"U.K.");
builder->EndTable();

// Usa la proprietà "RowFormat" della prima riga per modificare la formattazione
// del contenuto di tutte le celle in questa riga.
System::SharedPtr<Aspose::Words::Tables::RowFormat> rowFormat = table->get_FirstRow()->get_RowFormat();
rowFormat->set_Height(25);
rowFormat->get_Borders()->idx_get(Aspose::Words::BorderType::Bottom)->set_Color(System::Drawing::Color::get_Red());

// Usa la proprietà "CellFormat" della prima cella nell'ultima riga per modificare la formattazione del contenuto di quella cella.
System::SharedPtr<Aspose::Words::Tables::CellFormat> cellFormat = table->get_LastRow()->get_FirstCell()->get_CellFormat();
cellFormat->set_Width(100);
cellFormat->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());

doc->Save(get_ArtifactsDir() + u"Table.RowCellFormat.docx");
```


Mostra come modificare la formattazione di una cella di tabella.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Cell> firstCell = table->get_FirstRow()->get_FirstCell();

// Utilizza la proprietà "CellFormat" di una cella per impostare la formattazione che modifica l'aspetto di quella cella.
firstCell->get_CellFormat()->set_Width(30);
firstCell->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
firstCell->get_CellFormat()->get_Shading()->set_ForegroundPatternColor(System::Drawing::Color::get_LightGreen());

doc->Save(get_ArtifactsDir() + u"Table.CellFormat.docx");
```


Mostra come combinare le righe di due tabelle in una sola.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

// Di seguito sono riportati due modi per ottenere una tabella da un documento.
// 1 -  Dalla collezione "Tables" di un nodo Body:
System::SharedPtr<Aspose::Words::Tables::Table> firstTable = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// 2 -  Utilizzando il metodo "GetChild":
auto secondTable = System::ExplicitCast<Aspose::Words::Tables::Table>(doc->GetChild(Aspose::Words::NodeType::Table, 1, true));

// Aggiungi tutte le righe dalla tabella corrente a quella successiva.
while (secondTable->get_HasChildNodes())
{
    firstTable->get_Rows()->Add(secondTable->get_FirstRow());
}

// Rimuovi il contenitore della tabella vuota.
secondTable->Remove();

doc->Save(get_ArtifactsDir() + u"Table.CombineTables.docx");
```

## Vedi anche

* Class [CellFormat](../../cellformat/)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
