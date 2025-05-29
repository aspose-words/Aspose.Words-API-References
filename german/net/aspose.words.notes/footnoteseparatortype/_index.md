---
title: FootnoteSeparatorType Enum
linktitle: FootnoteSeparatorType
articleTitle: FootnoteSeparatorType
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.FootnoteSeparatorType, um Fußnoten- und Endnotentrennzeichen anzupassen und so die Dokumentformatierung und Lesbarkeit zu verbessern.
type: docs
weight: 5010
url: /de/net/aspose.words.notes/footnoteseparatortype/
---
## FootnoteSeparatorType enumeration

Gibt den Typ des Fußnoten-/Endnotentrennzeichens an.

```csharp
public enum FootnoteSeparatorType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| FootnoteSeparator | `0` | Trennzeichen zwischen Haupttext und Fußnotentext. |
| FootnoteContinuationSeparator | `1` | Wird über dem Fußnotentext auf einer Seite gedruckt, wenn der Text von einer vorherigen Seite fortgesetzt werden muss. |
| FootnoteContinuationNotice | `2` | Wird unter dem Fußnotentext auf einer Seite gedruckt, wenn der Fußnotentext auf einer nachfolgenden Seite fortgesetzt werden muss. |
| EndnoteSeparator | `3` | Trennzeichen zwischen Haupttext und Endnotentext. |
| EndnoteContinuationSeparator | `4` | Wird über dem Endnotentext auf einer Seite gedruckt, wenn der Text von einer vorherigen Seite fortgesetzt werden muss. |
| EndnoteContinuationNotice | `5` | Wird unter dem Endnotentext auf einer Seite gedruckt, wenn der Endnotentext auf einer nachfolgenden Seite fortgesetzt werden muss. |

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

* namensraum [Aspose.Words.Notes](../../aspose.words.notes/)
* Montage [Aspose.Words](../../)
