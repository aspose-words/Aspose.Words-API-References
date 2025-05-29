---
title: StructuredDocumentTagRangeStart.WordOpenXMLMinimal
linktitle: WordOpenXMLMinimal
articleTitle: WordOpenXMLMinimal
second_title: Aspose.Words pour .NET
description: Découvrez la propriété StructuredDocumentTagRangeStart dans WordOpenXMLMinimal. Accédez à une chaîne XML simplifiée au format FlatOpc, en vous concentrant uniquement sur le contenu.
type: docs
weight: 180
url: /fr/net/aspose.words.markup/structureddocumenttagrangestart/wordopenxmlminimal/
---
## StructuredDocumentTagRangeStart.WordOpenXMLMinimal property

Obtient une chaîne qui représente le XML contenu dans le nœud dans leFlatOpc format. Contrairement au[`WordOpenXML`](../wordopenxml/) propriété, cette méthode génère un document simplifié qui exclut toutes les parties non liées au contenu.

```csharp
public string WordOpenXMLMinimal { get; }
```

## Exemples

Montre comment obtenir le XML minimal contenu dans le nœud au format FlatOpc.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");
StructuredDocumentTagRangeStart tag =
    doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true) as StructuredDocumentTagRangeStart;

Assert.True(tag.WordOpenXMLMinimal
    .Contains(
        "<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
Assert.False(tag.WordOpenXMLMinimal.Contains("xmlns:w16cid=\"http://schemas.microsoft.com/office/word/2016/wordml/cid\""));
```

### Voir également

* class [StructuredDocumentTagRangeStart](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
