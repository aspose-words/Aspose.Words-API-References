---
title: PageInfo.Colored
linktitle: Colored
articleTitle: Colored
second_title: Aspose.Words für .NET
description: PageInfo Colored eigendom. Gibt zurückWAHR wenn die Seite farbige Inhalte enthält in C#.
type: docs
weight: 10
url: /de/net/aspose.words.rendering/pageinfo/colored/
---
## PageInfo.Colored property

Gibt zurück`WAHR` wenn die Seite farbige Inhalte enthält.

```csharp
public bool Colored { get; }
```

## Beispiele

Zeigt, wie Sie überprüfen können, ob die Seite farbig ist oder nicht.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Überprüfen Sie, ob die erste Seite des Dokuments nicht gefärbt ist.
Assert.IsFalse(doc.GetPageInfo(0).Colored);
```

### Siehe auch

* class [PageInfo](../)
* namensraum [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* Montage [Aspose.Words](../../../)
