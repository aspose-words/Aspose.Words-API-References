---
title: Enum OdsoDataSourceType
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Settings.OdsoDataSourceType enumeración. Especifica el tipo de fuente de datos externa a la que conectarse como parte de la información de conexión ODSO.
type: docs
weight: 5890
url: /es/net/aspose.words.settings/odsodatasourcetype/
---
## OdsoDataSourceType enumeration

Especifica el tipo de fuente de datos externa a la que conectarse como parte de la información de conexión ODSO.

```csharp
public enum OdsoDataSourceType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Text | `0` | Especifica que un documento determinado se ha conectado a un archivo de texto. Posiblemente wdMergeSubTypeOther. |
| Database | `1` | Especifica que un documento determinado se ha conectado a una base de datos. Posiblemente wdMergeSubTypeAccess. |
| AddressBook | `2` | Especifica que un documento determinado se ha conectado a una libreta de direcciones de contactos. Posiblemente wdMergeSubTypeOAL. |
| Document1 | `3` | Especifica que un documento determinado se ha conectado a otro formato de documento compatible con la aplicación productora. Posiblemente wdMergeSubTypeOLEDBWord. |
| Document2 | `4` | Especifica que un documento determinado se ha conectado a otro formato de documento compatible con la aplicación productora. Posiblemente wdMergeSubTypeWorks. |
| Native | `5` | Especifica que un documento determinado se ha conectado a otro formato de documento nativo de la aplicación productora. Posiblemente wdMergeSubTypeOLEDBText |
| Email | `6` | Especifica que un documento determinado se ha conectado a una aplicación de correo electrónico. Posiblemente wdMergeSubTypeOutlook. |
| None | `7` | El tipo de fuente de datos externa no está especificado. Posiblemente wdMergeSubTypeWord. |
| Legacy | `8` | Especifica que un documento determinado se ha conectado a un formato de documento heredado compatible con la aplicación productora Posiblemente wdMergeSubTypeWord2000. |
| Master | `9` | Especifica que un documento determinado se ha conectado a una fuente de datos que agrega otras fuentes de datos. |
| Default | `7` | Igual aNone . |

### Observaciones

La especificación OOXML es muy vaga para esta enumeración. Supongo que podría corresponder a la enumeración WdMergeSubType http://msdn.microsoft.com/en-us/library/bb237801.aspx.

### Ejemplos

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

// Crea una fuente de datos en forma de archivo ASCII, con el "|" personaje
// actuando como delimitador que separa las columnas. La primera línea contiene los nombres de las tres columnas,
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

* espacio de nombres [Aspose.Words.Settings](../../aspose.words.settings/)
* asamblea [Aspose.Words](../../)


