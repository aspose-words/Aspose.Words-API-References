---
title: FieldAdvance
second_title: Referencia de API de Aspose.Words para .NET
description: Implementa el campo ADVANCE.
type: docs
weight: 1390
url: /es/net/aspose.words.fields/fieldadvance/
---
## FieldAdvance class

Implementa el campo ADVANCE.

```csharp
public class FieldAdvance : Field
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FieldAdvance](fieldadvance/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtiene el texto que representa el resultado del campo mostrado. |
| [DownOffset](../../aspose.words.fields/fieldadvance/downoffset/) { get; set; } | Obtiene o establece el número de puntos por los que se debe mover hacia abajo el texto que sigue al campo. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtiene el nodo que representa el final del campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtiene un[`FieldFormat`](../fieldformat/) objeto que proporciona acceso escrito al formato del campo. |
| [HorizontalPosition](../../aspose.words.fields/fieldadvance/horizontalposition/) { get; set; } | Obtiene o establece el número de puntos por los que el texto que sigue al campo debe moverse horizontalmente desde el borde izquierdo de la columna, marco o cuadro de texto. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [LeftOffset](../../aspose.words.fields/fieldadvance/leftoffset/) { get; set; } | Obtiene o establece el número de puntos por los que se debe mover hacia la izquierda el texto que sigue al campo. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtiene o establece el LCID del campo. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtiene o establece el texto que se encuentra entre el separador de campo y el final del campo. |
| [RightOffset](../../aspose.words.fields/fieldadvance/rightoffset/) { get; set; } | Obtiene o establece el número de puntos por los que el texto que sigue al campo debe moverse hacia la derecha. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtiene el nodo que representa el separador de campos. Puede ser nulo. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtiene el nodo que representa el inicio del campo. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtiene el tipo de campo de Microsoft Word. |
| [UpOffset](../../aspose.words.fields/fieldadvance/upoffset/) { get; set; } | Obtiene o establece el número de puntos por los que se debe mover hacia arriba el texto que sigue al campo. |
| [VerticalPosition](../../aspose.words.fields/fieldadvance/verticalposition/) { get; set; } | Obtiene o establece el número de puntos por los que el texto que sigue al campo debe moverse verticalmente desde el borde superior de la página. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). Se incluyen tanto el código de campo como el resultado de campo de los campos secundarios. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). |
| [Remove](../../aspose.words.fields/field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo principal, devuelve su párrafo principal. Si el campo ya está eliminado, devuelve **nulo** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Realiza el desvinculado del campo. |
| [Update](../../aspose.words.fields/field/update/)() | Realiza la actualización del campo. Se lanza si el campo ya se está actualizando. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Realiza una actualización de campo. Se lanza si el campo ya se está actualizando. |

### Observaciones

Mueve el punto de inicio en el que se muestra el texto que sigue léxicamente al campo a la derecha o a la izquierda, hacia arriba o hacia abajo, o a una posición horizontal o vertical específica.

### Ejemplos

Muestra cómo insertar un campo ADVANCE y editar sus propiedades.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This text is in its normal place.");

// A continuación se muestran dos formas de usar el campo ADVANCE para ajustar la posición del texto que lo sigue.
// Los efectos de un campo ADVANCE continúan aplicándose hasta que finaliza el párrafo,
// u otro campo ADVANCE actualiza los valores de desplazamiento/coordenada.
// 1 - Especifique un desplazamiento direccional:
FieldAdvance field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.RightOffset = "5";
field.UpOffset = "5";

Assert.AreEqual(" ADVANCE  \\r 5 \\u 5", field.GetFieldCode());

builder.Write("This text will be moved up and to the right.");

field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.DownOffset = "5";
field.LeftOffset = "100";

Assert.AreEqual(" ADVANCE  \\d 5 \\l 100", field.GetFieldCode());

builder.Writeln("This text is moved down and to the left, overlapping the previous text.");

// 2 - Mover texto a una posición especificada por coordenadas:
field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.HorizontalPosition = "-100";
field.VerticalPosition = "200";

Assert.AreEqual(" ADVANCE  \\x -100 \\y 200", field.GetFieldCode());

builder.Write("This text is in a custom position.");

doc.Save(ArtifactsDir + "Field.ADVANCE.docx");
```

### Ver también

* class [Field](../field/)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
