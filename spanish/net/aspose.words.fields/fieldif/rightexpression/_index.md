---
title: FieldIf.RightExpression
linktitle: RightExpression
articleTitle: RightExpression
second_title: Aspose.Words para .NET
description: Descubra la propiedad FieldIf RightExpression, administre fácilmente el segmento correcto de sus expresiones de comparación para mejorar la precisión y eficiencia de los datos.
type: docs
weight: 50
url: /es/net/aspose.words.fields/fieldif/rightexpression/
---
## FieldIf.RightExpression property

Obtiene o establece la parte derecha de la expresión de comparación.

```csharp
public string RightExpression { get; set; }
```

## Ejemplos

Muestra cómo insertar un campo SI.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Statement 1: ");
FieldIf field = (FieldIf)builder.InsertField(FieldType.FieldIf, true);
field.LeftExpression = "0";
field.ComparisonOperator = "=";
field.RightExpression = "1";

// El campo SI mostrará una cadena de su propiedad "TrueText",
// o su propiedad "FalseText", dependiendo de la verdad de la declaración que hemos construido.
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

* class [FieldIf](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
