---
title: FieldIf.LeftExpression
linktitle: LeftExpression
articleTitle: LeftExpression
second_title: Aspose.Words pour .NET
description: Découvrez la propriété LeftExpression de FieldIf, gérez facilement le côté gauche de votre expression de comparaison pour une gestion et une analyse améliorées des données.
type: docs
weight: 40
url: /fr/net/aspose.words.fields/fieldif/leftexpression/
---
## FieldIf.LeftExpression property

Obtient ou définit la partie gauche de l'expression de comparaison.

```csharp
public string LeftExpression { get; set; }
```

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

* class [FieldIf](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
