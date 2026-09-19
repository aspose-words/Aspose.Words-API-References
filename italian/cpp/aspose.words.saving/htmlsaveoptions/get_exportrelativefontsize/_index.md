---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize metodo"
linktitle: "get_ExportRelativeFontSize"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize metodo. Specifica se le dimensioni dei caratteri devono essere esportate in unità relative durante il salvataggio in HTML, MHTML o EPUB. Il valore predefinito è false in C++."
type: docs
weight: 25000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_exportrelativefontsize/
---
## HtmlSaveOptions::get_ExportRelativeFontSize method


Specifica se le dimensioni dei caratteri devono essere emesse in unità relative durante il salvataggio in HTML, MHTML o EPUB. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize() const
```

## Note


In molti documenti esistenti (HTML, IDPF EPUB) le dimensioni dei caratteri sono specificate in unità relative. Questo consente alle applicazioni di regolare la dimensione del testo durante la visualizzazione/elaborazione dei documenti. Ad esempio, Microsoft Internet Explorer ha il sottomenu "View->Text Size", Adobe Digital Editions ha due pulsanti: Aumenta/Diminuisci dimensione testo. Se ti aspetti che questa funzionalità funzioni, imposta la proprietà [ExportRelativeFontSize](./) su **true**.

**Aspose**[Words](../../../aspose.words/) document model contains and operates only with absolute font size units. Relative units need additional logic to be recalculated from some initial (standard) size. [Font](../../../aspose.words/font/) size of **Normal** document style is taken as standard. For instance, if **Normal** has 12pt font and some text is 18pt then it will be output as **%1.5em.** to the HTML.

Quando questa opzione è abilitata, gli elementi del documento diversi dal testo manterranno comunque dimensioni assolute. Inoltre alcuni attributi relativi al testo potrebbero essere espressi in modo assoluto. In particolare, l'interlinea specificata con la regola "exactly" potrebbe produrre risultati indesiderati durante il ridimensionamento del testo. Pertanto i documenti di origine dovrebbero essere progettati e testati correttamente quando si esporta con [ExportRelativeFontSize](./) impostato su **true**.

## Esempi



Mostra come utilizzare le dimensioni dei caratteri relative durante il salvataggio in .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Default font size, ");
builder->get_Font()->set_Size(24);
builder->Writeln(u"2x default font size,");
builder->get_Font()->set_Size(96);
builder->Write(u"8x default font size");

// Quando salviamo il documento in HTML, possiamo passare un oggetto SaveOptions
// per determinare se utilizzare dimensioni dei caratteri relative o assolute.
// Imposta il flag "ExportRelativeFontSize" su "true" per dichiarare le dimensioni dei caratteri
// usando l'unità di misura "em", che è un fattore che moltiplica la dimensione corrente del carattere.
// Imposta il flag "ExportRelativeFontSize" su "false" per dichiarare le dimensioni dei caratteri
// usando l'unità di misura "pt", che è la dimensione assoluta del carattere in punti.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportRelativeFontSize(exportRelativeFontSize);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.RelativeFontSize.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.RelativeFontSize.html");

if (exportRelativeFontSize)
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<body style=\"font-family:'Times New Roman'\">") + u"<div>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" + u"<span>Default font size, </span>" + u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:2em\">" + u"<span>2x default font size,</span>" + u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:8em\">" + u"<span>8x default font size</span>" + u"</p>" + u"</div>" + u"</body>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<body style=\"font-family:'Times New Roman'; font-size:12pt\">") + u"<div>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" + u"<span>Default font size, </span>" + u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:24pt\">" + u"<span>2x default font size,</span>" + u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:96pt\">" + u"<span>8x default font size</span>" + u"</p>" + u"</div>" + u"</body>"));
}
```

## Vedi anche

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
