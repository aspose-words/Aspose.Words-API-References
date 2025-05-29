---
title: Range Class
linktitle: Range
articleTitle: Range
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Range, la clé pour gérer facilement les sections de vos documents. Améliorez le traitement de vos documents grâce à un contrôle et une flexibilité optimaux.
type: docs
weight: 5250
url: /fr/net/aspose.words/range/
---
## Range class

Représente une zone contiguë dans un document.

Pour en savoir plus, visitez le[Travailler avec des plages](https://docs.aspose.com/words/net/working-with-ranges/) article de documentation.

```csharp
public class Range : IEnumerable<Node>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Bookmarks](../../aspose.words/range/bookmarks/) { get; } | Renvoie un[`Bookmarks`](./bookmarks/) collection qui représente tous les signets de la plage. |
| [Fields](../../aspose.words/range/fields/) { get; } | Renvoie un[`Fields`](./fields/) collection qui représente tous les champs de la plage. |
| [FormFields](../../aspose.words/range/formfields/) { get; } | Renvoie un[`FormFields`](./formfields/) collection qui représente tous les champs de formulaire de la plage. |
| [Revisions](../../aspose.words/range/revisions/) { get; } | Obtient une collection de révisions (modifications suivies) qui existent dans cette plage. |
| [StructuredDocumentTags](../../aspose.words/range/structureddocumenttags/) { get; } | Renvoie un[`StructuredDocumentTags`](./structureddocumenttags/) collection qui représente toutes les balises de documents structurés dans la plage. |
| [Text](../../aspose.words/range/text/) { get; } | Obtient le texte de la plage. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Delete](../../aspose.words/range/delete/)() | Supprime tous les caractères de la plage. |
| [GetEnumerator](../../aspose.words/range/getenumerator/)() |  |
| [NormalizeFieldTypes](../../aspose.words/range/normalizefieldtypes/)() | Modifie les valeurs du type de champ[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype/) de[`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../aspose.words.fields/fieldend/) dans cette plage afin qu'ils correspondent aux types de champs contenus dans les codes de champ. |
| [Replace](../../aspose.words/range/replace/#replace_2)(*Regex, string*) | Remplace toutes les occurrences d'un modèle de caractère spécifié par une expression régulière par une autre chaîne. |
| [Replace](../../aspose.words/range/replace/#replace)(*string, string*) | Remplace toutes les occurrences d'un modèle de chaîne de caractères spécifié par une chaîne de remplacement. |
| [Replace](../../aspose.words/range/replace/#replace_3)(*Regex, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | Remplace toutes les occurrences d'un modèle de caractère spécifié par une expression régulière par une autre chaîne. |
| [Replace](../../aspose.words/range/replace/#replace_1)(*string, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | Remplace toutes les occurrences d'un modèle de chaîne de caractères spécifié par une chaîne de remplacement. |
| [ToDocument](../../aspose.words/range/todocument/)() | Construit un nouveau document entièrement formé qui contient la plage. |
| [UnlinkFields](../../aspose.words/range/unlinkfields/)() | Dissocie les champs de cette plage. |
| [UpdateFields](../../aspose.words/range/updatefields/)() | Met à jour les valeurs des champs de document dans cette plage. |

## Remarques

Le document est représenté par un arbre de nœuds et les nœuds fournissent des opérations pour travailler avec l'arbre, mais certaines opérations sont plus faciles à réaliser si le document est traité comme une séquence contiguë de texte.

`Range` est une interface « façade » qui fournit des méthodes qui traitent le document ou des parties du document comme du texte « plat », indépendamment du fait que les nœuds document sont stockés dans un modèle d'objet de type arborescence.

`Range` ne contient aucun texte ni nœud, c'est simplement une vue ou une « fenêtre » sur un fragment d'un document.

## Exemples

Montre comment obtenir le contenu textuel de tous les nœuds couverts par une plage.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.Range.Text.Trim());
```

### Voir également

* class [Node](../node/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
