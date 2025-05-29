---
title: DocumentSplitCriteria Enum
linktitle: DocumentSplitCriteria
articleTitle: DocumentSplitCriteria
second_title: Aspose.Words per .NET
description: Scopri come Aspose.Words.Saving.DocumentSplitCriteria migliora la suddivisione dei documenti per ottenere formati HTML, Epub e Azw3 ottimali. Semplifica il tuo processo di salvataggio!
type: docs
weight: 5710
url: /it/net/aspose.words.saving/documentsplitcriteria/
---
## DocumentSplitCriteria enumeration

Specifica come il documento viene suddiviso in parti durante il salvataggioHtml , Epub OAzw3 formato.

```csharp
[Flags]
public enum DocumentSplitCriteria
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Il documento non è diviso. |
| PageBreak | `1` | Il documento è diviso in parti con interruzioni di pagina esplicite. Un'interruzione di pagina può essere specificata da un[`PageBreak`](../../aspose.words/controlchar/pagebreak/) carattere, un'interruzione di sezione che specifica l'inizio di una nuova sezione su una nuova pagina, o un paragrafo che ha il suo[`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/) proprietà impostata su`VERO` . |
| ColumnBreak | `2` | Il documento viene diviso in parti in base alle interruzioni di colonna. Un'interruzione di colonna può essere specificata da un[`ColumnBreak`](../../aspose.words/controlchar/columnbreak/) carattere or un'interruzione di sezione che specifica l'inizio di una nuova sezione in una nuova colonna. |
| SectionBreak | `4` | Il documento è diviso in parti in corrispondenza di un'interruzione di sezione di qualsiasi tipo. |
| HeadingParagraph | `8` | Il documento è diviso in parti in un paragrafo formattato utilizzando uno stile di intestazione**Titolo 1** ,**Titolo 2** ecc. Da usare insieme a[`DocumentSplitHeadingLevel`](../htmlsaveoptions/documentsplitheadinglevel/) per specificare i livelli di intestazione (da 1 al livello specificato) in cui effettuare la divisione. |

## Osservazioni

`DocumentSplitCriteria`è un insieme di flag che possono essere combinati. Ad esempio, è possibile suddividere il documento document in interruzioni di pagina e in intestazioni di paragrafo nella stessa operazione di esportazione.

Diversi criteri possono sovrapporsi parzialmente. Ad esempio,**Titolo 1** allo stile viene spesso assegnato [`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/) proprietà, quindi rientra in due criteri:PageBreak e HeadingParagraphAlcune interruzioni di sezione possono causare interruzioni di pagina e così via. In casi tipici, specificare un solo flag è l'opzione più pratica.

## Esempi

Mostra come utilizzare una codifica specifica quando si salva un documento in formato .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Utilizzare un oggetto SaveOptions per specificare la codifica per un documento che salveremo.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Per impostazione predefinita, un documento .epub di output avrà tutto il suo contenuto in una parte HTML.
// Un criterio di suddivisione consente di segmentare il documento in più parti HTML.
// Imposteremo i criteri per suddividere il documento in paragrafi di intestazione.
// Questa funzione è utile per i lettori che non riescono a leggere file HTML di dimensioni superiori a una determinata soglia.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Specificare che si desidera esportare le proprietà del documento.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
