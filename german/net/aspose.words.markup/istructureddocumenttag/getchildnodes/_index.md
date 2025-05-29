---
title: IStructuredDocumentTag.GetChildNodes
linktitle: GetChildNodes
articleTitle: GetChildNodes
second_title: Aspose.Words für .NET
description: Entdecken Sie die GetChildNodes-Methode von IStructuredDocumentTag und greifen Sie auf eine dynamische Sammlung untergeordneter Knoten zu, die auf Ihre angegebenen Typen zugeschnitten sind, um die Dokumentenverwaltung zu verbessern.
type: docs
weight: 170
url: /de/net/aspose.words.markup/istructureddocumenttag/getchildnodes/
---
## IStructuredDocumentTag.GetChildNodes method

Gibt eine Live-Sammlung von untergeordneten Knoten zurück, die den angegebenen Typen entsprechen.

```csharp
public NodeCollection GetChildNodes(NodeType nodeType, bool isDeep)
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

* class [NodeCollection](../../../aspose.words/nodecollection/)
* enum [NodeType](../../../aspose.words/nodetype/)
* interface [IStructuredDocumentTag](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
