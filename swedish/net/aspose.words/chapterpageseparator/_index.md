---
title: ChapterPageSeparator Enum
linktitle: ChapterPageSeparator
articleTitle: ChapterPageSeparator
second_title: Aspose.Words för .NET
description: Aspose.Words.ChapterPageSeparator uppräkning. Definierar avgränsningstecknet som visas mellan kapitel och sidnummer i C#.
type: docs
weight: 200
url: /sv/net/aspose.words/chapterpageseparator/
---
## ChapterPageSeparator enumeration

Definierar avgränsningstecknet som visas mellan kapitel och sidnummer.

```csharp
public enum ChapterPageSeparator
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Hyphen | `0` | Ett kolon. |
| Period | `1` | En punkt. |
| Colon | `2` | Ett kolon. |
| EmDash | `3` | Ett betonat streck. |
| EnDash | `4` | Ett standardstreck. |

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
