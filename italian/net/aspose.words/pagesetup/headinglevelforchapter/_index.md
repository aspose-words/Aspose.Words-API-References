---
title: PageSetup.HeadingLevelForChapter
second_title: Aspose.Words per .NET API Reference
description: PageSetup proprietà. Ottiene o imposta lo stile del livello di intestazione applicato ai titoli dei capitoli nel documento.
type: docs
weight: 180
url: /it/net/aspose.words/pagesetup/headinglevelforchapter/
---
## PageSetup.HeadingLevelForChapter property

Ottiene o imposta lo stile del livello di intestazione applicato ai titoli dei capitoli nel documento.

```csharp
public int HeadingLevelForChapter { get; set; }
```

### Osservazioni

Può essere un numero compreso tra 0 e 9. 0 significa nessun numero di capitolo se applicato al numero di pagina.

Prima di poter creare numeri di pagina che includano numeri di capitolo, è necessario che alle intestazioni del documento sia applicato un formato struttura numerata.

### Esempi

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
* spazio dei nomi [Aspose.Words](../../pagesetup/)
* assemblea [Aspose.Words](../../../)


