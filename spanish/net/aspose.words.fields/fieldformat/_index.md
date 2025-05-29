---
title: FieldFormat Class
linktitle: FieldFormat
articleTitle: FieldFormat
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Fields.FieldFormat para acceder fácilmente a campos numéricos, de fecha y de hora. ¡Mejore el formato de sus documentos con potentes funciones!
type: docs
weight: 2350
url: /es/net/aspose.words.fields/fieldformat/
---
## FieldFormat class

Proporciona acceso escrito a los datos numéricos, de fecha y hora, y al formato general del campo.

Para obtener más información, visite el[Trabajar con campos](https://docs.aspose.com/words/net/working-with-fields/) Artículo de documentación.

```csharp
public class FieldFormat
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [DateTimeFormat](../../aspose.words.fields/fieldformat/datetimeformat/) { get; set; } | Obtiene o establece un formato que se aplica al resultado de un campo de fecha y hora. Corresponde al parámetro \@. |
| [GeneralFormats](../../aspose.words.fields/fieldformat/generalformats/) { get; } | Obtiene una colección de formatos generales que se aplican a un resultado numérico, de texto o de cualquier campo. Corresponde a los modificadores \*. |
| [NumericFormat](../../aspose.words.fields/fieldformat/numericformat/) { get; set; } | Obtiene o establece un formato que se aplica al resultado de un campo numérico. Corresponde al parámetro \#. |

## Ejemplos

Muestra cómo formatear los resultados del campo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Utilice un generador de documentos para insertar un campo que muestre un resultado sin formato aplicado.
Field field = builder.InsertField("= 2 + 3");

Assert.AreEqual("= 2 + 3", field.GetFieldCode());
Assert.AreEqual("5", field.Result);

//Podemos aplicar un formato al resultado de un campo usando las propiedades del campo.
//A continuación se muestran tres tipos de formatos que podemos aplicar al resultado de un campo.
// 1 - Formato numérico:
FieldFormat format = field.Format;
format.NumericFormat = "$###.00";
field.Update();

Assert.AreEqual("= 2 + 3 \\# $###.00", field.GetFieldCode());
Assert.AreEqual("$  5.00", field.Result);

// 2 - Formato de fecha y hora:
field = builder.InsertField("DATE");
format = field.Format;
format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());
Console.WriteLine($"Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

// 3 - Formato general:
field = builder.InsertField("= 25 + 33");
format = field.Format;
format.GeneralFormats.Add(GeneralFormat.LowercaseRoman);
format.GeneralFormats.Add(GeneralFormat.Upper);
field.Update();

int index = 0;
using (IEnumerator<GeneralFormat> generalFormatEnumerator = format.GeneralFormats.GetEnumerator())
    while (generalFormatEnumerator.MoveNext())
        Console.WriteLine($"General format index {index++}: {generalFormatEnumerator.Current}");

Assert.AreEqual("= 25 + 33 \\* roman \\* Upper", field.GetFieldCode());
Assert.AreEqual("LVIII", field.Result);
Assert.AreEqual(2, format.GeneralFormats.Count);
Assert.AreEqual(GeneralFormat.LowercaseRoman, format.GeneralFormats[0]);

//Podemos eliminar nuestros formatos para revertir el resultado del campo a su forma original.
format.GeneralFormats.Remove(GeneralFormat.LowercaseRoman);
format.GeneralFormats.RemoveAt(0);
Assert.AreEqual(0, format.GeneralFormats.Count);
field.Update();

Assert.AreEqual("= 25 + 33  ", field.GetFieldCode());
Assert.AreEqual("58", field.Result);
Assert.AreEqual(0, format.GeneralFormats.Count);
```

### Ver también

* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)
