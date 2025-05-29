---
title: PageInfo.Colored
linktitle: Colored
articleTitle: Colored
second_title: Aspose.Words für .NET
description: Finden Sie mit der PageInfo-Eigenschaft „Colored“ heraus, ob Ihre Seite Inhalte in leuchtenden Farben bietet. Steigern Sie die Nutzerinteraktion und verbessern Sie die visuelle Attraktivität!
type: docs
weight: 10
url: /de/net/aspose.words.rendering/pageinfo/colored/
---
## PageInfo.Colored property

Rückgaben`WAHR` wenn die Seite farbigen Inhalt enthält.

```csharp
public bool Colored { get; }
```

## Beispiele

Zeigt, wie Sie überprüfen können, ob die Seite farbig ist oder nicht.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Überprüfen Sie, dass die erste Seite des Dokuments nicht farbig ist.
Assert.IsFalse(doc.GetPageInfo(0).Colored);
```

### Siehe auch

* class [PageInfo](../)
* namensraum [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* Montage [Aspose.Words](../../../)
