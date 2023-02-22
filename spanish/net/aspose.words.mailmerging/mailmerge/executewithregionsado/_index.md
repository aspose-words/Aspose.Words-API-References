---
title: MailMerge.ExecuteWithRegionsADO
second_title: Referencia de API de Aspose.Words para .NET
description: MailMerge método. Realiza la combinación de correspondencia desde un objeto Recordset de ADO en el documento con regiones de combinación de correspondencia.
type: docs
weight: 210
url: /es/net/aspose.words.mailmerging/mailmerge/executewithregionsado/
---
## MailMerge.ExecuteWithRegionsADO method

Realiza la combinación de correspondencia desde un objeto Recordset de ADO en el documento con regiones de combinación de correspondencia.

```csharp
public void ExecuteWithRegionsADO(object recordset, string tableName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| recordset | Object | ADO Recordset u objeto Record. |
| tableName | String | Nombre de la región de combinación de correspondencia en el documento para completar. |

### Observaciones

Este método es útil cuando pretende usar clases de Aspose.Words como objetos COM de código no administrado, como una aplicación creada usando ASP o Visual Basic 6.0.

Para obtener más información, consulte la descripción de MailMerge.ExecuteWithRegions(DataTable).

### Ejemplos

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

Muestra cómo ejecutar una combinación de correspondencia con varias regiones, compilada con datos de un conjunto de datos ADO.

```csharp
public void ExecuteWithRegionsADO()
{
    Document doc = CreateSourceDocADOMailMergeWithRegions();

    // Para trabajar con ADO DataSets, necesitaremos agregar una referencia a la biblioteca Microsoft ActiveX Data Objects,
    // que se incluye en la distribución .NET y se almacena en "adodb.dll".
    ADODB.Connection connection = new ADODB.Connection();

    // Crear una cadena de conexión que apunte al archivo de base de datos "Northwind"
    // en nuestro sistema de archivos local y abrir una conexión.
    string connectionString = @"Provider=Microsoft.Jet.OLEDB.4.0;Data Source=" + DatabaseDir + "Northwind.mdb";
    connection.Open(connectionString);

    // Complete nuestro DataSet ejecutando un comando SQL en nuestra base de datos.
    // Los nombres de las columnas en la tabla de resultados deberán corresponder
    // a los valores de los MERGEFIELDS que acomodarán nuestros datos.
    string command = "SELECT FirstName, LastName, City FROM Employees";

    ADODB.Recordset recordset = new ADODB.Recordset();
    recordset.Open(command, connection);

    // Ejecute una combinación de correspondencia solo en la primera región, completando sus MERGEFIELDS con datos del conjunto de registros.
    doc.MailMerge.ExecuteWithRegionsADO(recordset, "MergeRegion1");

    // Cierra el conjunto de registros y vuelve a abrirlo con datos de otra consulta SQL.
    command = "SELECT * FROM Customers";

    recordset.Close();
    recordset.Open(command, connection);

    // Ejecute una segunda combinación de correspondencia en la segunda región y guarde el documento.
    doc.MailMerge.ExecuteWithRegionsADO(recordset, "MergeRegion2");

    doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsADO.docx");
}

/// <summary>
/// Cree un documento con dos regiones de combinación de correspondencia.
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
* espacio de nombres [Aspose.Words.MailMerging](../../mailmerge/)
* asamblea [Aspose.Words](../../../)


