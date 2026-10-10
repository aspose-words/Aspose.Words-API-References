---
title: "Aspose::Words::Tables::CellFormat::get_VerticalMerge metodo"
linktitle: "get_VerticalMerge"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::CellFormat::get_VerticalMerge metodo. Specifica come la cella viene unita ad altre celle verticalmente in C++."
type: docs
weight: 14000
url: /it/cpp/aspose.words.tables/cellformat/get_verticalmerge/
---
## CellFormat::get_VerticalMerge method


Specifica come la cella viene unita ad altre celle verticalmente.

```cpp
Aspose::Words::Tables::CellMerge Aspose::Words::Tables::CellFormat::get_VerticalMerge()
```

## Note


Le celle possono essere unite verticalmente solo se i loro bordi sinistro e destro sono identici.

Quando le celle sono unite verticalmente, le aree di visualizzazione delle celle unite vengono consolidate. L'area consolidata è usata per visualizzare il contenuto della prima cella unita verticalmente e tutte le altre celle unite verticalmente devono essere vuote.

## Esempi



Mostra come unire le celle della tabella verticalmente.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci una cella nella prima colonna della prima riga.
// Questa cella sarà la prima in un intervallo di celle unite verticalmente.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::First);
builder->Write(u"Text in merged cells.");

// Inserisci una cella nella seconda colonna della prima riga, poi termina la riga.
// Inoltre, configura il builder per disabilitare l'unione verticale nelle celle create.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::None);
builder->Write(u"Text in unmerged cell.");
builder->EndRow();

// Inserisci una cella nella prima colonna della seconda riga.
// Invece di aggiungere contenuti di testo, uniremo questa cella con la prima cella che abbiamo aggiunto direttamente sopra.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::Previous);

// Inserisci un'altra cella indipendente nella seconda colonna della seconda riga.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::None);
builder->Write(u"Text in unmerged cell.");
builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"CellFormat.VerticalMerge.docx");
```

## Vedi anche

* Enum [CellMerge](../../cellmerge/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
