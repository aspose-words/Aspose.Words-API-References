---
title: "Metodo Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers"
linktitle: "get_ExportTocPageNumbers"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers. Specifica se scrivere i numeri di pagina nell'indice durante il salvataggio in HTML, MHTML ed EPUB. Il valore predefinito è false in C++."
type: docs
weight: 29000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_exporttocpagenumbers/
---
## HtmlSaveOptions::get_ExportTocPageNumbers method


Specifica se scrivere i numeri di pagina nel sommario durante il salvataggio in HTML, MHTML e EPUB. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers() const
```


## Esempi



Mostra come visualizzare i numeri di pagina quando si salva un documento con un indice in .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci un indice, quindi popola il documento con paragrafi formattati usando un "Heading"
// stile che l'indice rileverà come voci. Ogni voce mostrerà il paragrafo di intestazione a sinistra,
// e il numero di pagina che contiene l'intestazione a destra.
auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));

builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 1"));
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Entry 1");
builder->Writeln(u"Entry 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Entry 3");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Entry 4");
fieldToc->UpdatePageNumbers();
doc->UpdateFields();

// I documenti HTML non hanno pagine. Se salviamo questo documento in HTML,
// i numeri di pagina che il nostro indice visualizza non avranno alcun significato.
// Quando salviamo il documento in HTML, possiamo passare un oggetto SaveOptions per omettere questi numeri di pagina dall'indice.
// Se impostiamo il flag "ExportTocPageNumbers" su "true",
// ogni voce dell'indice visualizzerà l'intestazione, il separatore e il numero di pagina, preservandone l'aspetto in Microsoft Word.
// Se impostiamo il flag "ExportTocPageNumbers" su "false",
// l'operazione di salvataggio ometterà sia il separatore sia il numero di pagina e lascerà intatta l'intestazione per ogni voce.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportTocPageNumbers(exportTocPageNumbers);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportTocPageNumbers.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportTocPageNumbers.html");

if (exportTocPageNumbers)
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<span>Entry 1</span>") + u"<span style=\"width:428.14pt; font-family:'Lucida Console'; font-size:10pt; display:inline-block; -aw-font-family:'Times New Roman'; " + u"-aw-tabstop-align:right; -aw-tabstop-leader:dots; -aw-tabstop-pos:469.8pt\">.......................................................................</span>" + u"<span>2</span>" + u"</p>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") + u"<span>Entry 2</span>" + u"</p>"));
}
```

## Vedi anche

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
