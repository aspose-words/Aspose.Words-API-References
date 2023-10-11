---
title: Enum ChapterPageSeparator
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.ChapterPageSeparator enum. Definisce il carattere separatore che appare tra il capitolo e il numero di pagina.
type: docs
weight: 200
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
| Hyphen | `0` | I due punti. |
| Period | `1` | Un punto. |
| Colon | `2` | I due punti. |
| EmDash | `3` | Un trattino enfatizzato. |
| EnDash | `4` | Un trattino standard. |

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

* class [PageSetup](../pagesetup/)
* property [ChapterPageSeparator](../pagesetup/chapterpageseparator/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)


