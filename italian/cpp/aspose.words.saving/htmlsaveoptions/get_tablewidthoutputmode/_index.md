---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode metodo"
linktitle: "get_TableWidthOutputMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode metodo. Controlla come le larghezze di tabelle, righe e celle vengono esportate in HTML, MHTML o EPUB. Il valore predefinito è All in C++."
type: docs
weight: 47000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_tablewidthoutputmode/
---
## HtmlSaveOptions::get_TableWidthOutputMode method


Controlla come le larghezze di tabelle, righe e celle vengono esportate in HTML, MHTML o EPUB. Il valore predefinito è [All](../../htmlelementsizeoutputmode/).

```cpp
Aspose::Words::Saving::HtmlElementSizeOutputMode Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode() const
```

## Note


Nel formato HTML, gli elementi di tabella, riga e cella (**%<table>**, **%<tr>**, **%<th>**, **%<td>**) possono avere le loro larghezze specificate sia in unità relative (percentuale) sia in unità assolute. In un documento in Aspose.Words, tabelle, righe e celle possono avere le loro larghezze specificate anch'esse usando unità relative o assolute.

Quando converti un documento in HTML usando Aspose.Words, potresti voler controllare come le larghezze di tabelle, righe e celle vengono esportate per influenzare il modo in cui il documento risultante viene visualizzato nell'agente visivo (ad es. un browser o un visualizzatore).

Usa questa proprietà come filtro per specificare quali valori di larghezza delle tabelle vengono esportati nel documento di destinazione. Ad esempio, se stai convertendo un documento in EPUB e intendi visualizzarlo su un dispositivo di lettura mobile, probabilmente vorrai evitare di esportare valori di larghezza assoluti. Per farlo, devi specificare la modalità di output [RelativeOnly](../../htmlelementsizeoutputmode/) o [None](../../htmlelementsizeoutputmode/) affinché il visualizzatore sul dispositivo mobile possa impaginare la tabella per adattarla alla larghezza dello schermo al meglio.

## Esempi



Mostra come preservare i rientri negativi nell'output .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci una tabella con un rientro negativo, che la sposterà a sinistra oltre il limite sinistro della pagina.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2");
builder->EndTable();
table->set_LeftIndent(-36);
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(144));

builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);

// Inserisci una tabella con un rientro positivo, che sposterà la tabella a destra.
table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2");
builder->EndTable();
table->set_LeftIndent(36);
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(144));

// Quando salviamo un documento in HTML, Aspose.Words preserverà solo i rientri negativi
// come quello che abbiamo applicato alla prima tabella se impostiamo il flag "AllowNegativeIndent"
// in un oggetto SaveOptions che imposteremo su "true".
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_AllowNegativeIndent(allowNegativeIndent);
options->set_TableWidthOutputMode(Aspose::Words::Saving::HtmlElementSizeOutputMode::RelativeOnly);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.NegativeIndent.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.NegativeIndent.html");

if (allowNegativeIndent)
{
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:-41.65pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
```

## Vedi anche

* Enum [HtmlElementSizeOutputMode](../../htmlelementsizeoutputmode/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
