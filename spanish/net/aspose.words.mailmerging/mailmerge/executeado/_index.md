---
title: MailMerge.ExecuteADO
linktitle: ExecuteADO
articleTitle: ExecuteADO
second_title: Aspose.Words para .NET
description: Optimice la creación de documentos con el método MailMerge ExecuteADO. Combine fácilmente datos de conjuntos de registros ADO para obtener resultados eficientes y personalizados.
type: docs
weight: 190
url: /es/net/aspose.words.mailmerging/mailmerge/executeado/
---
## MailMerge.ExecuteADO method

Realiza la fusión de correspondencia desde un objeto Recordset ADO en el documento.

```csharp
public void ExecuteADO(object recordset)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| recordset | Object | Conjunto de registros ADO u objeto de registro. |

## Observaciones

Este método es útil cuando desea utilizar clases Aspose.Words como objetos COM desde código no administrado, como una aplicación creada con ASP o Visual Basic 6.0.

Este método ignora elRemoveUnusedRegions opción.

Para más información ver descripción de[`Execute`](../execute/).

## Ejemplos

```csharp
[VBScript]

Dim RS
Set RS = CreateObject("ADODB.Recordset")
RS.Open _
    "SELECT TOP 50 * FROM Customers ORDER BY Country, CompanyName", _
    "Provider=Microsoft.Jet.OLEDB.4.0;Data Source=Northwind.mdb"

Dim License
Set License = CreateObject("Aspose.Words.License")
License.SetLicense "C:\MyPath\MyLicense.lic"

Dim Helper
Set Helper = CreateObject("Aspose.Words.ComHelper")
Dim Doc
Set Doc = Helper.Open("CustomerLabels.doc")

Doc.MailMerge.ExecuteADO RS
Doc.Save "C:\MyPath\CustomerLabels Out VBScript.doc"
```

Muestra cómo ejecutar una combinación de correspondencia con datos de un conjunto de datos ADO.

```csharp
public void ExecuteADO()
{
    Document doc = CreateSourceDocADOMailMerge();

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
    const string command = @"SELECT ProductName, QuantityPerUnit, UnitPrice FROM Products";

    ADODB.Recordset recordset = new ADODB.Recordset();
    recordset.Open(command, connection);

    // Ejecute la combinación de correspondencia y guarde el documento.
    doc.MailMerge.ExecuteADO(recordset);
    doc.Save(ArtifactsDir + "MailMerge.ExecuteADO.docx");
}

/// <summary>
/// Cree un documento en blanco y rellénelo con MERGEFIELDS que aceptarán datos cuando se ejecute una combinación de correspondencia.
/// </summary>
private static Document CreateSourceDocADOMailMerge()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Write("Product:\t");
    builder.InsertField(" MERGEFIELD ProductName");
    builder.Writeln();
    builder.InsertField(" MERGEFIELD QuantityPerUnit");
    builder.Write(" for $");
    builder.InsertField(" MERGEFIELD UnitPrice");

    return doc;
}
```

### Ver también

* class [MailMerge](../)
* espacio de nombres [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../../)
