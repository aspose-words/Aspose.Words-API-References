---
title: CustomXmlPart Class
linktitle: CustomXmlPart
articleTitle: CustomXmlPart
second_title: Aspose.Words pour .NET
description: Aspose.Words.Markup.CustomXmlPart classe. Représente une partie de stockage de données XML personnalisée données XML personnalisées dans un package en C#.
type: docs
weight: 3920
url: /fr/net/aspose.words.markup/customxmlpart/
---
## CustomXmlPart class

Représente une partie de stockage de données XML personnalisée (données XML personnalisées dans un package).

Pour en savoir plus, visitez le[Balises de documents structurés ou contrôle de contenu](https://docs.aspose.com/words/net/working-with-content-control-sdt/) article documentaire.

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
| [Clone](../../aspose.words.markup/customxmlpart/clone/)() | Crée une copie "suffisamment profonde" de l'objet. Ne duplique pas les octets du[`Data`](./data/) valeur. |

## Remarques

Un document DOCX ou DOC peut contenir une ou plusieurs parties de stockage de données XML personnalisées. Aspose.Words préserve et permet de créer et d'extraire des données XML personnalisées via le[`CustomXmlParts`](../../aspose.words/document/customxmlparts/) collection.

## Exemples

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

* espace de noms [Aspose.Words.Markup](../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../)
