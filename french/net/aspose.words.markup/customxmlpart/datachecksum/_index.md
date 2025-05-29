---
title: CustomXmlPart.DataChecksum
linktitle: DataChecksum
articleTitle: DataChecksum
second_title: Aspose.Words pour .NET
description: Découvrez la propriété CustomXmlPart DataChecksum, qui garantit l'intégrité des données grâce à une somme de contrôle CRC fiable pour votre contenu XML. Améliorez la fiabilité de vos données !
type: docs
weight: 30
url: /fr/net/aspose.words.markup/customxmlpart/datachecksum/
---
## CustomXmlPart.DataChecksum property

Spécifie une somme de contrôle de contrôle de redondance cyclique (CRC) du[`Data`](../data/) contenu.

```csharp
public long DataChecksum { get; }
```

## Exemples

Montre comment la somme de contrôle est calculée lors d'une exécution.

```csharp
Document doc = new Document();

StructuredDocumentTag richText = new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(richText);

// La somme de contrôle est en lecture seule et calculée à l'aide des données de la partie de données XML personnalisée correspondante.
richText.XmlMapping.SetMapping(doc.CustomXmlParts.Add(Guid.NewGuid().ToString(),
    "<root><text>ContentControl</text></root>"), "/root/text", "");

long checksum = richText.XmlMapping.CustomXmlPart.DataChecksum;
Console.WriteLine(checksum);

richText.XmlMapping.SetMapping(doc.CustomXmlParts.Add(Guid.NewGuid().ToString(),
    "<root><text>Updated ContentControl</text></root>"), "/root/text", "");

long updatedChecksum = richText.XmlMapping.CustomXmlPart.DataChecksum;
Console.WriteLine(updatedChecksum);

// Nous avons modifié la partie Xml de la balise et la somme de contrôle a été mise à jour lors de l'exécution.
Assert.AreNotEqual(checksum, updatedChecksum);
```

### Voir également

* class [CustomXmlPart](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
