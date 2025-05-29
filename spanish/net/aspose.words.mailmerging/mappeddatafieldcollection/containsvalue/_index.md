---
title: MappedDataFieldCollection.ContainsValue
linktitle: ContainsValue
articleTitle: ContainsValue
second_title: Aspose.Words para .NET
description: Descubra si existe una asignación de campos en MappedDataFieldCollection con el método ContieneValor. ¡Mejore la eficiencia de su gestión de datos hoy mismo!
type: docs
weight: 60
url: /es/net/aspose.words.mailmerging/mappeddatafieldcollection/containsvalue/
---
## MappedDataFieldCollection.ContainsValue method

Determina si existe en la colección una asignación del campo especificado en la fuente de datos.

```csharp
public bool ContainsValue(string dataSourceFieldName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| dataSourceFieldName | String | Nombre del campo en la fuente de datos que distingue entre mayúsculas y minúsculas. |

### Valor_devuelto

`verdadero`si el artículo se encuentra en la colección; de lo contrario,`FALSO`.

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

* class [MappedDataFieldCollection](../)
* espacio de nombres [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../../)
