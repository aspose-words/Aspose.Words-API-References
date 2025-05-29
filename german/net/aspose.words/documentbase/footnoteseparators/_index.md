---
title: DocumentBase.FootnoteSeparators
linktitle: FootnoteSeparators
articleTitle: FootnoteSeparators
second_title: Aspose.Words für .NET
description: Greifen Sie mit der FootnoteSeparators-Eigenschaft von DocumentBase auf Fußnoten- und Endnotentrennzeichen in Ihrem Dokument zu und passen Sie diese an, um eine verbesserte Formatierungskontrolle zu erhalten.
type: docs
weight: 40
url: /de/net/aspose.words/documentbase/footnoteseparators/
---
## DocumentBase.FootnoteSeparators property

Bietet Zugriff auf die im Dokument definierten Fußnoten-/Endnotentrennzeichen.

```csharp
public FootnoteSeparatorCollection FootnoteSeparators { get; }
```

## Beispiele

Zeigt, wie Endnotentrennzeichen entfernt werden.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator endnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.EndnoteSeparator];
// Endnotentrennzeichen entfernen.
endnoteSeparator.FirstParagraph.FirstChild.Remove();
```

Zeigt, wie das Fußnotentrennzeichenformat verwaltet wird.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator footnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.FootnoteSeparator];
// Fußnotentrennzeichen ausrichten.
footnoteSeparator.FirstParagraph.ParagraphFormat.Alignment = ParagraphAlignment.Center;
```

### Siehe auch

* class [FootnoteSeparatorCollection](../../../aspose.words.notes/footnoteseparatorcollection/)
* class [DocumentBase](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
