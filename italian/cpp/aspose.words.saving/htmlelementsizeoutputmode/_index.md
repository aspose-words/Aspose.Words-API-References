---
title: "Aspose::Words::Saving::HtmlElementSizeOutputMode enum"
linktitle: "HtmlElementSizeOutputMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlElementSizeOutputMode enum. Specifica come Aspose.Words esporta larghezze e altezze degli elementi in HTML, MHTML ed EPUB in C++."
type: docs
weight: 58000
url: /it/cpp/aspose.words.saving/htmlelementsizeoutputmode/
---
## HtmlElementSizeOutputMode enum


Specifica come Aspose.Words esporta le larghezze e le altezze degli elementi in HTML, MHTML e EPUB.

```cpp
enum class HtmlElementSizeOutputMode
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Tutti | 0 | Tutte le dimensioni degli elementi, sia in unità assolute che relative, specificate nel documento sono esportate. |
| RelativeOnly | 1 | Le dimensioni degli elementi vengono esportate solo se sono specificate in unità relative nel documento. Le dimensioni fisse non vengono esportate in questa modalità. Gli agenti visivi calcoleranno le dimensioni mancanti per rendere il layout del documento più naturale. |
| None | 2 | Le dimensioni degli elementi non vengono esportate. Gli agenti visivi costruiranno il layout automaticamente in base alla relazione tra gli elementi. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
