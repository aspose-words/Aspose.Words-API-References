---
title: MailMergeDataType Enum
linktitle: MailMergeDataType
articleTitle: MailMergeDataType
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.MailMergeDataType para una integración perfecta de fuentes de datos externas en sus proyectos de automatización de documentos.
type: docs
weight: 6650
url: /es/net/aspose.words.settings/mailmergedatatype/
---
## MailMergeDataType enumeration

Especifica el tipo de una fuente de datos de combinación de correspondencia externa.

```csharp
public enum MailMergeDataType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `-1` | No se especificó ninguna fuente de datos de combinación de correspondencia. |
| TextFile | `0` | Especifica que un documento determinado se ha conectado a un archivo de texto a través del sistema de intercambio dinámico de datos (DDE). |
| Database | `1` | Especifica que un documento determinado se ha conectado a una base de datos de Access a través del sistema de intercambio dinámico de datos (DDE). |
| Spreadsheet | `2` | Especifica que un documento determinado se ha conectado a una hoja de cálculo de Excel a través del sistema de intercambio dinámico de datos (DDE). |
| Query | `3` | Especifica que un documento determinado se ha conectado a una fuente de datos externa mediante una herramienta de consulta externa. |
| Odbc | `4` | Especifica que un documento determinado se ha conectado a una fuente de datos externa a través de la interfaz de Open Database Connectivity. |
| Native | `5` | Especifica que un documento determinado se ha conectado a una fuente de datos externa a través de la interfaz del objeto de origen de datos de Office (ODSO). |
| Default | `-1` | Es igual aNone . |

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

* property [DataType](../mailmergesettings/datatype/)
* espacio de nombres [Aspose.Words.Settings](../../aspose.words.settings/)
* asamblea [Aspose.Words](../../)
