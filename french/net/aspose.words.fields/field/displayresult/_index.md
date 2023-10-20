---
title: Field.DisplayResult
linktitle: DisplayResult
articleTitle: DisplayResult
second_title: Aspose.Words pour .NET
description: Field DisplayResult propriété. Obtient le texte qui représente le résultat du champ affiché en C#.
type: docs
weight: 10
url: /fr/net/aspose.words.fields/field/displayresult/
---
## Field.DisplayResult property

Obtient le texte qui représente le résultat du champ affiché.

```csharp
public string DisplayResult { get; }
```

## Remarques

Le[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/) la méthode doit être appelée pour obtenir la valeur correcte pour the [`FieldListNum`](../../fieldlistnum/) ,[`FieldAutoNum`](../../fieldautonum/) ,[`FieldAutoNumOut`](../../fieldautonumout/) et[`FieldAutoNumLgl`](../../fieldautonumlgl/) champs.

## Exemples

Montre comment obtenir le texte réel affiché par un champ dans le document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This document was written by ");
FieldAuthor fieldAuthor = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
fieldAuthor.AuthorName = "John Doe";

// Nous pouvons utiliser la propriété DisplayResult pour vérifier quel texte exact
// un champ s'afficherait à sa place dans le document.
Assert.AreEqual(string.Empty, fieldAuthor.DisplayResult);

 // Les champs ne conservent pas les valeurs de résultat précises en temps réel.
// Pour nous assurer que nos champs affichent des résultats précis à tout moment,
// comme juste avant une opération de sauvegarde, nous devons les mettre à jour manuellement.
fieldAuthor.Update();

Assert.AreEqual("John Doe", fieldAuthor.DisplayResult);

doc.Save(ArtifactsDir + "Field.DisplayResult.docx");
```

### Voir également

* class [Field](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
