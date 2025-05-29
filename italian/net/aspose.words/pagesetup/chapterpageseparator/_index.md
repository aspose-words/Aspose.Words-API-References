---
title: PageSetup.ChapterPageSeparator
linktitle: ChapterPageSeparator
articleTitle: ChapterPageSeparator
second_title: Aspose.Words per .NET
description: Scopri la proprietà ChapterPageSeparator in PageSetup. Personalizza facilmente il carattere separatore tra i numeri di capitolo e di pagina per un aspetto più curato.
type: docs
weight: 90
url: /it/net/aspose.words/pagesetup/chapterpageseparator/
---
## PageSetup.ChapterPageSeparator property

Ottiene o imposta il carattere separatore che appare tra il numero del capitolo e il numero di pagina.

```csharp
public ChapterPageSeparator ChapterPageSeparator { get; set; }
```

## Osservazioni

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

* enum [ChapterPageSeparator](../../chapterpageseparator/)
* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
