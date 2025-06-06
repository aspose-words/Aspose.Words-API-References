---
title: FieldDatabase Class
linktitle: FieldDatabase
articleTitle: FieldDatabase
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Fields.FieldDatabase para implementar eficientemente campos DATABASE en sus documentos. ¡Mejore la automatización de sus documentos hoy mismo!
type: docs
weight: 2150
url: /es/net/aspose.words.fields/fielddatabase/
---
## FieldDatabase class

Implementa el campo BASE DE DATOS.

Para obtener más información, visite el[Trabajar con campos](https://docs.aspose.com/words/net/working-with-fields/) Artículo de documentación.

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
| [FileName](../../aspose.words.fields/fielddatabase/filename/) { get; set; } | Obtiene o establece la ruta completa y el nombre del archivo de la base de datos |
| [FirstRecord](../../aspose.words.fields/fielddatabase/firstrecord/) { get; set; } | Obtiene o establece el número de registro integral del primer registro de datos a insertar. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtiene un[`FieldFormat`](../fieldformat/)objeto que proporciona acceso tipificado al formato del campo. |
| [FormatAttributes](../../aspose.words.fields/fielddatabase/formatattributes/) { get; set; } | Obtiene o establece qué atributos del formato se aplicarán a la tabla. |
| [InsertHeadings](../../aspose.words.fields/fielddatabase/insertheadings/) { get; set; } | Obtiene o establece si se deben insertar los nombres de campo de la base de datos como encabezados de columna en la tabla resultante. |
| [InsertOnceOnMailMerge](../../aspose.words.fields/fielddatabase/insertonceonmailmerge/) { get; set; } | Obtiene o establece si se deben insertar datos al comienzo de una fusión. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [LastRecord](../../aspose.words.fields/fielddatabase/lastrecord/) { get; set; } | Obtiene o establece el número de registro integral del último registro de datos a insertar. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtiene o establece el LCID del campo. |
| [Query](../../aspose.words.fields/fielddatabase/query/) { get; set; } | Obtiene o establece un conjunto de instrucciones SQL que consultan la base de datos. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtiene o establece el texto que está entre el separador de campo y el final del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtiene el nodo que representa el separador de campo. Puede ser`nulo` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtiene el nodo que representa el inicio del campo. |
| [TableFormat](../../aspose.words.fields/fielddatabase/tableformat/) { get; set; } | Obtiene o establece el formato que se aplicará al resultado de la consulta de base de datos. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtiene el tipo de campo de Microsoft Word. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). Se incluyen tanto el código de campo como el resultado de campo de los campos secundarios. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). |
| [Remove](../../aspose.words.fields/field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo padre, devuelve su párrafo padre. Si el campo ya se ha eliminado, devuelve`nulo` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Realiza la desvinculación del campo. |
| [Update](../../aspose.words.fields/field/update/)() | Realiza la actualización del campo. Se lanza una excepción si el campo ya se está actualizando. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Realiza una actualización de campo. Se lanza una excepción si el campo ya se está actualizando. |

## Observaciones

Inserta los resultados de una consulta de base de datos en una tabla WordprocessingML.

## Ejemplos

Muestra cómo extraer datos de una base de datos e insertarlos como un campo en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Este campo BASE DE DATOS ejecutará una consulta en una base de datos y mostrará el resultado en una tabla.
FieldDatabase field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = DatabaseDir + "Northwind.accdb";
field.Connection = "Provider=Microsoft.ACE.OLEDB.12.0";
field.Query = "SELECT * FROM [Products]";

Assert.AreEqual($" DATABASE  \\d {DatabaseDir.Replace("\\", "\\\\") + "Northwind.accdb"} \\c Provider=Microsoft.ACE.OLEDB.12.0 \\s \"SELECT * FROM [Products]\"", field.GetFieldCode());

// Inserte otro campo BASE DE DATOS con una consulta más compleja que ordene todos los productos en orden descendente por ventas brutas.
field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = DatabaseDir + "Northwind.accdb";
field.Connection = "Provider=Microsoft.ACE.OLEDB.12.0";
field.Query =
    "SELECT [Products].ProductName, FORMAT(SUM([Order Details].UnitPrice * (1 - [Order Details].Discount) * [Order Details].Quantity), 'Currency') AS GrossSales " +
    "FROM([Products] " +
    "LEFT JOIN[Order Details] ON[Products].[ProductID] = [Order Details].[ProductID]) " +
    "GROUP BY[Products].ProductName " +
    "ORDER BY SUM([Order Details].UnitPrice* (1 - [Order Details].Discount) * [Order Details].Quantity) DESC";

// Estas propiedades tienen la misma función que las cláusulas LIMIT y TOP.
// Configúrelos para mostrar solo las filas 1 a 10 del resultado de la consulta en la tabla del campo.
field.FirstRecord = "1";
field.LastRecord = "10";

Esta propiedad es el índice del formato que queremos usar para nuestra tabla. La lista de formatos de tabla se encuentra en el menú "Autoformato de tabla..."
// que aparece al crear un campo de BASE DE DATOS en Microsoft Word. El índice 10 corresponde al formato "Colorful 3".
field.TableFormat = "10";

// La propiedad FormatAttribute es una representación de cadena de un entero que almacena múltiples indicadores.
//Podemos aplicar de forma patriarcal el formato al que apunta la propiedad TableFormat estableciendo diferentes indicadores en esta propiedad.
// El número que utilizamos es la suma de una combinación de valores correspondientes a diferentes aspectos del estilo de la tabla.
// 63 representa 1 (bordes) + 2 (sombreado) + 4 (fuente) + 8 (color) + 16 (ajuste automático) + 32 (filas de encabezado).
field.FormatAttributes = "63";
field.InsertHeadings = true;
field.InsertOnceOnMailMerge = true;

doc.FieldOptions.FieldDatabaseProvider = new OleDbFieldDatabaseProvider();
doc.UpdateFields();

doc.Save(ArtifactsDir + "Field.DATABASE.docx");
```

### Ver también

* class [Field](../field/)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)
