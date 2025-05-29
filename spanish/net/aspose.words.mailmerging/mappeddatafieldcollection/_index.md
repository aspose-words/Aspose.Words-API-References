---
title: MappedDataFieldCollection Class
linktitle: MappedDataFieldCollection
articleTitle: MappedDataFieldCollection
second_title: Aspose.Words para .NET
description: Descubra Aspose.Words.MailMerging.MappedDataFieldCollection para una asignación perfecta de campos de fuente de datos a campos de combinación de correspondencia, mejorando la automatización de documentos.
type: docs
weight: 4560
url: /es/net/aspose.words.mailmerging/mappeddatafieldcollection/
---
## MappedDataFieldCollection class

Permite asignar automáticamente entre los nombres de los campos en su fuente de datos y los nombres de los campos de combinación de correspondencia en el documento.

Para obtener más información, visite el[Combinación de correspondencia e informes](https://docs.aspose.com/words/net/mail-merge-and-reporting/) Artículo de documentación.

```csharp
public class MappedDataFieldCollection : IEnumerable<KeyValuePair<string, string>>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words.mailmerging/mappeddatafieldcollection/count/) { get; } | Obtiene el número de elementos contenidos en la colección. |
| [Item](../../aspose.words.mailmerging/mappeddatafieldcollection/item/) { get; set; } | Obtiene o establece el nombre del campo en la fuente de datos asociado con el campo de combinación de correspondencia especificado. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Add](../../aspose.words.mailmerging/mappeddatafieldcollection/add/)(*string, string*) | Agrega una nueva asignación de campo. |
| [Clear](../../aspose.words.mailmerging/mappeddatafieldcollection/clear/)() | Elimina todos los elementos de la colección. |
| [ContainsKey](../../aspose.words.mailmerging/mappeddatafieldcollection/containskey/)(*string*) | Determina si existe en la colección una asignación del campo especificado en el documento. |
| [ContainsValue](../../aspose.words.mailmerging/mappeddatafieldcollection/containsvalue/)(*string*) | Determina si existe en la colección una asignación del campo especificado en la fuente de datos. |
| [GetEnumerator](../../aspose.words.mailmerging/mappeddatafieldcollection/getenumerator/)() | Devuelve un objeto enumerador de diccionario que se puede utilizar para iterar sobre todos los elementos de la colección. |
| [Remove](../../aspose.words.mailmerging/mappeddatafieldcollection/remove/)(*string*) | Elimina una asignación de campo. |

## Observaciones

Esto se implementa como una colección de claves de cadena en valores de cadena. Las claves son los nombres de los campos de combinación de correspondencia en el documento y los valores son los nombres de los campos en su fuente de datos.

## Ejemplos

Muestra cómo asignar columnas de datos y MERGEFIELDs con diferentes nombres para que los datos se transfieran entre ellos durante una combinación de correspondencia.

```csharp
public void MappedDataFieldCollection()
{
    Document doc = CreateSourceDocMappedDataFields();
    DataTable dataTable = CreateSourceTableMappedDataFields();

    // La tabla tiene una columna llamada "Columna2", pero no hay ningún MERGEFIELD con ese nombre.
    // Además, tenemos un MERGEFIELD llamado "Column3", pero la fuente de datos no tiene una columna con ese nombre.
    // Si los datos de "Columna2" son adecuados para el CAMPO DE COMBINACIÓN "Columna3",
    //podemos asignar ese nombre de columna al MERGEFIELD en el par clave/valor "MappedDataFields".
    MappedDataFieldCollection mappedDataFields = doc.MailMerge.MappedDataFields;

    //Podemos vincular un nombre de columna de fuente de datos a un nombre MERGEFIELD de esta manera.
    mappedDataFields.Add("MergeFieldName", "DataSourceColumnName");

    // Vincula la columna de fuente de datos denominada "Columna2" a los campos MERGEFIELD denominados "Columna3".
    mappedDataFields.Add("Column3", "Column2");

    // El nombre de MERGEFIELD es la "clave" del nombre de la columna de fuente de datos respectiva "valor".
    Assert.AreEqual("DataSourceColumnName", mappedDataFields["MergeFieldName"]);
    Assert.True(mappedDataFields.ContainsKey("MergeFieldName"));
    Assert.True(mappedDataFields.ContainsValue("DataSourceColumnName"));

    // Ahora, si ejecutamos esta combinación de correspondencia, los MERGEFIELDs "Columna3" tomarán datos de la "Columna2" de la tabla.
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "MailMerge.MappedDataFieldCollection.docx");

    //Podemos iterar sobre los elementos de esta colección.
    Assert.AreEqual(2, mappedDataFields.Count);

    using (IEnumerator<KeyValuePair<string, string>> enumerator = mappedDataFields.GetEnumerator())
        while (enumerator.MoveNext())
            Console.WriteLine(
                $"Column named {enumerator.Current.Value} is mapped to MERGEFIELDs named {enumerator.Current.Key}");

    //También podemos eliminar elementos de la colección.
    mappedDataFields.Remove("MergeFieldName");

    Assert.False(mappedDataFields.ContainsKey("MergeFieldName"));
    Assert.False(mappedDataFields.ContainsValue("DataSourceColumnName"));

    mappedDataFields.Clear();

    Assert.AreEqual(0, mappedDataFields.Count);
}

/// <summary>
/// Crea un documento con 2 MERGEFIELDs, uno de los cuales no tiene un
/// columna correspondiente en la tabla de datos del método siguiente.
/// </summary>
private static Document CreateSourceDocMappedDataFields()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD Column1");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD Column3");

    return doc;
}

/// <summary>
/// Cree una tabla de datos con 2 columnas, una de las cuales no tiene una
/// MERGEFIELD correspondiente en el documento fuente del método anterior.
/// </summary>
private static DataTable CreateSourceTableMappedDataFields()
{
    DataTable dataTable = new DataTable("MyTable");
    dataTable.Columns.Add("Column1");
    dataTable.Columns.Add("Column2");
    dataTable.Rows.Add(new object[] { "Value1", "Value2" });

    return dataTable;
}
```

### Ver también

* espacio de nombres [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../)
