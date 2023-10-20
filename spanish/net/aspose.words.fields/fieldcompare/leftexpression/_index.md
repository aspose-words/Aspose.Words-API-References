---
title: FieldCompare.LeftExpression
linktitle: LeftExpression
articleTitle: LeftExpression
second_title: Aspose.Words para .NET
description: FieldCompare LeftExpression propiedad. Obtiene o establece la parte izquierda de la expresión de comparación en C#.
type: docs
weight: 30
url: /es/net/aspose.words.fields/fieldcompare/leftexpression/
---
## FieldCompare.LeftExpression property

Obtiene o establece la parte izquierda de la expresión de comparación.

```csharp
public string LeftExpression { get; set; }
```

## Ejemplos

Muestra cómo comparar expresiones usando un campo COMPARE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldCompare field = (FieldCompare)builder.InsertField(FieldType.FieldCompare, true);
field.LeftExpression = "3";
field.ComparisonOperator = "<";
field.RightExpression = "2";
field.Update();

// El campo COMPARAR muestra un "0" o un "1", dependiendo de la veracidad de su declaración.
// El resultado de esta declaración es falso por lo que este campo mostrará un "0".
Assert.AreEqual(" COMPARE  3 < 2", field.GetFieldCode());
Assert.AreEqual("0", field.Result);

builder.Writeln();

field = (FieldCompare)builder.InsertField(FieldType.FieldCompare, true);
field.LeftExpression = "5";
field.ComparisonOperator = "=";
field.RightExpression = "2 + 3";
field.Update();

// Este campo muestra un "1" ya que la afirmación es verdadera.
Assert.AreEqual(" COMPARE  5 = \"2 + 3\"", field.GetFieldCode());
Assert.AreEqual("1", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.COMPARE.docx");
```

### Ver también

* class [FieldCompare](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
