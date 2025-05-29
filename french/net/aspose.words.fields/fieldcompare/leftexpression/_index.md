---
title: FieldCompare.LeftExpression
linktitle: LeftExpression
articleTitle: LeftExpression
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FieldCompare LeftExpression, accédez ou modifiez facilement le côté gauche de vos expressions de comparaison pour une analyse de données améliorée.
type: docs
weight: 30
url: /fr/net/aspose.words.fields/fieldcompare/leftexpression/
---
## FieldCompare.LeftExpression property

Obtient ou définit la partie gauche de l'expression de comparaison.

```csharp
public string LeftExpression { get; set; }
```

## Exemples

Montre comment comparer des expressions à l'aide d'un champ COMPARE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldCompare field = (FieldCompare)builder.InsertField(FieldType.FieldCompare, true);
field.LeftExpression = "3";
field.ComparisonOperator = "<";
field.RightExpression = "2";
field.Update();

// Le champ COMPARE affiche un « 0 » ou un « 1 », selon la véracité de son affirmation.
// Le résultat de cette instruction est faux, donc ce champ affichera un « 0 ».
Assert.AreEqual(" COMPARE  3 < 2", field.GetFieldCode());
Assert.AreEqual("0", field.Result);

builder.Writeln();

field = (FieldCompare)builder.InsertField(FieldType.FieldCompare, true);
field.LeftExpression = "5";
field.ComparisonOperator = "=";
field.RightExpression = "2 + 3";
field.Update();

// Ce champ affiche un « 1 » puisque l'affirmation est vraie.
Assert.AreEqual(" COMPARE  5 = \"2 + 3\"", field.GetFieldCode());
Assert.AreEqual("1", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.COMPARE.docx");
```

### Voir également

* class [FieldCompare](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
