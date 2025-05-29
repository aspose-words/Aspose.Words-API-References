---
title: XmlMapping Class
linktitle: XmlMapping
articleTitle: XmlMapping
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Markup.XmlMapping pour lier de manière transparente les balises de documents structurés aux éléments XML, améliorant ainsi l'intégration des données de votre document.
type: docs
weight: 4790
url: /fr/net/aspose.words.markup/xmlmapping/
---
## XmlMapping class

Spécifie les informations utilisées pour établir un mappage entre la balise de document structurée parent et un élément XML stocké dans une partie de données XML personnalisée du document.

Pour en savoir plus, visitez le[Balises de documents structurés ou contrôle de contenu](https://docs.aspose.com/words/net/working-with-content-control-sdt/) article de documentation.

```csharp
public class XmlMapping
```

## Propriétés

| Nom | La description |
| --- | --- |
| [CustomXmlPart](../../aspose.words.markup/xmlmapping/customxmlpart/) { get; } | Renvoie la partie de données XML personnalisée à laquelle la balise de document structuré parent est mappée. |
| [IsMapped](../../aspose.words.markup/xmlmapping/ismapped/) { get; } | Retours`vrai` si la balise du document structuré parent est correctement mappée aux données XML. |
| [PrefixMappings](../../aspose.words.markup/xmlmapping/prefixmappings/) { get; } | Renvoie les mappages de préfixes d'espace de noms XML pour évaluer le[`XPath`](./xpath/) . |
| [StoreItemId](../../aspose.words.markup/xmlmapping/storeitemid/) { get; } | Spécifie l'identifiant de données XML personnalisé pour la partie de données XML personnalisée qui doit être utilisé pour évaluer le[`XPath`](./xpath/) expression. |
| [XPath](../../aspose.words.markup/xmlmapping/xpath/) { get; } | Renvoie l'expression XPath, qui est évaluée pour trouver le nœud XML personnalisé qui est mappé à la balise de document structuré parent. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Delete](../../aspose.words.markup/xmlmapping/delete/)() | Supprime le mappage du document structuré parent aux données XML. |
| [SetMapping](../../aspose.words.markup/xmlmapping/setmapping/)(*[CustomXmlPart](../customxmlpart/), string, string*) | Définit un mappage entre la balise de document structuré parent et un nœud XML d'une partie de données XML personnalisée. |

## Exemples

Montre comment définir des mappages XML pour des parties XML personnalisées.

```csharp
Document doc = new Document();

// Construisez une partie XML contenant du texte et ajoutez-la à la collection CustomXmlPart du document.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Text element #1</text><text>Text element #2</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual("<root><text>Text element #1</text><text>Text element #2</text></root>",
    Encoding.UTF8.GetString(xmlPart.Data));

// Créez une balise de document structurée qui affichera le contenu de notre CustomXmlPart.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);

// Définissez un mappage pour notre balise de document structuré. Ce mappage indiquera
// notre balise de document structurée pour afficher une partie du contenu textuel de la partie XML vers laquelle pointe XPath.
// Dans ce cas, il s'agira du contenu du deuxième élément "<texte>" du premier élément "<racine>" : "Élément texte #2".
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[2]", "xmlns:ns='http://www.w3.org/2001/XMLSchema'");

Assert.True(tag.XmlMapping.IsMapped);
Assert.AreEqual(xmlPart, tag.XmlMapping.CustomXmlPart);
Assert.AreEqual("/root[1]/text[2]", tag.XmlMapping.XPath);
Assert.AreEqual("xmlns:ns='http://www.w3.org/2001/XMLSchema'", tag.XmlMapping.PrefixMappings);

// Ajoutez la balise de document structuré au document pour afficher le contenu de notre partie personnalisée.
doc.FirstSection.Body.AppendChild(tag);
doc.Save(ArtifactsDir + "StructuredDocumentTag.XmlMapping.docx");
```

### Voir également

* espace de noms [Aspose.Words.Markup](../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../)
