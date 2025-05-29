---
title: FootnoteSeparatorCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words für .NET
description: Greifen Sie auf die Elementeigenschaft FootnoteSeparatorCollection zu, um einfach benutzerdefinierte FootnoteSeparators nach Typ abzurufen und so die Formatierung Ihres Dokuments zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words.notes/footnoteseparatorcollection/item/
---
## FootnoteSeparatorCollection indexer

Ruft eine[`FootnoteSeparator`](../../footnoteseparator/) des angegebenen Typs.

```csharp
public FootnoteSeparator this[FootnoteSeparatorType separatorType] { get; }
```

## Bemerkungen

Rückgaben`null` wenn das Fußnoten-/Endnotentrennzeichen des angegebenen Typs nicht gefunden wird.

## Beispiele

Zeigt, wie das Fußnotentrennzeichenformat verwaltet wird.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator footnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.FootnoteSeparator];
// Fußnotentrennzeichen ausrichten.
footnoteSeparator.FirstParagraph.ParagraphFormat.Alignment = ParagraphAlignment.Center;
```

### Siehe auch

* class [FootnoteSeparator](../../footnoteseparator/)
* enum [FootnoteSeparatorType](../../footnoteseparatortype/)
* class [FootnoteSeparatorCollection](../)
* namensraum [Aspose.Words.Notes](../../../aspose.words.notes/)
* Montage [Aspose.Words](../../../)
