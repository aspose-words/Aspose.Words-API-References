---
title: PageSetup.HeadingLevelForChapter
second_title: Aspose.Words für .NET-API-Referenz
description: PageSetup eigendom. Ruft den Stil der Überschriftenebene ab der auf die Kapiteltitel im Dokument angewendet wird oder legt diesen fest.
type: docs
weight: 180
url: /de/net/aspose.words/pagesetup/headinglevelforchapter/
---
## PageSetup.HeadingLevelForChapter property

Ruft den Stil der Überschriftenebene ab, der auf die Kapiteltitel im Dokument angewendet wird, oder legt diesen fest.

```csharp
public int HeadingLevelForChapter { get; set; }
```

### Bemerkungen

Kann eine Zahl von 0 bis 9 sein. 0 bedeutet keine Kapitelnummer, wenn es auf die Seitennummer angewendet wird.

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

* class [PageSetup](../)
* namensraum [Aspose.Words](../../pagesetup/)
* Montage [Aspose.Words](../../../)


