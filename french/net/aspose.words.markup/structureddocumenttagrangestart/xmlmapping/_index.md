---
title: StructuredDocumentTagRangeStart.XmlMapping
linktitle: XmlMapping
articleTitle: XmlMapping
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété StructuredDocumentTagRangeStart XmlMapping connecte la plage de balises de votre document aux données XML personnalisées, améliorant ainsi l'intégration du document.
type: docs
weight: 190
url: /fr/net/aspose.words.markup/structureddocumenttagrangestart/xmlmapping/
---
## StructuredDocumentTagRangeStart.XmlMapping property

Obtient un objet qui représente le mappage de cette plage de balises de document structuré aux données XML dans une partie XML personnalisée du document actuel.

```csharp
public XmlMapping XmlMapping { get; }
```

## Remarques

Vous pouvez utiliser le[`SetMapping`](../../xmlmapping/setmapping/) méthode de cet objet pour mapper une plage de balises de document structuré à des données XML.

## Exemples

Montre comment définir des mappages XML pour le début de la plage d'une balise de document structuré.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");

// Construisez une partie XML contenant du texte et ajoutez-la à la collection CustomXmlPart du document.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Text element #1</text><text>Text element #2</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual("<root><text>Text element #1</text><text>Text element #2</text></root>",
    Encoding.UTF8.GetString(xmlPart.Data));

// Créez une balise de document structurée qui affichera le contenu de notre CustomXmlPart dans le document.
StructuredDocumentTagRangeStart sdtRangeStart = (StructuredDocumentTagRangeStart)doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true);

// Si nous définissons un mappage pour notre balise de document structuré,
// il n'affichera qu'une partie du CustomXmlPart vers lequel pointe le XPath.
// Ce XPath pointera vers le contenu du deuxième élément "<text>" du premier élément "<root>" de notre CustomXmlPart.
sdtRangeStart.XmlMapping.SetMapping(xmlPart, "/root[1]/text[2]", null);

doc.Save(ArtifactsDir + "StructuredDocumentTag.StructuredDocumentTagRangeStartXmlMapping.docx");
```

### Voir également

* class [XmlMapping](../../xmlmapping/)
* class [StructuredDocumentTagRangeStart](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
