---
title: FootnoteSeparatorType Enum
linktitle: FootnoteSeparatorType
articleTitle: FootnoteSeparatorType
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.FootnoteSeparatorType per personalizzare i separatori delle note a piè di pagina e di chiusura, migliorando la formattazione e la leggibilità del documento.
type: docs
weight: 5010
url: /it/net/aspose.words.notes/footnoteseparatortype/
---
## FootnoteSeparatorType enumeration

Specifica il tipo di separatore delle note a piè di pagina/note di chiusura.

```csharp
public enum FootnoteSeparatorType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| FootnoteSeparator | `0` | Separatore tra il testo principale e il testo della nota a piè di pagina. |
| FootnoteContinuationSeparator | `1` | Stampato sopra il testo della nota a piè di pagina su una pagina quando il testo deve essere continuato da una pagina precedente. |
| FootnoteContinuationNotice | `2` | Stampato sotto il testo della nota a piè di pagina su una pagina quando il testo della nota a piè di pagina deve continuare su una pagina successiva. |
| EndnoteSeparator | `3` | Separatore tra il testo principale e il testo della nota finale. |
| EndnoteContinuationSeparator | `4` | Stampato sopra il testo della nota finale su una pagina quando il testo deve essere continuato da una pagina precedente. |
| EndnoteContinuationNotice | `5` | Stampato sotto il testo della nota di chiusura su una pagina quando il testo della nota di chiusura deve continuare su una pagina successiva. |

## Esempi

Mostra come rimuovere il separatore delle note di chiusura.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator endnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.EndnoteSeparator];
// Rimuovi il separatore delle note di chiusura.
endnoteSeparator.FirstParagraph.FirstChild.Remove();
```

Mostra come gestire il formato del separatore delle note a piè di pagina.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator footnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.FootnoteSeparator];
// Allinea il separatore delle note a piè di pagina.
footnoteSeparator.FirstParagraph.ParagraphFormat.Alignment = ParagraphAlignment.Center;
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Notes](../../aspose.words.notes/)
* assemblea [Aspose.Words](../../)
