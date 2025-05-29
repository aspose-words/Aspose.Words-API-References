---
title: Document.GetPageInfo
linktitle: GetPageInfo
articleTitle: GetPageInfo
second_title: Aspose.Words für .NET
description: Entdecken Sie die GetPageInfo-Methode zum Abrufen wichtiger Seitengrößen, Ausrichtungen und Rendering-Details für optimiertes Drucken und verbessertes Dokumentenmanagement.
type: docs
weight: 650
url: /de/net/aspose.words/document/getpageinfo/
---
## Document.GetPageInfo method

Ruft die Seitengröße, Ausrichtung und andere Informationen zu einer Seite ab, die zum Drucken oder Rendern nützlich sein können.

```csharp
public PageInfo GetPageInfo(int pageIndex)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pageIndex | Int32 | Der 0-basierte Seitenindex. |

## Beispiele

Zeigt, wie Sie überprüfen können, ob die Seite farbig ist oder nicht.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Überprüfen Sie, dass die erste Seite des Dokuments nicht farbig ist.
Assert.IsFalse(doc.GetPageInfo(0).Colored);
```

### Siehe auch

* class [PageInfo](../../../aspose.words.rendering/pageinfo/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
