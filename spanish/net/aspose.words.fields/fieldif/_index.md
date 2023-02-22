---
title: Class FieldIf
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Fields.FieldIf clase. Implementa el campo IF.
type: docs
weight: 1850
url: /es/net/aspose.words.fields/fieldif/
---
## FieldIf class

Implementa el campo IF.

```csharp
public class FieldIf : Field
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FieldIf](fieldif/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [ComparisonOperator](../../aspose.words.fields/fieldif/comparisonoperator/) { get; set; } | Obtiene o establece el operador de comparación. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtiene el texto que representa el resultado del campo mostrado. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtiene el nodo que representa el final del campo. |
| [FalseText](../../aspose.words.fields/fieldif/falsetext/) { get; set; } | Obtiene o establece el texto que se muestra si la expresión de comparación es falsa. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtiene un[`FieldFormat`](../fieldformat/) objeto que proporciona acceso escrito al formato del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [LeftExpression](../../aspose.words.fields/fieldif/leftexpression/) { get; set; } | Obtiene o establece la parte izquierda de la expresión de comparación. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtiene o establece el LCID del campo. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtiene o establece el texto que se encuentra entre el separador de campo y el final del campo. |
| [RightExpression](../../aspose.words.fields/fieldif/rightexpression/) { get; set; } | Obtiene o establece la parte derecha de la expresión de comparación. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtiene el nodo que representa el separador de campos. Puede ser nulo. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtiene el nodo que representa el inicio del campo. |
| [TrueText](../../aspose.words.fields/fieldif/truetext/) { get; set; } | Obtiene o establece el texto que se muestra si la expresión de comparación es verdadera. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtiene el tipo de campo de Microsoft Word. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [EvaluateCondition](../../aspose.words.fields/fieldif/evaluatecondition/)() | Evalúa la condición. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). Se incluyen tanto el código de campo como el resultado de campo de los campos secundarios. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). |
| [Remove](../../aspose.words.fields/field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo principal, devuelve su párrafo principal. Si el campo ya está eliminado, devuelve **nulo** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Realiza el desvinculado del campo. |
| [Update](../../aspose.words.fields/field/update/)() | Realiza la actualización del campo. Se lanza si el campo ya se está actualizando. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Realiza una actualización de campo. Se lanza si el campo ya se está actualizando. |

### Observaciones

Compara los valores designados por las expresiones[`LeftExpression`](./leftexpression/) y[`RightExpression`](./rightexpression/) en comparación usando el operador designado por[`ComparisonOperator`](./comparisonoperator/).

Se utilizará un campo con el siguiente formato como fuente de combinación de correspondencia: { IF 0 = 0 "{PatientsNameFML}" "" \* MERGEFORMAT }

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

* class [Field](../field/)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)


