---
title: GeneralFormatCollection Class
linktitle: GeneralFormatCollection
articleTitle: GeneralFormatCollection
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Fields.GeneralFormatCollection: una poderosa colección tipada para administrar formatos generales sin esfuerzo en sus documentos.
type: docs
weight: 3060
url: /es/net/aspose.words.fields/generalformatcollection/
---
## GeneralFormatCollection class

Representa una colección tipificada de formatos generales.

Para obtener más información, visite el[Trabajar con campos](https://docs.aspose.com/words/net/working-with-fields/) Artículo de documentación.

```csharp
public class GeneralFormatCollection : IEnumerable<GeneralFormat>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words.fields/generalformatcollection/count/) { get; } | Obtiene el número total de elementos de la colección. |
| [Item](../../aspose.words.fields/generalformatcollection/item/) { get; } | Obtiene un formato general en el índice especificado. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Add](../../aspose.words.fields/generalformatcollection/add/)(*[GeneralFormat](../generalformat/)*) | Agrega un formato general a la colección. |
| [GetEnumerator](../../aspose.words.fields/generalformatcollection/getenumerator/)() | Devuelve un objeto enumerador. |
| [Remove](../../aspose.words.fields/generalformatcollection/remove/)(*[GeneralFormat](../generalformat/)*) | Elimina todas las ocurrencias del formato general especificado de la colección. |
| [RemoveAt](../../aspose.words.fields/generalformatcollection/removeat/)(*int*) | Elimina una ocurrencia de formato general en el índice especificado. |

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

* enum [GeneralFormat](../generalformat/)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)
