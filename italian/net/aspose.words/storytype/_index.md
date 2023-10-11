---
title: Enum StoryType
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.StoryType enum. Il testo di un documento Word è archiviato in brani.StoryType identifica una storia.
type: docs
weight: 6120
url: /it/net/aspose.words/storytype/
---
## StoryType enumeration

Il testo di un documento Word è archiviato in brani.`StoryType` identifica una storia.

```csharp
public enum StoryType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Valore predefinito. Non c'è una storia del genere nel documento. |
| MainText | `1` | Contiene il testo principale del documento, rappresentato da[`Body`](../body/) . |
| Footnotes | `2` | Contiene il testo della nota a piè di pagina, rappresentato da[`Footnote`](../../aspose.words.notes/footnote/) . |
| Endnotes | `3` | Contiene il testo delle note di chiusura, rappresentato da[`Footnote`](../../aspose.words.notes/footnote/) . |
| Comments | `4` | Contiene commenti al documento (annotazioni), rappresentati da[`Comment`](../comment/) . |
| Textbox | `5` | Contiene testo in forma o casella di testo, rappresentato da[`Shape`](../../aspose.words.drawing/shape/) . |
| EvenPagesHeader | `6` | Contiene il testo dell'intestazione delle pagine pari, rappresentato da[`HeaderFooter`](../headerfooter/) . |
| PrimaryHeader | `7` | Contiene il testo dell'intestazione primaria. Quando l'intestazione è diversa per le pagine pari e dispari, contiene il testo dell'intestazione delle pagine dispari. Rappresentata da[`HeaderFooter`](../headerfooter/) . |
| EvenPagesFooter | `8` | Contiene il testo del piè di pagina delle pagine pari, rappresentato da[`HeaderFooter`](../headerfooter/) . |
| PrimaryFooter | `9` | Contiene il testo del piè di pagina principale. Quando il piè di pagina è diverso per le pagine pari e dispari, contiene il testo del piè di pagina delle pagine dispari. Rappresentata da[`HeaderFooter`](../headerfooter/) . |
| FirstPageHeader | `10` | Contiene il testo dell'intestazione della prima pagina, rappresentato da[`HeaderFooter`](../headerfooter/) . |
| FirstPageFooter | `11` | Contiene il testo del piè di pagina della prima pagina, rappresentato da[`HeaderFooter`](../headerfooter/) . |
| FootnoteSeparator | `12` | Contiene il testo del separatore delle note a piè di pagina, rappresentato daFootnoteSeparator . |
| FootnoteContinuationSeparator | `13` | Contiene il testo del separatore di continuazione della nota, rappresentato daFootnoteSeparator . |
| FootnoteContinuationNotice | `14` | Contiene il testo del separatore dell'avviso di continuazione della nota, rappresentato daFootnoteSeparator . |
| EndnoteSeparator | `15` | Contiene il testo del separatore della nota di chiusura, rappresentato daFootnoteSeparator . |
| EndnoteContinuationSeparator | `16` | Contiene il testo del separatore di continuazione della nota di chiusura, rappresentato daFootnoteSeparator . |
| EndnoteContinuationNotice | `17` | Contiene il testo del separatore dell'avviso di continuazione della nota di chiusura, rappresentato daFootnoteSeparator . |

### Esempi

Mostra come rimuovere tutte le forme da un nodo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Utilizza un DocumentBuilder per inserire una forma. Questa è una forma in linea,
// che ha un Paragrafo genitore, che è un nodo figlio del Corpo della prima sezione.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// Possiamo eliminare tutte le forme dai paragrafi figlio di questo Body.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)


