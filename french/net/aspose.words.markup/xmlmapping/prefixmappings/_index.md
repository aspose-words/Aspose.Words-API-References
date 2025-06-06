---
title: XmlMapping.PrefixMappings
linktitle: PrefixMappings
articleTitle: PrefixMappings
second_title: Aspose.Words pour .NET
description: Découvrez la propriété XmlMapping PrefixMappings pour un mappage fluide des préfixes d'espaces de noms XML et une évaluation XPath efficace. Améliorez votre traitement XML dès aujourd'hui !
type: docs
weight: 30
url: /fr/net/aspose.words.markup/xmlmapping/prefixmappings/
---
## XmlMapping.PrefixMappings property

Renvoie les mappages de préfixes d'espace de noms XML pour évaluer le[`XPath`](../xpath/) .

```csharp
public string PrefixMappings { get; }
```

## Remarques

Spécifie l'ensemble des mappages de préfixes, qui doivent être utilisés pour interpréter l'expression XPath lorsque l'expression XPath est évaluée par rapport aux parties de données XML personnalisées dans le document.

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

* class [XmlMapping](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
