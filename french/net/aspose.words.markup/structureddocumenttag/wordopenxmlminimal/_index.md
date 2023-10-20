---
title: StructuredDocumentTag.WordOpenXMLMinimal
linktitle: WordOpenXMLMinimal
articleTitle: WordOpenXMLMinimal
second_title: Aspose.Words pour .NET
description: StructuredDocumentTag WordOpenXMLMinimal propriété. Obtient une chaîne qui représente le XML contenu dans le nœud dans leFlatOpc format. Contrairement auWordOpenXMLpropriété cette méthode génère un document simplifié qui exclut toutes les parties non liées au contenu en C#.
type: docs
weight: 310
url: /fr/net/aspose.words.markup/structureddocumenttag/wordopenxmlminimal/
---
## StructuredDocumentTag.WordOpenXMLMinimal property

Obtient une chaîne qui représente le XML contenu dans le nœud dans leFlatOpc format. Contrairement au[`WordOpenXML`](../wordopenxml/)propriété, cette méthode génère un document simplifié qui exclut toutes les parties non liées au contenu.

```csharp
public string WordOpenXMLMinimal { get; }
```

## Exemples

Montre comment utiliser les styles pour les éléments de contrôle de contenu.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vous trouverez ci-dessous deux manières d'appliquer un style du document à une balise de document structuré.
// 1 - Appliquer un objet style de la collection de styles du document :
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Référencer un style dans le document par son nom :
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Console.WriteLine(sdt.WordOpenXMLMinimal);

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

### Voir également

* class [StructuredDocumentTag](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
