---
title: Class CustomXmlPart
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Markup.CustomXmlPart classe. Représente une partie de stockage de données XML personnalisée données XML personnalisées dans un package.
type: docs
weight: 3680
url: /fr/net/aspose.words.markup/customxmlpart/
---
## CustomXmlPart class

Représente une partie de stockage de données XML personnalisée (données XML personnalisées dans un package).

```csharp
public class CustomXmlPart
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [CustomXmlPart](customxmlpart/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [Data](../../aspose.words.markup/customxmlpart/data/) { get; set; } | Obtient ou définit le contenu XML de cette partie de stockage de données XML personnalisée. |
| [DataChecksum](../../aspose.words.markup/customxmlpart/datachecksum/) { get; } | Spécifie une somme de contrôle de contrôle de redondance cyclique (CRC) du[`Data`](./data/) contenu. |
| [Id](../../aspose.words.markup/customxmlpart/id/) { get; set; } | Obtient ou définit la chaîne qui identifie cette partie XML personnalisée dans un document OOXML. |
| [Schemas](../../aspose.words.markup/customxmlpart/schemas/) { get; } | Spécifie l'ensemble de schémas XML associés à cette partie XML personnalisée. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Clone](../../aspose.words.markup/customxmlpart/clone/)() | Fait une copie "assez profonde" de l'objet. Ne duplique pas les octets du[`Data`](./data/) valeur. |

### Remarques

Un document DOCX ou DOC peut contenir une ou plusieurs parties de stockage de données XML personnalisées. Aspose.Words préserve et permet de créer et d'extraire des données XML personnalisées via le[`CustomXmlParts`](../../aspose.words/document/customxmlparts/) le recueil.

### Exemples

Montre comment créer une balise de document structurée avec des données XML personnalisées.

```csharp
Document doc = new Document();

// Construire une partie XML qui contient des données et l'ajouter à la collection du document.
// Si nous activons l'onglet "Développeur" dans Microsoft Word,
// nous pouvons trouver des éléments de cette collection dans le "XML Mapping Pane", ainsi que quelques éléments par défaut.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello world!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual(Encoding.ASCII.GetBytes(xmlPartContent), xmlPart.Data);
Assert.AreEqual(xmlPartId, xmlPart.Id);

// Vous trouverez ci-dessous deux façons de faire référence à des parties XML.
// 1 - Par un index dans la collection de parties XML personnalisée :
Assert.AreEqual(xmlPart, doc.CustomXmlParts[0]);

// 2 - Par GUID :
Assert.AreEqual(xmlPart, doc.CustomXmlParts.GetById(xmlPartId));

// Ajouter une association de schéma XML.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Clone une partie, puis l'insère dans la collection.
CustomXmlPart xmlPartClone = xmlPart.Clone();
xmlPartClone.Id = Guid.NewGuid().ToString("B");
doc.CustomXmlParts.Add(xmlPartClone);

Assert.AreEqual(2, doc.CustomXmlParts.Count);

// Itérer dans la collection et imprimer le contenu de chaque partie.
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

// Clone la collection de parties XML, puis utilise la méthode "Clear" pour supprimer tous ses éléments d'un coup.
CustomXmlPartCollection customXmlParts = doc.CustomXmlParts.Clone();
customXmlParts.Clear();

// Crée une balise de document structurée qui affichera le contenu de notre partie et l'insérera dans le corps du document.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[1]", string.Empty);

doc.FirstSection.Body.AppendChild(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CustomXml.docx");
```

### Voir également

* espace de noms [Aspose.Words.Markup](../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../)


