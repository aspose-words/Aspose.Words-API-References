---
title: FootnoteOptions.Columns
linktitle: Columns
articleTitle: Columns
second_title: Aspose.Words für .NET
description: FootnoteOptions Columns eigendom. Gibt die Anzahl der Spalten an mit denen der Fußnotenbereich formatiert wird in C#.
type: docs
weight: 10
url: /de/net/aspose.words.notes/footnoteoptions/columns/
---
## FootnoteOptions.Columns property

Gibt die Anzahl der Spalten an, mit denen der Fußnotenbereich formatiert wird.

```csharp
public int Columns { get; set; }
```

## Bemerkungen

Wenn diese Eigenschaft den Wert 0 hat, wird der Fußnotenbereich mit einer Anzahl von Spalten formatiert, die auf der Anzahl der Spalten auf der angezeigten Seite basiert. Der Standardwert ist 0.

## Beispiele

Zeigt, wie der Fußnotenabschnitt in eine bestimmte Anzahl von Spalten aufgeteilt wird.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");
doc.FootnoteOptions.Columns = 2;
doc.Save(ArtifactsDir + "Document.FootnoteColumns.docx");
```

### Siehe auch

* class [FootnoteOptions](../)
* namensraum [Aspose.Words.Notes](../../../aspose.words.notes/)
* Montage [Aspose.Words](../../../)
