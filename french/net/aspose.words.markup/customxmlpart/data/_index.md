---
title: CustomXmlPart.Data
second_title: Référence de l'API Aspose.Words pour .NET
description: CustomXmlPart propriété. Obtient ou définit le contenu XML de cette partie de stockage de données XML personnalisée.
type: docs
weight: 20
url: /fr/net/aspose.words.markup/customxmlpart/data/
---
## CustomXmlPart.Data property

Obtient ou définit le contenu XML de cette partie de stockage de données XML personnalisée.

```csharp
public byte[] Data { get; set; }
```

### Remarques

La valeur par défaut est un tableau d'octets vide. La valeur ne peut pas être`nul`.

### Exemples

Montre comment créer une balise de document structuré avec des données XML personnalisées.

```csharp
Document doc = new Document();

// Construisez une partie XML contenant des données et ajoutez-la à la collection du document.
// Si nous activons l'onglet "Développeur" dans Microsoft Word,
// nous pouvons trouver des éléments de cette collection dans le "XML Mapping Pane", ainsi que quelques éléments par défaut.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello world!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual(Encoding.ASCII.GetBytes(xmlPartContent), xmlPart.Data);
Assert.AreEqual(xmlPartId, xmlPart.Id);

// Vous trouverez ci-dessous deux manières de faire référence aux parties XML.
// 1 - Par un index dans la collection de composants XML personnalisés :
Assert.AreEqual(xmlPart, doc.CustomXmlParts[0]);

// 2 - Par GUID :
Assert.AreEqual(xmlPart, doc.CustomXmlParts.GetById(xmlPartId));

// Ajout d'une association de schéma XML.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Clonez une pièce, puis insérez-la dans la collection.
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

// Utilisez la méthode "RemoveAt" pour supprimer la partie clonée par index.
doc.CustomXmlParts.RemoveAt(1);

Assert.AreEqual(1, doc.CustomXmlParts.Count);

// Clonez la collection de composants XML, puis utilisez la méthode "Clear" pour supprimer tous ses éléments en même temps.
CustomXmlPartCollection customXmlParts = doc.CustomXmlParts.Clone();
customXmlParts.Clear();

// Créez une balise de document structurée qui affichera le contenu de notre pièce et l'insérerez dans le corps du document.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[1]", string.Empty);

doc.FirstSection.Body.AppendChild(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CustomXml.docx");
```

### Voir également

* class [CustomXmlPart](../)
* espace de noms [Aspose.Words.Markup](../../customxmlpart/)
* Assemblée [Aspose.Words](../../../)


