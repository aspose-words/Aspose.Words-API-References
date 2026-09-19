---
title: "Aspose::Words::Tables::CellFormat::SetPaddings metodo"
linktitle: "SetPaddings"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::CellFormat::SetPaddings metodo. Imposta la quantità di spazio (in punti) da aggiungere a sinistra/sopra/destra/sotto il contenuto della cella in C++."
type: docs
weight: 31000
url: /it/cpp/aspose.words.tables/cellformat/setpaddings/
---
## CellFormat::SetPaddings method


Imposta la quantità di spazio (in punti) da aggiungere a sinistra/sopra/destra/sotto del contenuto della cella.

```cpp
void Aspose::Words::Tables::CellFormat::SetPaddings(double leftPadding, double topPadding, double rightPadding, double bottomPadding)
```


## Esempi



Mostra come aggiungere spaziatura al contenuto di una cella con spazi bianchi.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Imposta una distanza di riempimento (in punti) tra il bordo e il contenuto del testo
// di ogni cella di tabella che creiamo con il document builder.
builder->get_CellFormat()->SetPaddings(5, 10, 40, 50);

// Crea una tabella con una cella il cui contenuto avrà un riempimento di spazi bianchi.
builder->StartTable();
builder->InsertCell();
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ") + u"Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc->Save(get_ArtifactsDir() + u"CellFormat.Padding.docx");
```

## Vedi anche

* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
