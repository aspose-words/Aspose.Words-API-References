---
title: IStructuredDocumentTag.WordOpenXML
linktitle: WordOpenXML
articleTitle: WordOpenXML
second_title: Aspose.Words pour .NET
description: Découvrez la propriété WordOpenXML IStructuredDocumentTag, accédez aux chaînes XML au format FlatOpc pour une gestion et une intégration améliorées des documents.
type: docs
weight: 150
url: /fr/net/aspose.words.markup/istructureddocumenttag/wordopenxml/
---
## IStructuredDocumentTag.WordOpenXML property

Obtient une chaîne qui représente le XML contenu dans le nœud dans leFlatOpc format.

```csharp
public string WordOpenXML { get; }
```

## Exemples

Montre comment obtenir du XML contenu dans le nœud au format FlatOpc.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

List<StructuredDocumentTag> tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true)
    .OfType<StructuredDocumentTag>().ToList();

Assert.True(tags[0].WordOpenXML
    .Contains(
        "<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
```

### Voir également

* interface [IStructuredDocumentTag](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
