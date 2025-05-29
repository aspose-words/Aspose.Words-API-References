---
title: ChapterPageSeparator Enum
linktitle: ChapterPageSeparator
articleTitle: ChapterPageSeparator
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.ChapterPageSeparator per personalizzare i separatori dei numeri di capitolo e di pagina per migliorare la formattazione e la chiarezza del documento.
type: docs
weight: 390
url: /it/net/aspose.words/chapterpageseparator/
---
## ChapterPageSeparator enumeration

Definisce il carattere separatore che appare tra il capitolo e il numero di pagina.

```csharp
public enum ChapterPageSeparator
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Hyphen | `0` | Due punti. |
| Period | `1` | Un periodo. |
| Colon | `2` | Due punti. |
| EmDash | `3` | Un trattino enfatizzato. |
| EnDash | `4` | Un trattino standard. |

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

* class [PageSetup](../pagesetup/)
* property [ChapterPageSeparator](../pagesetup/chapterpageseparator/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
