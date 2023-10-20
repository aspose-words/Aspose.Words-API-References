---
title: XmlMapping.Delete
linktitle: Delete
articleTitle: Delete
second_title: Aspose.Words pour .NET
description: XmlMapping Delete méthode. Supprime le mappage du document structuré parent avec les données XML en C#.
type: docs
weight: 60
url: /fr/net/aspose.words.markup/xmlmapping/delete/
---
## XmlMapping.Delete method

Supprime le mappage du document structuré parent avec les données XML.

```csharp
public void Delete()
```

## Exemples

Montre comment définir des mappages XML pour les parties XML personnalisées.

```csharp
Document doc = new Document();

// Construisez une partie XML contenant du texte et ajoutez-la à la collection CustomXmlPart du document.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Text element #1</text><text>Text element #2</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual("<root><text>Text element #1</text><text>Text element #2</text></root>", 
    Encoding.UTF8.GetString(xmlPart.Data));

// Créez une balise de document structuré qui affichera le contenu de notre CustomXmlPart.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);

// Définissez un mappage pour notre balise de document structuré. Cette cartographie indiquera
// notre balise de document structuré pour afficher une partie du contenu textuel de la partie XML vers laquelle pointe XPath.
// Dans ce cas, ce sera le contenu du deuxième "<text>" élément du premier "<root>" élément : "Élément de texte #2".
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
