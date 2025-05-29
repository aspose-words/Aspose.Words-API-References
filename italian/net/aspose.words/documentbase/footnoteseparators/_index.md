---
title: DocumentBase.FootnoteSeparators
linktitle: FootnoteSeparators
articleTitle: FootnoteSeparators
second_title: Aspose.Words per .NET
description: Accedi e personalizza i separatori delle note a piè di pagina e delle note di chiusura nel tuo documento con la proprietà FootnoteSeparators di DocumentBase per un controllo avanzato della formattazione.
type: docs
weight: 40
url: /it/net/aspose.words/documentbase/footnoteseparators/
---
## DocumentBase.FootnoteSeparators property

Fornisce l'accesso ai separatori di note a piè di pagina/note di chiusura definiti nel documento.

```csharp
public FootnoteSeparatorCollection FootnoteSeparators { get; }
```

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

* class [FootnoteSeparatorCollection](../../../aspose.words.notes/footnoteseparatorcollection/)
* class [DocumentBase](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
