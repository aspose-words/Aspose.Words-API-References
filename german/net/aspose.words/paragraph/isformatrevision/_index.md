---
title: Paragraph.IsFormatRevision
linktitle: IsFormatRevision
articleTitle: IsFormatRevision
second_title: Aspose.Words für .NET
description: Paragraph IsFormatRevision eigendom. Gibt true zurück wenn die Formatierung des Objekts in Microsoft Word geändert wurde während die Änderungsverfolgung aktiviert war in C#.
type: docs
weight: 90
url: /de/net/aspose.words/paragraph/isformatrevision/
---
## Paragraph.IsFormatRevision property

Gibt „true“ zurück, wenn die Formatierung des Objekts in Microsoft Word geändert wurde, während die Änderungsverfolgung aktiviert war.

```csharp
public bool IsFormatRevision { get; }
```

## Beispiele

Zeigt, wie man prüft, ob es sich bei einem Absatz um eine Formatrevision handelt.

```csharp
Document doc = new Document(MyDir + "Format revision.docx");

// Dieser Absatz ist eine „Format“-Revision, die auftritt, wenn wir die Formatierung von vorhandenem Text ändern
// während Überarbeitungen in Microsoft Word über „Überprüfen“ verfolgt werden -> "Änderungen verfolgen".
Assert.True(doc.FirstSection.Body.FirstParagraph.IsFormatRevision);
```

### Siehe auch

* class [Paragraph](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
