---
title: Class FieldDatabase
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Fields.FieldDatabase clase. Implementa el campo BASE DE DATOS.
type: docs
weight: 1590
url: /es/net/aspose.words.fields/fielddatabase/
---
## FieldDatabase class

Implementa el campo BASE DE DATOS.

```csharp
public class FieldDatabase : Field
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FieldDatabase](fielddatabase/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Connection](../../aspose.words.fields/fielddatabase/connection/) { get; set; } | Obtiene o establece una conexión a los datos. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtiene el texto que representa el resultado del campo mostrado. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtiene el nodo que representa el final del campo. |
| [FileName](../../aspose.words.fields/fielddatabase/filename/) { get; set; } | Obtiene o establece la ruta completa y el nombre de archivo de la base de datos |
| [FirstRecord](../../aspose.words.fields/fielddatabase/firstrecord/) { get; set; } | Obtiene o establece el número de registro integral del primer registro de datos a insertar. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtiene un[`FieldFormat`](../fieldformat/) objeto que proporciona acceso escrito al formato del campo. |
| [FormatAttributes](../../aspose.words.fields/fielddatabase/formatattributes/) { get; set; } | Obtiene o establece qué atributos del formato se aplicarán a la tabla. |
| [InsertHeadings](../../aspose.words.fields/fielddatabase/insertheadings/) { get; set; } | Obtiene o establece si insertar los nombres de campo de la base de datos como encabezados de columna en la tabla resultante. |
| [InsertOnceOnMailMerge](../../aspose.words.fields/fielddatabase/insertonceonmailmerge/) { get; set; } | Obtiene o establece si se insertan datos al comienzo de una combinación. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [LastRecord](../../aspose.words.fields/fielddatabase/lastrecord/) { get; set; } | Obtiene o establece el número de registro integral del último registro de datos a insertar. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtiene o establece el LCID del campo. |
| [Query](../../aspose.words.fields/fielddatabase/query/) { get; set; } | Obtiene o establece un conjunto de instrucciones SQL que consultan la base de datos. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtiene o establece el texto que se encuentra entre el separador de campo y el final del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtiene el nodo que representa el separador de campos. Puede ser nulo. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtiene el nodo que representa el inicio del campo. |
| [TableFormat](../../aspose.words.fields/fielddatabase/tableformat/) { get; set; } | Obtiene o establece el formato que se aplicará al resultado de la consulta a la base de datos. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtiene el tipo de campo de Microsoft Word. |

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

Inserta los resultados de una consulta de base de datos en una tabla de WordprocessingML.

### Ejemplos

Muestra cómo extraer datos de una base de datos e insertarlos como un campo en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Este campo BASE DE DATOS ejecutará una consulta en una base de datos y mostrará el resultado en una tabla.
FieldDatabase field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = MyDir + @"Database\Northwind.mdb";
field.Connection = "DSN=MS Access Databases";
field.Query = "SELECT * FROM [Products]";

Assert.AreEqual($" DATABASE  \\d \"{DatabaseDir.Replace("\\", "\\\\") + "Northwind.mdb"}\" \\c \"DSN=MS Access Databases\" \\s \"SELECT * FROM [Products]\"", 
    field.GetFieldCode());

// Inserte otro campo de BASE DE DATOS con una consulta más compleja que clasifique todos los productos en orden descendente por ventas brutas.
field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = MyDir + @"Database\Northwind.mdb";
field.Connection = "DSN=MS Access Databases";
field.Query =
    "SELECT [Products].ProductName, FORMAT(SUM([Order Details].UnitPrice * (1 - [Order Details].Discount) * [Order Details].Quantity), 'Currency') AS GrossSales " +
    "FROM([Products] " +
    "LEFT JOIN[Order Details] ON[Products].[ProductID] = [Order Details].[ProductID]) " +
    "GROUP BY[Products].ProductName " +
    "ORDER BY SUM([Order Details].UnitPrice* (1 - [Order Details].Discount) * [Order Details].Quantity) DESC";

// Estas propiedades tienen la misma función que las cláusulas LIMIT y TOP.
// Configurarlos para mostrar solo las filas 1 a 10 del resultado de la consulta en la tabla del campo.
field.FirstRecord = "1";
field.LastRecord = "10";

// Esta propiedad es el índice del formato que queremos usar para nuestra tabla. La lista de formatos de tabla se encuentra en el menú "Autoformato de tabla..."
// que aparece cuando creamos un campo BASE DE DATOS en Microsoft Word. El índice #10 corresponde al formato "Colorful 3".
field.TableFormat = "10";

// La propiedad FormatAttribute es una representación de cadena de un número entero que almacena varias banderas.
// Podemos aplicar patrialmente el formato al que apunta la propiedad TableFormat configurando diferentes banderas en esta propiedad.
// El número que usamos es la suma de una combinación de valores correspondientes a diferentes aspectos del estilo de la tabla.
// 63 representa 1 (bordes) + 2 (sombreado) + 4 (fuente) + 8 (color) + 16 (ajuste automático) + 32 (filas de encabezado).
field.FormatAttributes = "63";
field.InsertHeadings = true;
field.InsertOnceOnMailMerge = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.DATABASE.docx");
```

### Ver también

* class [Field](../field/)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)


