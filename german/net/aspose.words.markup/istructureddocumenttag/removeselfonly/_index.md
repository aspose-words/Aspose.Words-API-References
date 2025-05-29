---
title: IStructuredDocumentTag.RemoveSelfOnly
linktitle: RemoveSelfOnly
articleTitle: RemoveSelfOnly
second_title: Aspose.Words für .NET
description: Entdecken Sie die Methode „IStructuredDocumentTag RemoveSelfOnly“, um mühelos einen SDT-Knoten zu entfernen und gleichzeitig seinen Inhalt in Ihrem Dokumentbaum beizubehalten.
type: docs
weight: 180
url: /de/net/aspose.words.markup/istructureddocumenttag/removeselfonly/
---
## IStructuredDocumentTag.RemoveSelfOnly method

Entfernt nur diesen SDT-Knoten selbst, behält aber seinen Inhalt im Dokumentbaum.

```csharp
public void RemoveSelfOnly()
```

## Beispiele

Zeigt, wie strukturierte Dokument-Tags entfernt werden, der Inhalt jedoch erhalten bleibt.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

    // Diese Sammlung bietet eine einheitliche Schnittstelle für den Zugriff auf strukturierte Tags mit und ohne Bereich.
IEnumerable<IStructuredDocumentTag> sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(5, sdts.Count());

// Hier können wir untergeordnete Knoten aus der gemeinsamen Schnittstelle strukturierter Tags mit und ohne Bereich abrufen.
foreach (IStructuredDocumentTag sdt in sdts)
    if (sdt.GetChildNodes(NodeType.Any, false).Count > 0)
        sdt.RemoveSelfOnly();

sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(0, sdts.Count());
```

### Siehe auch

* interface [IStructuredDocumentTag](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
