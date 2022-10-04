---
title: Odso
second_title: Referencia de API de Aspose.Words para .NET
description: Especifica la configuración del objeto de origen de datos de Office ODSO para un origen de datos de combinación de correspondencia.
type: docs
weight: 5580
url: /es/net/aspose.words.settings/odso/
---
## Odso class

Especifica la configuración del objeto de origen de datos de Office (ODSO) para un origen de datos de combinación de correspondencia.

```csharp
public class Odso
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [Odso](odso/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [ColumnDelimiter](../../aspose.words.settings/odso/columndelimiter/) { get; set; } | Especifica el carácter que se interpretará como el delimitador de columna utilizado para separar columnas dentro de fuentes de datos externas. El valor predeterminado es 0, lo que significa que no hay un delimitador de columna definido. |
| [DataSource](../../aspose.words.settings/odso/datasource/) { get; set; } | Especifica la ubicación de la fuente de datos externa que se conectará a un documento para realizar la combinación de correspondencia. El valor predeterminado es una cadena vacía. |
| [DataSourceType](../../aspose.words.settings/odso/datasourcetype/) { get; set; } | Especifica el tipo de origen de datos externo al que se conectará como parte de la información de conexión de ODSO para esta combinación de correspondencia. El valor predeterminado esDefault . |
| [FieldMapDatas](../../aspose.words.settings/odso/fieldmapdatas/) { get; set; } | Obtiene o establece una colección de objetos que especifican cómo se asignan las columnas del origen de datos externo a los nombres de campo de combinación predefinidos en el documento. Este objeto nunca es nulo. |
| [FirstRowContainsColumnNames](../../aspose.words.settings/odso/firstrowcontainscolumnnames/) { get; set; } | Especifica que una aplicación de hospedaje tratará la primera fila de datos en la fuente de datos externa especificada como una fila de encabezado que contiene los nombres de cada columna en la fuente de datos. El valor predeterminado es`falso` . |
| [RecipientDatas](../../aspose.words.settings/odso/recipientdatas/) { get; set; } | Obtiene o establece una colección de objetos que especifican la inclusión/exclusión de registros individuales en la combinación de correspondencia. Este objeto nunca es nulo. |
| [TableName](../../aspose.words.settings/odso/tablename/) { get; set; } | Especifica el conjunto particular de datos al que se conectará una fuente dentro de una fuente de datos externa. El valor predeterminado es una cadena vacía. |
| [UdlConnectString](../../aspose.words.settings/odso/udlconnectstring/) { get; set; } | Especifica la cadena de conexión de enlace de datos universal (UDL) utilizada para conectarse a una fuente de datos externa. El valor predeterminado es una cadena vacía. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Clone](../../aspose.words.settings/odso/clone/)() | Devuelve un clon profundo de este objeto. |

### Observaciones

ODSO parece ser la "nueva" forma en que las versiones más nuevas de Microsoft Word prefieren usar al especificar ciertos tipos de fuentes de datos para un documento de combinación de correspondencia. ODSO probablemente apareció por primera vez en Microsoft Word 2000.

El uso de ODSO está mal documentado y la mejor manera de aprender a usar las propiedades de este objeto es crear un documento con una fuente de datos deseada manualmente en Microsoft Word y luego abrir ese documento usando Aspose.Words y examinar las propiedades. del[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) y [`Odso`](../mailmergesettings/odso/) objetos. Este es un buen enfoque si desea aprender cómo configurar mediante programación una fuente de datos, por ejemplo.

Normalmente no necesita crear objetos de esta clase directamente porque ODSO settings siempre está disponible a través de la[`Odso`](../mailmergesettings/odso/) propiedad.

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

* espacio de nombres [Aspose.Words.Settings](../../aspose.words.settings/)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
