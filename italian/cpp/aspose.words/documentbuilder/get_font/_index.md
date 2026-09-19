---
title: "Metodo Aspose::Words::DocumentBuilder::get_Font"
linktitle: "get_Font"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::DocumentBuilder::get_Font. Restituisce un oggetto che rappresenta le proprietà di formattazione del carattere corrente in C++."
type: docs
weight: 17000
url: /it/cpp/aspose.words/documentbuilder/get_font/
---
## DocumentBuilder::get_Font method


Restituisce un oggetto che rappresenta le proprietà di formattazione del carattere corrente.

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::DocumentBuilder::get_Font()
```

## Note


Usa [Font](./) per accedere e modificare le proprietà di formattazione del carattere.

Specifica la formattazione del carattere prima di inserire il testo.

## Esempi



Mostra come inserire una stringa circondata da un bordo in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```


Mostra come creare una tabella formattata usando [DocumentBuilder](../).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
table->set_LeftIndent(20);

// Imposta alcune opzioni di formattazione per il testo e l'aspetto della tabella.
builder->get_RowFormat()->set_Height(40);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::AtLeast);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::FromArgb(198, 217, 241));

builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->get_Font()->set_Size(16);
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Bold(true);

// Configurare le opzioni di formattazione in un document builder le applicherà
// alla cella/riga corrente in cui si trova il cursore,
// nonché a tutte le nuove celle e righe create usando quel builder.
builder->Write(u"Header Row,\n Cell 1");
builder->InsertCell();
builder->Write(u"Header Row,\n Cell 2");
builder->InsertCell();
builder->Write(u"Header Row,\n Cell 3");
builder->EndRow();

// Riconfigura gli oggetti di formattazione del builder per le nuove righe e celle che stiamo per creare.
// Il builder non applicherà questi alla prima riga già creata in modo che risalti come riga di intestazione.
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_White());
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->get_RowFormat()->set_Height(30);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Auto);
builder->InsertCell();
builder->get_Font()->set_Size(12);
builder->get_Font()->set_Bold(false);

builder->Write(u"Row 1, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 3.");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 2.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 3.");
builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateFormattedTable.docx");
```

## Vedi anche

* Class [Font](../../font/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
