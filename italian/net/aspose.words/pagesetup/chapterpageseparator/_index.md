---
title: PageSetup.ChapterPageSeparator
second_title: Aspose.Words per .NET API Reference
description: PageSetup proprietà. Ottiene o imposta il carattere separatore visualizzato tra il numero del capitolo e il numero della pagina.
type: docs
weight: 90
url: /it/net/aspose.words/pagesetup/chapterpageseparator/
---
## PageSetup.ChapterPageSeparator property

Ottiene o imposta il carattere separatore visualizzato tra il numero del capitolo e il numero della pagina.

```csharp
public ChapterPageSeparator ChapterPageSeparator { get; set; }
```

### Osservazioni

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

* enum [ChapterPageSeparator](../../chapterpageseparator/)
* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../pagesetup/)
* assemblea [Aspose.Words](../../../)


