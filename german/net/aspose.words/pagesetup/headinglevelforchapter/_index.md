---
title: PageSetup.HeadingLevelForChapter
linktitle: HeadingLevelForChapter
articleTitle: HeadingLevelForChapter
second_title: Aspose.Words für .NET
description: Entdecken Sie die PageSetup HeadingLevelForChapter-Eigenschaft, um die Kapitelüberschriftenstile in Ihrem Dokument einfach anzupassen und so die Lesbarkeit und Professionalität zu verbessern.
type: docs
weight: 180
url: /de/net/aspose.words/pagesetup/headinglevelforchapter/
---
## PageSetup.HeadingLevelForChapter property

Ruft den Überschriftenebenenstil ab oder legt ihn fest, der auf die Kapitelüberschriften im Dokument angewendet wird.

```csharp
public int HeadingLevelForChapter { get; set; }
```

## Bemerkungen

Kann eine Zahl zwischen 0 und 9 sein. 0 bedeutet keine Kapitelnummer, wenn es auf die Seitenzahl angewendet wird.

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

* class [PageSetup](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
