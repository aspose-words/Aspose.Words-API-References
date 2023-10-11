---
title: Enum DocumentSplitCriteria
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Saving.DocumentSplitCriteria enum. Specifica il modo in cui il documento viene diviso in parti durante il salvataggio inHtml  Epub OAzw3 formato.
type: docs
weight: 4960
url: /it/net/aspose.words.saving/documentsplitcriteria/
---
## DocumentSplitCriteria enumeration

Specifica il modo in cui il documento viene diviso in parti durante il salvataggio inHtml , Epub OAzw3 formato.

```csharp
[Flags]
public enum DocumentSplitCriteria
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Il documento non è diviso. |
| PageBreak | `1` | Il documento viene diviso in parti in corrispondenza di interruzioni di pagina esplicite. Un'interruzione di pagina può essere specificata da[`PageBreak`](../../aspose.words/controlchar/pagebreak/) carattere, un'interruzione di sezione che specifica l'inizio di una nuova sezione su una nuova pagina, o un paragrafo che ha il suo[`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/) proprietà impostata su`VERO` . |
| ColumnBreak | `2` | Il documento viene diviso in parti in corrispondenza delle interruzioni di colonna. Un'interruzione di colonna può essere specificata da[`ColumnBreak`](../../aspose.words/controlchar/columnbreak/) carattere o un'interruzione di sezione che specifica l'inizio di una nuova sezione in una nuova colonna. |
| SectionBreak | `4` | Il documento viene diviso in parti in corrispondenza di un'interruzione di sezione di qualsiasi tipo. |
| HeadingParagraph | `8` | Il documento è diviso in parti in un paragrafo formattato utilizzando uno stile di titolo **Rubrica 1** , **Rubrica 2** ecc. Da utilizzare insieme a[`DocumentSplitHeadingLevel`](../htmlsaveoptions/documentsplitheadinglevel/) per specificare i livelli di intestazione (da 1 al livello specificato) in cui dividere. |

### Osservazioni

`DocumentSplitCriteria`è un insieme di flag che possono essere combinati. Ad esempio, puoi dividere il documento nelle interruzioni di pagina e nei paragrafi di intestazione nella stessa operazione di esportazione.

Criteri diversi possono parzialmente sovrapporsi. Ad esempio, **Rubrica 1** lo stile viene spesso fornito [`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/) proprietà quindi rientra in due criteri:PageBreak e HeadingParagraph. Alcune interruzioni di sezione possono causare interruzioni di pagina e così via. Nei casi tipici, specificare un solo flag è l'opzione più pratica.

### Esempi

Mostra come utilizzare una codifica specifica quando si salva un documento in .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Utilizza un oggetto SaveOptions per specificare la codifica per un documento che salveremo.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Per impostazione predefinita, un documento .epub di output avrà tutto il suo contenuto in una parte HTML.
// Un criterio di suddivisione ci permette di segmentare il documento in più parti HTML.
// Imposteremo i criteri per suddividere il documento in paragrafi di intestazione.
// Ciò è utile per i lettori che non possono leggere file HTML più significativi di una dimensione specifica.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Specifica che vogliamo esportare le proprietà del documento.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)


