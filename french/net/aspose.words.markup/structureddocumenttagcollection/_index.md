---
title: StructuredDocumentTagCollection Class
linktitle: StructuredDocumentTagCollection
articleTitle: StructuredDocumentTagCollection
second_title: Aspose.Words pour .NET
description: Explorez la classe Aspose.Words.Markup.StructuredDocumentTagCollection pour une gestion efficace des balises de documents structurés, améliorant ainsi vos capacités de traitement de documents.
type: docs
weight: 4760
url: /fr/net/aspose.words.markup/structureddocumenttagcollection/
---
## StructuredDocumentTagCollection class

Une collection de[`IStructuredDocumentTag`](../istructureddocumenttag/) instances qui représentent les balises de document structurées dans la plage spécifiée.

Pour en savoir plus, visitez le[Balises de documents structurés ou contrôle de contenu](https://docs.aspose.com/words/net/working-with-content-control-sdt/) article de documentation.

```csharp
public class StructuredDocumentTagCollection : IEnumerable<IStructuredDocumentTag>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words.markup/structureddocumenttagcollection/count/) { get; } | Renvoie le nombre de balises de documents structurés dans la collection. |
| [Item](../../aspose.words.markup/structureddocumenttagcollection/item/) { get; } | Renvoie la balise de document structuré à l'index spécifié. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetById](../../aspose.words.markup/structureddocumenttagcollection/getbyid/)(*int*) | Renvoie la balise du document structuré par identifiant. |
| [GetByTag](../../aspose.words.markup/structureddocumenttagcollection/getbytag/)(*string*) | Renvoie la première balise de document structuré rencontrée dans la collection avec la balise spécifiée. |
| [GetByTitle](../../aspose.words.markup/structureddocumenttagcollection/getbytitle/)(*string*) | Renvoie la première balise de document structuré rencontrée dans la collection avec le titre spécifié. |
| [GetEnumerator](../../aspose.words.markup/structureddocumenttagcollection/getenumerator/)() | Renvoie un objet énumérateur. |
| [Remove](../../aspose.words.markup/structureddocumenttagcollection/remove/)(*int*) | Supprime la balise de document structuré avec l'identifiant spécifié. |
| [RemoveAt](../../aspose.words.markup/structureddocumenttagcollection/removeat/)(*int*) | Supprime une balise de document structuré à l'index spécifié. |

## Exemples

Montre comment obtenir une balise de document structurée.

```csharp
Document doc = new Document(MyDir + "Structured document tags by id.docx");

// Récupérez la balise du document structuré par ID.
IStructuredDocumentTag sdt = doc.Range.StructuredDocumentTags.GetById(1160505028);
Console.WriteLine(sdt.IsMultiSection);
Console.WriteLine(sdt.Title);

// Obtenez la balise de document structurée ou la balise à distance par titre.
sdt = doc.Range.StructuredDocumentTags.GetByTitle("Alias4");
Console.WriteLine(sdt.Id);
```

### Voir également

* interface [IStructuredDocumentTag](../istructureddocumenttag/)
* espace de noms [Aspose.Words.Markup](../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../)
