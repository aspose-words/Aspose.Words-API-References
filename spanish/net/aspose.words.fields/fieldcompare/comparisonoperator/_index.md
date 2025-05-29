---
title: FieldCompare.ComparisonOperator
linktitle: ComparisonOperator
articleTitle: ComparisonOperator
second_title: Aspose.Words para .NET
description: Descubra la propiedad FieldCompare ComparisonOperator: administre fácilmente sus operadores de comparación para mejorar el análisis y la eficiencia de los datos.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldcompare/comparisonoperator/
---
## FieldCompare.ComparisonOperator property

Obtiene o establece el operador de comparación.

```csharp
public string ComparisonOperator { get; set; }
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
