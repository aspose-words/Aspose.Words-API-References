---
title: FootnoteSeparatorCollection Class
linktitle: FootnoteSeparatorCollection
articleTitle: FootnoteSeparatorCollection
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.Notes.FootnoteSeparatorCollection für einfachen Zugriff auf Fußnotentrennzeichen in Ihren Dokumenten. Verbessern Sie noch heute Ihre Dokumentformatierung!
type: docs
weight: 5000
url: /de/net/aspose.words.notes/footnoteseparatorcollection/
---
## FootnoteSeparatorCollection class

Bietet typisierten Zugriff auf[`FootnoteSeparator`](../footnoteseparator/) Knoten eines Dokuments.

```csharp
public class FootnoteSeparatorCollection : IEnumerable<FootnoteSeparator>
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FootnoteSeparatorCollection](footnoteseparatorcollection/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Item](../../aspose.words.notes/footnoteseparatorcollection/item/) { get; } | Ruft eine[`FootnoteSeparator`](../footnoteseparator/) des angegebenen Typs. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetEnumerator](../../aspose.words.notes/footnoteseparatorcollection/getenumerator/)() |  |

## Beispiele

Zeigt, wie das Fußnotentrennzeichenformat verwaltet wird.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator footnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.FootnoteSeparator];
// Fußnotentrennzeichen ausrichten.
footnoteSeparator.FirstParagraph.ParagraphFormat.Alignment = ParagraphAlignment.Center;
```

### Siehe auch

* class [FootnoteSeparator](../footnoteseparator/)
* namensraum [Aspose.Words.Notes](../../aspose.words.notes/)
* Montage [Aspose.Words](../../)
