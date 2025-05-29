---
title: ChapterPageSeparator Enum
linktitle: ChapterPageSeparator
articleTitle: ChapterPageSeparator
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.ChapterPageSeparator, um Kapitel- und Seitenzahlentrennzeichen für eine verbesserte Dokumentformatierung und -übersichtlichkeit anzupassen.
type: docs
weight: 390
url: /de/net/aspose.words/chapterpageseparator/
---
## ChapterPageSeparator enumeration

Definiert das Trennzeichen, das zwischen der Kapitel- und der Seitenzahl erscheint.

```csharp
public enum ChapterPageSeparator
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Hyphen | `0` | Ein Doppelpunkt. |
| Period | `1` | Ein Punkt. |
| Colon | `2` | Ein Doppelpunkt. |
| EmDash | `3` | Ein hervorgehobener Gedankenstrich. |
| EnDash | `4` | Ein Standardstrich. |

## Beispiele

Zeigt, wie mit Seitenkapiteln gearbeitet wird.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

PageSetup pageSetup = doc.FirstSection.PageSetup;

pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;
pageSetup.ChapterPageSeparator = Aspose.Words.ChapterPageSeparator.Colon;
pageSetup.HeadingLevelForChapter = 1;
```

### Siehe auch

* class [PageSetup](../pagesetup/)
* property [ChapterPageSeparator](../pagesetup/chapterpageseparator/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
