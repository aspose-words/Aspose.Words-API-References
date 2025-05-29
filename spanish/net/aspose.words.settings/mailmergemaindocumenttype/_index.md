---
title: MailMergeMainDocumentType Enum
linktitle: MailMergeMainDocumentType
articleTitle: MailMergeMainDocumentType
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.MailMergeMainDocumentType, que define varios tipos de documentos fuente de combinación de correspondencia para una automatización perfecta de documentos.
type: docs
weight: 6670
url: /es/net/aspose.words.settings/mailmergemaindocumenttype/
---
## MailMergeMainDocumentType enumeration

Especifica los tipos posibles para un documento fuente de combinación de correspondencia.

```csharp
public enum MailMergeMainDocumentType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| NotAMergeDocument | `0` | Este documento no es un documento de combinación de correspondencia. |
| FormLetters | `1` | Especifica que el documento de origen de la combinación de correspondencia es del tipo carta modelo. |
| MailingLabels | `2` | Especifica que el documento de origen de la combinación de correspondencia es del tipo de etiqueta de correo. |
| Envelopes | `4` | Especifica que el documento de origen de la combinación de correspondencia es del tipo sobre. |
| Catalog | `8` | Especifica que el documento de origen de la combinación de correspondencia es del tipo catálogo. |
| Email | `16` | Especifica que el documento de origen de la combinación de correspondencia es del tipo de mensaje de correo electrónico. |
| Fax | `32` | Especifica que el documento de origen de la combinación de correspondencia es del tipo fax. |
| Default | `0` | Es igual aNotAMergeDocument |

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

* property [MainDocumentType](../mailmergesettings/maindocumenttype/)
* espacio de nombres [Aspose.Words.Settings](../../aspose.words.settings/)
* asamblea [Aspose.Words](../../)
