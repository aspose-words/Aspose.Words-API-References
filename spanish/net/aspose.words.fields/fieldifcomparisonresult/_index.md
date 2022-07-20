---
title: FieldIfComparisonResult
second_title: Referencia de API de Aspose.Words para .NET
description: Especifica el resultado de la evaluación de la condición del campo IF.
type: docs
weight: 1860
url: /es/net/aspose.words.fields/fieldifcomparisonresult/
---
## FieldIfComparisonResult enumeration

Especifica el resultado de la evaluación de la condición del campo IF.

```csharp
public enum FieldIfComparisonResult
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Error | `0` | Hay un error en la condición. |
| True | `1` | La condición es`verdadero` . |
| False | `2` | La condición es`falso` . |

### Ejemplos

Muestra cómo insertar un campo IF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Statement 1: ");
FieldIf field = (FieldIf)builder.InsertField(FieldType.FieldIf, true);
field.LeftExpression = "0";
field.ComparisonOperator = "=";
field.RightExpression = "1";

// El campo IF mostrará una cadena de su propiedad "TrueText",
// o su propiedad "FalseText", dependiendo de la verdad del enunciado que hayamos construido.
field.TrueText = "True";
field.FalseText = "False";
field.Update();

// En este caso, "0 = 1" es incorrecto, por lo que el resultado mostrado será "Falso".
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

// Esta vez la afirmación es correcta, por lo que el resultado mostrado será "Verdadero".
Assert.AreEqual(" IF  5 = \"2 + 3\" True False", field.GetFieldCode());
Assert.AreEqual(FieldIfComparisonResult.True, field.EvaluateCondition());
Assert.AreEqual("True", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.IF.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->