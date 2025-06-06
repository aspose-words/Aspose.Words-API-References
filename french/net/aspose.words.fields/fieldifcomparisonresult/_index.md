---
title: FieldIfComparisonResult Enum
linktitle: FieldIfComparisonResult
articleTitle: FieldIfComparisonResult
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Fields.FieldIfComparisonResult, qui définit les résultats des évaluations de champs IF, améliorant ainsi vos capacités d'automatisation de documents.
type: docs
weight: 2420
url: /fr/net/aspose.words.fields/fieldifcomparisonresult/
---
## FieldIfComparisonResult enumeration

Spécifie le résultat de l'évaluation de la condition du champ IF.

```csharp
public enum FieldIfComparisonResult
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Error | `0` | Il y a une erreur dans la condition. |
| True | `1` | La condition est`vrai` . |
| False | `2` | La condition est`FAUX` . |

## Exemples

Montre comment insérer un champ SI.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Statement 1: ");
FieldIf field = (FieldIf)builder.InsertField(FieldType.FieldIf, true);
field.LeftExpression = "0";
field.ComparisonOperator = "=";
field.RightExpression = "1";

// Le champ IF affichera une chaîne provenant de sa propriété « TrueText »,
// ou sa propriété "FalseText", selon la véracité de l'énoncé que nous avons construit.
field.TrueText = "True";
field.FalseText = "False";
field.Update();

// Dans ce cas, "0 = 1" est incorrect, donc le résultat affiché sera "Faux".
Assert.AreEqual(" IF  0 = 1 True False", field.GetFieldCode());
Assert.AreEqual(FieldIfComparisonResult.False, field.EvaluateCondition());
Assert.AreEqual("False", field.Result);

builder.Write("\nStatement 2: ");
field = (FieldIf)builder.InsertField(FieldType.FieldIf, true);
field.LeftExpression = "5";
field.ComparisonOperator = "=";
field.RightExpression = "2 + 3";
field.TrueText = "True";
field.FalseText = "False";
field.Update();

// Cette fois, l'instruction est correcte, donc le résultat affiché sera « Vrai ».
Assert.AreEqual(" IF  5 = \"2 + 3\" True False", field.GetFieldCode());
Assert.AreEqual(FieldIfComparisonResult.True, field.EvaluateCondition());
Assert.AreEqual("True", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.IF.docx");
```

### Voir également

* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)
