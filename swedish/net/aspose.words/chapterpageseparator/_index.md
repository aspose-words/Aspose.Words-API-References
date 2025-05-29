---
title: ChapterPageSeparator Enum
linktitle: ChapterPageSeparator
articleTitle: ChapterPageSeparator
second_title: Aspose.Words för .NET
description: Upptäck enumereringen Aspose.Words.ChapterPageSeparator för att anpassa kapitel- och sidnummeravgränsare för förbättrad dokumentformatering och tydlighet.
type: docs
weight: 390
url: /sv/net/aspose.words/chapterpageseparator/
---
## ChapterPageSeparator enumeration

Definierar avgränsartecknet som visas mellan kapitel- och sidnumret.

```csharp
public enum ChapterPageSeparator
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Hyphen | `0` | Ett kolon. |
| Period | `1` | En punkt. |
| Colon | `2` | Ett kolon. |
| EmDash | `3` | Ett betonat bindestreck. |
| EnDash | `4` | Ett vanligt streck. |

## Exempel

Visar hur man arbetar med sidkapitel.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

PageSetup pageSetup = doc.FirstSection.PageSetup;

pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;
pageSetup.ChapterPageSeparator = Aspose.Words.ChapterPageSeparator.Colon;
pageSetup.HeadingLevelForChapter = 1;
```

### Se även

* class [PageSetup](../pagesetup/)
* property [ChapterPageSeparator](../pagesetup/chapterpageseparator/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
