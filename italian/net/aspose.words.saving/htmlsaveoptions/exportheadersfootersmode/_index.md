---
title: HtmlSaveOptions.ExportHeadersFootersMode
linktitle: ExportHeadersFootersMode
articleTitle: ExportHeadersFootersMode
second_title: Aspose.Words per .NET
description: Scopri come la proprietà ExportHeadersFootersMode di HtmlSaveOptions ottimizza l'output di intestazioni e piè di pagina per i formati HTML, MHTML ed EPUB. Massimizza la presentazione del tuo documento!
type: docs
weight: 160
url: /it/net/aspose.words.saving/htmlsaveoptions/exportheadersfootersmode/
---
## HtmlSaveOptions.ExportHeadersFootersMode property

Specifica come le intestazioni e i piè di pagina vengono emessi in HTML, MHTML o EPUB. Il valore predefinito èPerSection per HTML/MHTML eNone per EPUB.

```csharp
public ExportHeadersFootersMode ExportHeadersFootersMode { get; set; }
```

## Osservazioni

È difficile esportare intestazioni e piè di pagina in modo significativo in HTML perché il codice HTML non è suddiviso in pagine.

Quando questa proprietà èPerSection, Aspose.Words esporta solo intestazioni e piè di pagina primari all'inizio e alla fine di ogni sezione.

Quando èFirstSectionHeaderLastSectionFooter vengono esportati solo la prima intestazione primaria e l'ultimo piè di pagina primario (inclusi quelli collegati al precedente).

È possibile disabilitare completamente l'esportazione di intestazioni e piè di pagina impostando questa proprietà suNone.

## Esempi

Mostra come omettere intestazioni e piè di pagina quando si salva un documento in formato HTML.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Questo documento contiene intestazioni e piè di pagina. Possiamo accedervi tramite la raccolta "HeadersFooters".
Assert.AreEqual("First header", doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());

// Formati come .html non dividono il documento in pagine, quindi intestazioni/piè di pagina non funzioneranno allo stesso modo
// come accadrebbe se aprissimo il documento come .docx utilizzando Microsoft Word.
// Se convertiamo un documento con intestazioni/piè di pagina in HTML, la conversione assimilerà le intestazioni/piè di pagina nel corpo del testo.
// Possiamo usare un oggetto SaveOptions per omettere intestazioni e piè di pagina durante la conversione in HTML.
HtmlSaveOptions saveOptions =
    new HtmlSaveOptions(SaveFormat.Html) { ExportHeadersFootersMode = ExportHeadersFootersMode.None };

doc.Save(ArtifactsDir + "HeaderFooter.ExportMode.html", saveOptions);

// Apriamo il nostro documento salvato e verifichiamo che non contenga il testo dell'intestazione
doc = new Document(ArtifactsDir + "HeaderFooter.ExportMode.html");

Assert.IsFalse(doc.Range.Text.Contains("First header"));
```

### Guarda anche

* enum [ExportHeadersFootersMode](../../exportheadersfootersmode/)
* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
