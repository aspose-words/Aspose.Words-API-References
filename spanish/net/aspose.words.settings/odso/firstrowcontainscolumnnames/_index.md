---
title: Odso.FirstRowContainsColumnNames
linktitle: FirstRowContainsColumnNames
articleTitle: FirstRowContainsColumnNames
second_title: Aspose.Words para .NET
description: Descubra la propiedad FirstRowContainsColumnNames de Odso, que permite a las aplicaciones reconocer la primera fila de datos como encabezados, mejorando la claridad y la facilidad de uso de los datos.
type: docs
weight: 60
url: /es/net/aspose.words.settings/odso/firstrowcontainscolumnnames/
---
## Odso.FirstRowContainsColumnNames property

Especifica que una aplicación de alojamiento debe tratar la primera fila de datos en la fuente de datos externa especificada como una fila de encabezado que contiene los nombres de cada columna en la fuente de datos. El valor predeterminado es`FALSO` .

```csharp
public bool FirstRowContainsColumnNames { get; set; }
```

## Observaciones

RK Nunca he visto esto en uso.

## Ejemplos

Muestra cómo ejecutar una combinación de correspondencia con datos de un objeto de origen de datos de Office.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");
builder.Writeln(": ");
builder.InsertField("MERGEFIELD Message", "<Message>");

// Crea una fuente de datos en forma de archivo ASCII, con el carácter "|"
// Actúa como delimitador que separa las columnas. La primera línea contiene los nombres de las tres columnas.
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

 // Al abrir este documento en Microsoft Word se ejecutará la combinación de correspondencia antes de mostrar el contenido.
doc.Save(ArtifactsDir + "MailMerge.MailMergeSettings.docx");
```

### Ver también

* class [Odso](../)
* espacio de nombres [Aspose.Words.Settings](../../../aspose.words.settings/)
* asamblea [Aspose.Words](../../../)
