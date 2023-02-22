---
title: Document.MailMergeSettings
second_title: Referencia de API de Aspose.Words para .NET
description: Document propiedad. Obtiene o establece el objeto que contiene toda la información de combinación de correspondencia de un documento.
type: docs
weight: 250
url: /es/net/aspose.words/document/mailmergesettings/
---
## Document.MailMergeSettings property

Obtiene o establece el objeto que contiene toda la información de combinación de correspondencia de un documento.

```csharp
public MailMergeSettings MailMergeSettings { get; set; }
```

### Observaciones

Puede usar este objeto para especificar una fuente de datos de combinación de correspondencia para un documento y esta información (junto con los campos de datos disponibles) aparecerá en Microsoft Word cuando el usuario abra este documento. O puede usar este objeto para consultar la configuración de combinación de correspondencia que el usuario ha especificado en Microsoft Word para este documento.

Este objeto nunca es nulo.

### Ejemplos

Muestra cómo ejecutar una combinación de correo con datos de un objeto de origen de datos de Office.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");
builder.Writeln(": ");
builder.InsertField("MERGEFIELD Message", "<Message>");

// Crear una fuente de datos en forma de archivo ASCII, con el "|" personaje
// actuando como el delimitador que separa las columnas. La primera línea contiene los nombres de las tres columnas,
// y cada línea subsiguiente es una fila con sus respectivos valores.
string[] lines = { "FirstName|LastName|Message",
    "John|Doe|Hello! This message was created with Aspose Words mail merge." };
string dataSrcFilename = ArtifactsDir + "MailMerge.MailMergeSettings.DataSource.txt";

File.WriteAllLines(dataSrcFilename, lines);

MailMergeSettings settings = doc.MailMergeSettings;
settings.MainDocumentType = MailMergeMainDocumentType.MailingLabels;
settings.CheckErrors = MailMergeCheckErrors.Simulate;
settings.DataType = MailMergeDataType.Native;
settings.DataSource = dataSrcFilename;
settings.Query = "SELECT * FROM " + doc.MailMergeSettings.DataSource;
settings.LinkToQuery = true;
settings.ViewMergedData = true;

Assert.AreEqual(MailMergeDestination.Default, settings.Destination);
Assert.False(settings.DoNotSupressBlankLines);

Odso odso = settings.Odso;
odso.DataSource = dataSrcFilename;
odso.DataSourceType = OdsoDataSourceType.Text;
odso.ColumnDelimiter = '|';
odso.FirstRowContainsColumnNames = true;

Assert.AreNotSame(odso, odso.Clone());
Assert.AreNotSame(settings, settings.Clone());

// Al abrir este documento en Microsoft Word, se ejecutará la combinación de correspondencia antes de mostrar el contenido. 
doc.Save(ArtifactsDir + "MailMerge.MailMergeSettings.docx");
```

### Ver también

* class [MailMergeSettings](../../../aspose.words.settings/mailmergesettings/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)


