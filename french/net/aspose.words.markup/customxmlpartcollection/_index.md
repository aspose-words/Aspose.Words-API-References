---
title: CustomXmlPartCollection
second_title: Référence de l'API Aspose.Words pour .NET
description: Représente une collection de parties XML personnalisées. Les articles sontCustomXmlPart./customxmlpart objets.
type: docs
weight: 3690
url: /fr/net/aspose.words.markup/customxmlpartcollection/
---
## CustomXmlPartCollection class

Représente une collection de parties XML personnalisées. Les articles sont[`CustomXmlPart`](../customxmlpart) objets.

```csharp
public class CustomXmlPartCollection : IEnumerable<CustomXmlPart>
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [CustomXmlPartCollection](customxmlpartcollection)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words.markup/customxmlpartcollection/count) { get; } | Obtient le nombre d'éléments contenus dans la collection. |
| [Item](../../aspose.words.markup/customxmlpartcollection/item) { get; set; } | Obtient ou définit un élément à l'index spécifié. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlpartcollection/add#add_1)(CustomXmlPart) | Ajoute un élément à la collection. |
| [Add](../../aspose.words.markup/customxmlpartcollection/add#add)(string, string) | Crée une nouvelle partie XML avec le XML spécifié et l'ajoute à la collection. |
| [Clear](../../aspose.words.markup/customxmlpartcollection/clear)() | Supprime tous les éléments de la collection. |
| [Clone](../../aspose.words.markup/customxmlpartcollection/clone)() | Crée une copie complète de cette collection et de ses éléments. |
| [GetById](../../aspose.words.markup/customxmlpartcollection/getbyid)(string) | Recherche et renvoie une partie XML personnalisée par son identifiant. |
| [GetEnumerator](../../aspose.words.markup/customxmlpartcollection/getenumerator)() | Renvoie un objet énumérateur qui peut être utilisé pour itérer sur tous les éléments de la collection. |
| [RemoveAt](../../aspose.words.markup/customxmlpartcollection/removeat)(int) | Supprime un élément à l'index spécifié. |

### Remarques

Vous n'avez normalement pas besoin de créer des instances de cette classe. Vous pouvez accéder aux données XML personnalisées stockées dans un document via le[`CustomXmlParts`](../../aspose.words/document/customxmlparts) propriété.

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

* class [CustomXmlPart](../customxmlpart)
* espace de noms [Aspose.Words.Markup](../../aspose.words.markup)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
