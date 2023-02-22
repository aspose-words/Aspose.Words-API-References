---
title: Paragraph.IsFormatRevision
second_title: Aspose.Words für .NET-API-Referenz
description: Paragraph eigendom. Gibt true zurück wenn die Formatierung des Objekts in Microsoft Word geändert wurde während die Änderungsverfolgung aktiviert war.
type: docs
weight: 90
url: /de/net/aspose.words/paragraph/isformatrevision/
---
## Paragraph.IsFormatRevision property

Gibt „true“ zurück, wenn die Formatierung des Objekts in Microsoft Word geändert wurde, während die Änderungsverfolgung aktiviert war.

```csharp
public bool IsFormatRevision { get; }
```

### Beispiele

Zeigt, wie überprüft wird, ob es sich bei einem Absatz um eine Formatüberarbeitung handelt.

```csharp
Document doc = new Document(MyDir + "Format revision.docx");

// Dieser Absatz ist eine "Format"-Überarbeitung, die auftritt, wenn wir die Formatierung von vorhandenem Text ändern
// beim Verfolgen von Revisionen in Microsoft Word über "Review" -> "Änderungen verfolgen".
Assert.True(doc.FirstSection.Body.FirstParagraph.IsFormatRevision);
```

### Siehe auch

* class [Paragraph](../)
* namensraum [Aspose.Words](../../paragraph/)
* Montage [Aspose.Words](../../../)


