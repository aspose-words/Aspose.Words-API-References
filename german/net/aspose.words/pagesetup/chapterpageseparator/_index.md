---
title: PageSetup.ChapterPageSeparator
linktitle: ChapterPageSeparator
articleTitle: ChapterPageSeparator
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „ChapterPageSeparator“ in „PageSetup“. Passen Sie das Trennzeichen zwischen Kapitel- und Seitenzahlen ganz einfach an, um ein ansprechendes Erscheinungsbild zu erzielen.
type: docs
weight: 90
url: /de/net/aspose.words/pagesetup/chapterpageseparator/
---
## PageSetup.ChapterPageSeparator property

Ruft das Trennzeichen ab, das zwischen der Kapitelnummer und der Seitenzahl angezeigt wird, oder legt dieses fest.

```csharp
public ChapterPageSeparator ChapterPageSeparator { get; set; }
```

## Bemerkungen

Bevor Sie Seitenzahlen erstellen können, die Kapitelnummern enthalten, muss auf die Dokumentüberschriften ein nummeriertes Gliederungsformat angewendet werden.

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

* enum [ChapterPageSeparator](../../chapterpageseparator/)
* class [PageSetup](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
