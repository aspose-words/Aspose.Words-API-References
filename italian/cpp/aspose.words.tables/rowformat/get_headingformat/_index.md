---
title: "Aspose::Words::Tables::RowFormat::get_HeadingFormat metodo"
linktitle: "get_HeadingFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::RowFormat::get_HeadingFormat metodo. Vero se la riga è ripetuta come intestazione della tabella su ogni pagina quando la tabella si estende su più di una pagina in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.tables/rowformat/get_headingformat/
---
## RowFormat::get_HeadingFormat method


Vero se la riga viene ripetuta come intestazione della tabella su ogni pagina quando la tabella si estende su più di una pagina.

```cpp
bool Aspose::Words::Tables::RowFormat::get_HeadingFormat()
```


## Esempi



Mostra come creare una tabella con righe che si ripetono su ogni pagina.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// Qualsiasi riga inserita mentre il flag "HeadingFormat" è impostato su "true"
// apparirà nella parte superiore della tabella su ogni pagina che essa copre.
builder->get_RowFormat()->set_HeadingFormat(true);
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->get_CellFormat()->set_Width(100);
builder->InsertCell();
builder->Write(u"Heading row 1");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Heading row 2");
builder->EndRow();

builder->get_CellFormat()->set_Width(50);
builder->get_ParagraphFormat()->ClearFormatting();
builder->get_RowFormat()->set_HeadingFormat(false);

// Aggiungi sufficienti righe affinché la tabella copra due pagine.
for (int32_t i = 0; i < 50; i++)
{
    builder->InsertCell();
    builder->Write(System::String::Format(u"Row {0}, column 1.", table->get_Rows()->get_Count()));
    builder->InsertCell();
    builder->Write(System::String::Format(u"Row {0}, column 2.", table->get_Rows()->get_Count()));
    builder->EndRow();
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableSetHeadingRow.docx");
```

## Vedi anche

* Class [RowFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
