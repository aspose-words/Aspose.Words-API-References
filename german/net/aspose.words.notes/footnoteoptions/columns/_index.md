---
title: FootnoteOptions.Columns
linktitle: Columns
articleTitle: Columns
second_title: Aspose.Words für .NET
description: Entdecken Sie die FootnoteOptions-Spalteneigenschaft, um Ihre Fußnoten einfach mit anpassbaren Spaltenlayouts für verbesserte Lesbarkeit und Präsentation zu formatieren.
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

Wenn diese Eigenschaft den Wert 0 hat, wird der Fußnotenbereich mit einer Spaltenanzahl formatiert, die der Spaltenanzahl auf der angezeigten Seite entspricht. Der Standardwert ist 0.

## Beispiele

Zeigt, wie der Fußnotenabschnitt in eine bestimmte Anzahl Spalten aufgeteilt wird.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");
doc.FootnoteOptions.Columns = 2;
doc.Save(ArtifactsDir + "Document.FootnoteColumns.docx");
```

### Siehe auch

* class [FootnoteOptions](../)
* namensraum [Aspose.Words.Notes](../../../aspose.words.notes/)
* Montage [Aspose.Words](../../../)
