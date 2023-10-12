---
title: PageSetup.ChapterPageSeparator
second_title: Aspose.Words für .NET-API-Referenz
description: PageSetup eigendom. Ruft das Trennzeichen ab das zwischen der Kapitelnummer und der Seitennummer angezeigt wird oder legt dieses fest.
type: docs
weight: 90
url: /de/net/aspose.words/pagesetup/chapterpageseparator/
---
## PageSetup.ChapterPageSeparator property

Ruft das Trennzeichen ab, das zwischen der Kapitelnummer und der Seitennummer angezeigt wird, oder legt dieses fest.

```csharp
public ChapterPageSeparator ChapterPageSeparator { get; set; }
```

### Bemerkungen

Bevor Sie Seitenzahlen erstellen können, die Kapitelnummern enthalten, muss auf die Dokumentüberschriften ein nummeriertes Gliederungsformat angewendet werden.

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

* enum [ChapterPageSeparator](../../chapterpageseparator/)
* class [PageSetup](../)
* namensraum [Aspose.Words](../../pagesetup/)
* Montage [Aspose.Words](../../../)


