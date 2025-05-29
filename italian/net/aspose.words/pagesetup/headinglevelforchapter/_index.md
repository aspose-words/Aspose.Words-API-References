---
title: PageSetup.HeadingLevelForChapter
linktitle: HeadingLevelForChapter
articleTitle: HeadingLevelForChapter
second_title: Aspose.Words per .NET
description: Scopri la proprietà PageSetup HeadingLevelForChapter per personalizzare facilmente gli stili dei titoli dei capitoli nel tuo documento, migliorando così la leggibilità e la professionalità.
type: docs
weight: 180
url: /it/net/aspose.words/pagesetup/headinglevelforchapter/
---
## PageSetup.HeadingLevelForChapter property

Ottiene o imposta lo stile del livello di intestazione applicato ai titoli dei capitoli nel documento.

```csharp
public int HeadingLevelForChapter { get; set; }
```

## Osservazioni

Può essere un numero da 0 a 9. 0 indica nessun numero di capitolo se applicato al numero di pagina.

Prima di poter creare numeri di pagina che includano i numeri di capitolo, è necessario applicare un formato di struttura numerata alle intestazioni del documento.

## Esempi

Mostra come lavorare con i capitoli di pagina.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

PageSetup pageSetup = doc.FirstSection.PageSetup;

pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;
pageSetup.ChapterPageSeparator = Aspose.Words.ChapterPageSeparator.Colon;
pageSetup.HeadingLevelForChapter = 1;
```

### Guarda anche

* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
