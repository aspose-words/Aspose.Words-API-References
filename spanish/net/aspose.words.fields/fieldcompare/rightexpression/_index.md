---
title: FieldCompare.RightExpression
linktitle: RightExpression
articleTitle: RightExpression
second_title: Aspose.Words para .NET
description: Descubra la propiedad RightExpression de FieldCompare para administrar y personalizar fácilmente el lado derecho de sus expresiones de comparación para un rendimiento óptimo.
type: docs
weight: 40
url: /es/net/aspose.words.fields/fieldcompare/rightexpression/
---
## FieldCompare.RightExpression property

Obtiene o establece la parte derecha de la expresión de comparación.

```csharp
public string RightExpression { get; set; }
```

## Ejemplos

Muestra cómo comparar expresiones utilizando un campo COMPARAR.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldCompare field = (FieldCompare)builder.InsertField(FieldType.FieldCompare, true);
field.LeftExpression = "3";
field.ComparisonOperator = "<";
field.RightExpression = "2";
field.Update();

// El campo COMPARAR muestra un "0" o un "1", dependiendo de la veracidad de su afirmación.
//El resultado de esta declaración es falso, por lo que este campo mostrará un "0".
Assert.AreEqual(" COMPARE  3 < 2", field.GetFieldCode());
Assert.AreEqual("0", field.Result);

builder.Writeln();

field = (FieldCompare)builder.InsertField(FieldType.FieldCompare, true);
field.LeftExpression = "5";
field.ComparisonOperator = "=";
field.RightExpression = "2 + 3";
field.Update();

//Este campo muestra un "1" ya que la declaración es verdadera.
Assert.AreEqual(" COMPARE  5 = \"2 + 3\"", field.GetFieldCode());
Assert.AreEqual("1", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.COMPARE.docx");
```

### Ver también

* class [FieldCompare](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
