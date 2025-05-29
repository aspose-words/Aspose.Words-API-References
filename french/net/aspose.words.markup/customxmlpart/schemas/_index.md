---
title: CustomXmlPart.Schemas
linktitle: Schemas
articleTitle: Schemas
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Schémas CustomXmlPart pour gérer facilement les schémas XML liés à vos parties XML personnalisées, améliorant ainsi l'organisation et l'efficacité des données.
type: docs
weight: 50
url: /fr/net/aspose.words.markup/customxmlpart/schemas/
---
## CustomXmlPart.Schemas property

Spécifie l'ensemble des schémas XML associés à cette partie XML personnalisée.

```csharp
public CustomXmlSchemaCollection Schemas { get; }
```

## Exemples

Montre comment créer une balise de document structurée avec des données XML personnalisées.

```csharp
Document doc = new Document();

// Construisez une partie XML contenant des données et ajoutez-la à la collection du document.
// Si nous activons l'onglet « Développeur » dans Microsoft Word,
// nous pouvons trouver des éléments de cette collection dans le « volet de mappage XML », ainsi que quelques éléments par défaut.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello world!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual(Encoding.ASCII.GetBytes(xmlPartContent), xmlPart.Data);
Assert.AreEqual(xmlPartId, xmlPart.Id);

// Vous trouverez ci-dessous deux manières de faire référence aux parties XML.
// 1 - Par un index dans la collection de parties XML personnalisées :
Assert.AreEqual(xmlPart, doc.CustomXmlParts[0]);

// 2 - Par GUID :
Assert.AreEqual(xmlPart, doc.CustomXmlParts.GetById(xmlPartId));

// Ajouter une association de schéma XML.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Clonez une partie, puis insérez-la dans la collection.
CustomXmlPart xmlPartClone = xmlPart.Clone();
xmlPartClone.Id = Guid.NewGuid().ToString("B");
doc.CustomXmlParts.Add(xmlPartClone);

Assert.AreEqual(2, doc.CustomXmlParts.Count);

// Parcourez la collection et imprimez le contenu de chaque partie.
using (IEnumerator<CustomXmlPart> enumerator = doc.CustomXmlParts.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"XML part index {index}, ID: {enumerator.Current.Id}");
        Console.WriteLine($"\tContent: {Encoding.UTF8.GetString(enumerator.Current.Data)}");
        index++;
    }
}

// Utilisez la méthode « RemoveAt » pour supprimer la partie clonée par index.
doc.CustomXmlParts.RemoveAt(1);

Assert.AreEqual(1, doc.CustomXmlParts.Count);

// Clonez la collection de pièces XML, puis utilisez la méthode « Clear » pour supprimer tous ses éléments à la fois.
CustomXmlPartCollection customXmlParts = doc.CustomXmlParts.Clone();
customXmlParts.Clear();

// Créez une balise de document structurée qui affichera le contenu de notre partie et l'insérera dans le corps du document.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[1]", string.Empty);

doc.FirstSection.Body.AppendChild(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CustomXml.docx");
```

### Voir également

* class [CustomXmlSchemaCollection](../../customxmlschemacollection/)
* class [CustomXmlPart](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
