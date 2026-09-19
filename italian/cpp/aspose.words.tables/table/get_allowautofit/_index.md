---
title: "Metodo Aspose::Words::Tables::Table::get_AllowAutoFit"
linktitle: "get_AllowAutoFit"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Tables::Table::get_AllowAutoFit. Consente a Microsoft Word e Aspose.Words di ridimensionare automaticamente le celle di una tabella per adattarle al loro contenuto in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words.tables/table/get_allowautofit/
---
## Table::get_AllowAutoFit method


Consente a Microsoft Word e Aspose.Words di ridimensionare automaticamente le celle in una tabella per adattarle al loro contenuto.

```cpp
bool Aspose::Words::Tables::Table::get_AllowAutoFit()
```

## Note


Il valore predefinito è **true**.

## Esempi



Mostra come abilitare/disabilitare il ridimensionamento automatico delle celle della tabella.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(100));
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::Auto());
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->EndRow();
builder->EndTable();

// Imposta la proprietà "AllowAutoFit" su "false" per far sì che la tabella mantenga le dimensioni
// di tutte le sue righe e celle, e trunca i contenuti se diventano troppo grandi per adattarsi.
// Imposta la proprietà "AllowAutoFit" su "true" per consentire alla tabella di modificare la larghezza e l'altezza delle sue celle
// per adattare i loro contenuti.
table->set_AllowAutoFit(allowAutoFit);

doc->Save(get_ArtifactsDir() + u"Table.AllowAutoFitOnTable.html");
```

## Vedi anche

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
