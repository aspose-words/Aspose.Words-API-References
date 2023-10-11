---
title: Enum ChapterPageSeparator
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.ChapterPageSeparator opsomming. Definiert das Trennzeichen das zwischen Kapitel und Seitenzahl erscheint.
type: docs
weight: 200
url: /de/net/aspose.words/chapterpageseparator/
---
## ChapterPageSeparator enumeration

Definiert das Trennzeichen, das zwischen Kapitel und Seitenzahl erscheint.

```csharp
public enum ChapterPageSeparator
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Hyphen | `0` | Ein Doppelpunkt. |
| Period | `1` | Ein Punkt. |
| Colon | `2` | Ein Doppelpunkt. |
| EmDash | `3` | Ein betonter Strich. |
| EnDash | `4` | Ein Standard-Armaturenbrett. |

### Beispiele

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


