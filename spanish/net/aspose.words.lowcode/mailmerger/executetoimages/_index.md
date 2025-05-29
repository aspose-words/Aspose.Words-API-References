---
title: MailMerger.ExecuteToImages
linktitle: ExecuteToImages
articleTitle: ExecuteToImages
second_title: Aspose.Words para .NET
description: Realice sin esfuerzo una combinación de correspondencia para registros individuales y convierta los resultados en imágenes de alta calidad con el método MailMerger ExecuteToImages.
type: docs
weight: 30
url: /es/net/aspose.words.lowcode/mailmerger/executetoimages/
---
## ExecuteToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_5}

Realiza una operación de combinación de correspondencia para un solo registro y convierte el resultado en imágenes.

```csharp
public static Stream[] ExecuteToImages(string inputFileName, ImageSaveOptions saveOptions, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFileName | String | El nombre del archivo de entrada. |
| saveOptions | ImageSaveOptions | Opciones de guardado de la salida. |
| fieldNames | String[] | Matriz de nombres de campos de combinación. Los nombres de campo no distinguen entre mayúsculas y minúsculas. Si se encuentra un nombre de campo que no se encuentra en el documento, se ignora. |
| fieldValues | Object[] | Matriz de valores que se insertarán en los campos de combinación. El número de elementos de esta matriz debe ser igual al número de elementos de fieldNames. |
| mailMergeOptions | MailMergeOptions | Opciones de combinación de correspondencia. |

## Ejemplos

Muestra cómo realizar la operación de combinación de correspondencia para un solo registro y guardar el resultado en imágenes.

```csharp
// Hay varias formas de realizar la operación de combinación de correspondencia:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

Stream[] images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), fieldNames, fieldValues, mailMergeOptions);
```

### Ver también

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## ExecuteToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_2}

Realiza una operación de combinación de correspondencia para un solo registro y convierte el resultado en imágenes.

```csharp
public static Stream[] ExecuteToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputStream | Stream | El flujo de archivo de entrada. |
| saveOptions | ImageSaveOptions | Opciones de guardado de la salida. |
| fieldNames | String[] | Matriz de nombres de campos de combinación. Los nombres de campo no distinguen entre mayúsculas y minúsculas. Si se encuentra un nombre de campo que no se encuentra en el documento, se ignora. |
| fieldValues | Object[] | Matriz de valores que se insertarán en los campos de combinación. El número de elementos de esta matriz debe ser igual al número de elementos de fieldNames. |
| mailMergeOptions | MailMergeOptions | Opciones de combinación de correspondencia. |

## Ejemplos

Muestra cómo realizar la operación de combinación de correspondencia para un solo registro del flujo y guardar el resultado en imágenes.

```csharp
// Hay varias formas de realizar la operación de combinación de correspondencia utilizando documentos del flujo:
string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    Stream[] images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), fieldNames, fieldValues);

    MailMergeOptions mailMergeOptions = new MailMergeOptions();
    mailMergeOptions.TrimWhitespaces = true;
    images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), fieldNames, fieldValues, mailMergeOptions);
}
```

### Ver también

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## ExecuteToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_3}

Realiza la fusión de correspondencia desde un DataRow al documento y procesa el resultado en imágenes.

```csharp
public static Stream[] ExecuteToImages(string inputFileName, ImageSaveOptions saveOptions, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFileName | String | El nombre del archivo de entrada. |
| saveOptions | ImageSaveOptions | Opciones de guardado de la salida. |
| dataRow | DataRow | Fila que contiene datos que se insertarán en los campos de combinación de correspondencia. Los nombres de campo no distinguen entre mayúsculas y minúsculas. Si se encuentra un nombre de campo que no se encuentra en el documento, se ignora. |
| mailMergeOptions | MailMergeOptions | Opciones de combinación de correspondencia. |

## Ejemplos

Muestra cómo realizar una operación de combinación de correspondencia desde un DataRow y guardar el resultado en imágenes.

```csharp
// Hay varias formas de realizar la operación de combinación de correspondencia desde un DataRow:
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

Stream[] images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataRow);
images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataRow, new MailMergeOptions() { TrimWhitespaces = true });
```

### Ver también

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## ExecuteToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages}

Realiza la fusión de correspondencia desde un DataRow al documento y procesa el resultado en imágenes.

```csharp
public static Stream[] ExecuteToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputStream | Stream | El flujo de archivo de entrada. |
| saveOptions | ImageSaveOptions | Opciones de guardado de la salida. |
| dataRow | DataRow | Fila que contiene datos que se insertarán en los campos de combinación de correspondencia. Los nombres de campo no distinguen entre mayúsculas y minúsculas. Si se encuentra un nombre de campo que no se encuentra en el documento, se ignora. |
| mailMergeOptions | MailMergeOptions | Opciones de combinación de correspondencia. |

## Ejemplos

Muestra cómo realizar una operación de combinación de correspondencia desde un DataRow utilizando documentos de la secuencia y guardar el resultado en imágenes.

```csharp
// Hay varias formas de realizar una operación de combinación de correspondencia desde un DataRow usando documentos del flujo:
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    Stream[] images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataRow);
    images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataRow, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### Ver también

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## ExecuteToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_4}

Realiza la fusión de correspondencia desde un DataRow al documento y procesa el resultado en imágenes.

```csharp
public static Stream[] ExecuteToImages(string inputFileName, ImageSaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFileName | String | El nombre del archivo de entrada. |
| saveOptions | ImageSaveOptions | Opciones de guardado de la salida. |
| dataTable | DataTable | Tabla que contiene datos que se insertarán en los campos de combinación de correspondencia. Los nombres de campo no distinguen entre mayúsculas y minúsculas. Si se encuentra un nombre de campo que no se encuentra en el documento, se ignora. |
| mailMergeOptions | MailMergeOptions | Opciones de combinación de correspondencia. |

## Ejemplos

Muestra cómo realizar la operación de combinación de correspondencia desde una DataTable y guardar el resultado en imágenes.

```csharp
// Hay varias formas de realizar la operación de combinación de correspondencia desde una DataTable:
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

Stream[] images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataTable);
images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataTable, new MailMergeOptions() { TrimWhitespaces = true });
```

### Ver también

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## ExecuteToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_1}

Realiza la fusión de correspondencia desde un DataRow al documento y procesa el resultado en imágenes.

```csharp
public static Stream[] ExecuteToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputStream | Stream | El flujo de archivo de entrada. |
| saveOptions | ImageSaveOptions | Opciones de guardado de la salida. |
| dataTable | DataTable | Tabla que contiene datos que se insertarán en los campos de combinación de correspondencia. Los nombres de campo no distinguen entre mayúsculas y minúsculas. Si se encuentra un nombre de campo que no se encuentra en el documento, se ignora. |
| mailMergeOptions | MailMergeOptions | Opciones de combinación de correspondencia. |

## Ejemplos

Muestra cómo realizar una operación de combinación de correspondencia desde una DataTable utilizando documentos de la secuencia y guardándolos en imágenes.

```csharp
Hay varias formas de realizar una operación de combinación de correspondencia desde una DataTable usando documentos del flujo y guardar el resultado en imágenes:
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    Stream[] images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataTable);
    images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataTable, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### Ver también

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)
