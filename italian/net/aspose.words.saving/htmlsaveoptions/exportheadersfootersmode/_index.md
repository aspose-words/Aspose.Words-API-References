---
title: HtmlSaveOptions.ExportHeadersFootersMode
linktitle: ExportHeadersFootersMode
articleTitle: ExportHeadersFootersMode
second_title: Aspose.Words per .NET
description: HtmlSaveOptions ExportHeadersFootersMode proprietà. Specifica la modalità di output di intestazioni e piè di pagina in HTML MHTML o EPUB. Il valore predefinito èPerSection per HTML/MHTML eNone per EPUB in C#.
type: docs
weight: 160
url: /it/net/aspose.words.saving/htmlsaveoptions/exportheadersfootersmode/
---
## HtmlSaveOptions.ExportHeadersFootersMode property

Specifica la modalità di output di intestazioni e piè di pagina in HTML, MHTML o EPUB. Il valore predefinito èPerSection per HTML/MHTML eNone per EPUB.

```csharp
public ExportHeadersFootersMode ExportHeadersFootersMode { get; set; }
```

## Osservazioni

È difficile restituire intestazioni e piè di pagina in modo significativo in HTML perché l'HTML non è impaginato.

Quando questa proprietà èPerSection, Aspose.Words exports solo intestazioni e piè di pagina primari all'inizio e alla fine di ogni sezione.

Quando èFirstSectionHeaderLastSectionFooter vengono esportati solo la prima intestazione principale e l'ultimo piè di pagina principale (incluso quello collegato al precedente).

Puoi disabilitare del tutto l'esportazione di intestazioni e piè di pagina impostando questa proprietà suNone.

## Esempi

Mostra come omettere intestazioni/piè di pagina quando si salva un documento in HTML.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Questo documento contiene intestazioni e piè di pagina. Possiamo accedervi tramite la raccolta "HeadersFooters".
Assert.AreEqual("First header", doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());

// Formati come .html non dividono il documento in pagine, quindi intestazioni/piè di pagina non funzioneranno allo stesso modo
// lo farebbero quando apriamo il documento come .docx utilizzando Microsoft Word.
// Se convertiamo un documento con intestazioni/piè di pagina in html, la conversione assimilerà le intestazioni/piè di pagina nel corpo del testo.
// Possiamo utilizzare un oggetto SaveOptions per omettere intestazioni/piè di pagina durante la conversione in html.
HtmlSaveOptions saveOptions =
    new HtmlSaveOptions(SaveFormat.Html) { ExportHeadersFootersMode = ExportHeadersFootersMode.None };

doc.Save(ArtifactsDir + "HeaderFooter.ExportMode.html", saveOptions);

// Apri il nostro documento salvato e verifica che non contenga il testo dell'intestazione
doc = new Document(ArtifactsDir + "HeaderFooter.ExportMode.html");

Assert.IsFalse(doc.Range.Text.Contains("First header"));
```

### Guarda anche

* enum [ExportHeadersFootersMode](../../exportheadersfootersmode/)
* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
