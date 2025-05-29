---
title: MailMerge.ExecuteWithRegionsADO
linktitle: ExecuteWithRegionsADO
articleTitle: ExecuteWithRegionsADO
second_title: Aspose.Words para .NET
description: Optimice la creación de documentos con el método MailMerge ExecuteWithRegionsADO. Combine fácilmente datos de conjuntos de registros ADO para obtener resultados personalizados.
type: docs
weight: 210
url: /es/net/aspose.words.mailmerging/mailmerge/executewithregionsado/
---
## MailMerge.ExecuteWithRegionsADO method

Realiza la combinación de correspondencia desde un objeto Recordset ADO en el documento con regiones de combinación de correspondencia.

```csharp
public void ExecuteWithRegionsADO(object recordset, string tableName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| recordset | Object | Conjunto de registros ADO u objeto de registro. |
| tableName | String | Nombre de la región de combinación de correspondencia en el documento que se va a rellenar. |

## Observaciones

Este método es útil cuando desea utilizar clases Aspose.Words como objetos COM desde código no administrado, como una aplicación creada con ASP o Visual Basic 6.0.

Para más información ver descripción de[`ExecuteWithRegions`](../executewithregions/).

## Ejemplos

```csharp
[VBScript]

Dim RS
Set RS = CreateObject("ADODB.Recordset")
RS.Open _
    "SELECT * FROM AsposeWordOrderDetails WHERE OrderId = 10444 ORDER BY ProductID", _
    "Provider=Microsoft.Jet.OLEDB.4.0;Data Source=Northwind.mdb"

Dim Helper
Set Helper = CreateObject("Aspose.Words.ComHelper")

Dim Doc
Set Doc = Helper.Open("Invoice.doc")

Doc.MailMerge.ExecuteWithRegionsADO RS, "OrderDetails"
Doc.Save "Invoice Out VBScript.doc"
```

Muestra cómo ejecutar una combinación de correspondencia con múltiples regiones, compilada con datos de un conjunto de datos ADO.

```csharp
public void ExecuteWithRegionsADO()
{
    Document doc = CreateSourceDocADOMailMergeWithRegions();

    // Para trabajar con conjuntos de datos ADO, necesitaremos agregar una referencia a la biblioteca de objetos de datos ActiveX de Microsoft,
    // que se incluye en la distribución .NET y se almacena en "adodb.dll".
    ADODB.Connection connection = new ADODB.Connection();

    // Crea una cadena de conexión que apunta al archivo de base de datos "Northwind"
    // en nuestro sistema de archivos local y abrir una conexión.
    string connectionString = @"Provider=Microsoft.ACE.OLEDB.12.0;Data Source=" + DatabaseDir + "Northwind.accdb";
    connection.Open(connectionString);

    // Rellene nuestro conjunto de datos ejecutando un comando SQL en nuestra base de datos.
    // Los nombres de las columnas en la tabla de resultados deberán corresponder
    // a los valores de los MERGEFIELDS que albergarán nuestros datos.
    string command = "SELECT FirstName, LastName, City FROM Employees";

    ADODB.Recordset recordset = new ADODB.Recordset();
    recordset.Open(command, connection);

    // Ejecute una combinación de correspondencia solo en la primera región, llenando sus MERGEFIELDS con datos del conjunto de registros.
    doc.MailMerge.ExecuteWithRegionsADO(recordset, "MergeRegion1");

    // Cierre el conjunto de registros y vuelva a abrirlo con datos de otra consulta SQL.
    command = "SELECT * FROM Customers";

    recordset.Close();
    recordset.Open(command, connection);

    // Ejecute una segunda combinación de correspondencia en la segunda región y guarde el documento.
    doc.MailMerge.ExecuteWithRegionsADO(recordset, "MergeRegion2");

    doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsADO.docx");

}

/// <summary>
/// Crea un documento con dos regiones de combinación de correspondencia.
/// </summary>
private static Document CreateSourceDocADOMailMergeWithRegions()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("\tEmployees: ");
    builder.InsertField(" MERGEFIELD TableStart:MergeRegion1");
    builder.InsertField(" MERGEFIELD FirstName");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD LastName");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD City");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion1");
    builder.InsertParagraph();

    builder.Writeln("\tCustomers: ");
    builder.InsertField(" MERGEFIELD TableStart:MergeRegion2");
    builder.InsertField(" MERGEFIELD ContactName");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD Address");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD City");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion2");

    return doc;
}
```

### Ver también

* class [MailMerge](../)
* espacio de nombres [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../../)
