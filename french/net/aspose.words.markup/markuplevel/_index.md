---
title: MarkupLevel Enum
linktitle: MarkupLevel
articleTitle: MarkupLevel
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Markup.MarkupLevel, définissant où StructuredDocumentTags s'intègre dans l'arborescence de votre document pour une organisation et un contrôle améliorés.
type: docs
weight: 4670
url: /fr/net/aspose.words.markup/markuplevel/
---
## MarkupLevel enumeration

Spécifie le niveau dans l'arborescence du document où un[`StructuredDocumentTag`](../structureddocumenttag/) peut se produire.

```csharp
public enum MarkupLevel
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Unknown | `0` | Spécifie la valeur inconnue ou non valide. |
| Inline | `1` | L'élément apparaît au niveau de la ligne (par exemple parmi des séquences de texte). |
| Block | `2` | L'élément apparaît au niveau du bloc (par exemple parmi les tableaux et les paragraphes). |
| Row | `3` | L'élément apparaît parmi les lignes d'un tableau. |
| Cell | `4` | L'élément apparaît parmi les cellules d'une ligne. |

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

* espace de noms [Aspose.Words.Markup](../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../)
