---
title: CustomXmlPart.DataChecksum
linktitle: DataChecksum
articleTitle: DataChecksum
second_title: Aspose.Words pour .NET
description: CustomXmlPart DataChecksum propriété. Spécifie une somme de contrôle de contrôle de redondance cyclique CRC duData contenu en C#.
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

Montre comment la somme de contrôle est calculée dans un runtime.

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

// Nous avons modifié le XmlPart de la balise et la somme de contrôle a été mise à jour au moment de l'exécution.
Assert.AreNotEqual(checksum, updatedChecksum);
```

### Voir également

* class [CustomXmlPart](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
