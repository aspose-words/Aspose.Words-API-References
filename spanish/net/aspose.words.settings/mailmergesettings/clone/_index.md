---
title: MailMergeSettings.Clone
second_title: Referencia de API de Aspose.Words para .NET
description: MailMergeSettings método. Devuelve un clon profundo de este objeto.
type: docs
weight: 190
url: /es/net/aspose.words.settings/mailmergesettings/clone/
---
## MailMergeSettings.Clone method

Devuelve un clon profundo de este objeto.

```csharp
public MailMergeSettings Clone()
```

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

* class [MailMergeSettings](../)
* espacio de nombres [Aspose.Words.Settings](../../mailmergesettings/)
* asamblea [Aspose.Words](../../../)


