---
title: StructuredDocumentTag.Style
linktitle: Style
articleTitle: Style
second_title: Aspose.Words pour .NET
description: Découvrez comment gérer la propriété Style de StructuredDocumentTags pour améliorer la mise en forme de votre document et améliorer la lisibilité sans effort.
type: docs
weight: 260
url: /fr/net/aspose.words.markup/structureddocumenttag/style/
---
## StructuredDocumentTag.Style property

Obtient ou définit le style de la balise de document structuré.

```csharp
public Style Style { get; set; }
```

## Remarques

SeulementCharacter style ouParagraph le style avec le style de caractère lié peut être défini.

## Exemples

Montre comment travailler avec des styles pour les éléments de contrôle de contenu.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vous trouverez ci-dessous deux manières d'appliquer un style du document à une balise de document structurée.
// 1 - Appliquer un objet de style de la collection de styles du document :
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

* class [Style](../../../aspose.words/style/)
* class [StructuredDocumentTag](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
