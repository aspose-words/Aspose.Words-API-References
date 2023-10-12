---
title: Enum ExportHeadersFootersMode
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Saving.ExportHeadersFootersMode enum. Specifica la modalità di esportazione di intestazioni e piè di pagina in HTML MHTML o EPUB.
type: docs
weight: 5000
url: /it/net/aspose.words.saving/exportheadersfootersmode/
---
## ExportHeadersFootersMode enumeration

Specifica la modalità di esportazione di intestazioni e piè di pagina in HTML, MHTML o EPUB.

```csharp
public enum ExportHeadersFootersMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Intestazioni e piè di pagina non vengono esportati. |
| PerSection | `1` | Le intestazioni e i piè di pagina principali vengono esportati all'inizio e alla fine di ogni sezione. |
| FirstSectionHeaderLastSectionFooter | `2` | L'intestazione principale della prima sezione viene esportata all'inizio del documento e il piè di pagina principale è alla fine. |
| FirstPageHeaderFooterPerSection | `3` | L'intestazione e il piè di pagina della prima pagina vengono esportati all'inizio e alla fine di ogni sezione. |

### Esempi

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

* property [ExportHeadersFootersMode](../htmlsaveoptions/exportheadersfootersmode/)
* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)


