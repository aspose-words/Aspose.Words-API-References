---
title: Paragraph.IsFormatRevision
linktitle: IsFormatRevision
articleTitle: IsFormatRevision
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „IsFormatRevision“ in Microsoft Word Formatierungsänderungen verfolgt und so genaue Dokumentbearbeitungen und eine verbesserte Zusammenarbeit gewährleistet.
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

Zeigt, wie Sie überprüfen, ob es sich bei einem Absatz um eine Formatrevision handelt.

```csharp
Document doc = new Document(MyDir + "Format revision.docx");

// Dieser Absatz ist eine "Format"-Revision, die auftritt, wenn wir die Formatierung des vorhandenen Textes ändern
// während Sie Revisionen in Microsoft Word über „Überprüfen“ -> „Änderungen nachverfolgen“ verfolgen.
Assert.True(doc.FirstSection.Body.FirstParagraph.IsFormatRevision);
```

### Siehe auch

* class [Paragraph](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
