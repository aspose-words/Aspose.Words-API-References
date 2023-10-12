---
title: Class MailMergeSettings
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Settings.MailMergeSettings clase. Especifica toda la información de combinación de correspondencia de un documento.
type: docs
weight: 5850
url: /es/net/aspose.words.settings/mailmergesettings/
---
## MailMergeSettings class

Especifica toda la información de combinación de correspondencia de un documento.

Para obtener más información, visite el[Combinación de correspondencia e informes](https://docs.aspose.com/words/net/mail-merge-and-reporting/) artículo de documentación.

```csharp
public class MailMergeSettings
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [MailMergeSettings](mailmergesettings/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [ActiveRecord](../../aspose.words.settings/mailmergesettings/activerecord/) { get; set; } | Especifica el índice de base uno del registro de la fuente de datos que se mostrará en Microsoft Word. El valor predeterminado es 1. |
| [AddressFieldName](../../aspose.words.settings/mailmergesettings/addressfieldname/) { get; set; } | Especifica la columna dentro de la fuente de datos que contiene direcciones de correo electrónico. El valor predeterminado es una cadena vacía. |
| [CheckErrors](../../aspose.words.settings/mailmergesettings/checkerrors/) { get; set; } | Especifica el tipo de informe de errores que realizará Microsoft Word al realizar una combinación de correspondencia. El valor predeterminado esDefault . |
| [ConnectString](../../aspose.words.settings/mailmergesettings/connectstring/) { get; set; } | Especifica la cadena de conexión utilizada para conectarse a una fuente de datos externa. El valor predeterminado es una cadena vacía. |
| [DataSource](../../aspose.words.settings/mailmergesettings/datasource/) { get; set; } | Especifica la ruta al origen de datos de combinación de correspondencia. El valor predeterminado es una cadena vacía. |
| [DataType](../../aspose.words.settings/mailmergesettings/datatype/) { get; set; } | Especifica el tipo de origen de datos de combinación de correspondencia y el método de acceso a los datos. El valor predeterminado esDefault . |
| [Destination](../../aspose.words.settings/mailmergesettings/destination/) { get; set; } | Especifica cómo Microsoft Word generará los resultados de una combinación de correspondencia. El valor predeterminado esDefault . |
| [DoNotSupressBlankLines](../../aspose.words.settings/mailmergesettings/donotsupressblanklines/) { get; set; } | Especifica cómo una aplicación que realiza la combinación de correspondencia manejará las líneas en blanco en los documentos combinados resultantes de la combinación de correspondencia. El valor predeterminado es`FALSO` . |
| [HeaderSource](../../aspose.words.settings/mailmergesettings/headersource/) { get; set; } | Especifica la ruta al origen del encabezado de combinación de correspondencia. El valor predeterminado es una cadena vacía. |
| [LinkToQuery](../../aspose.words.settings/mailmergesettings/linktoquery/) { get; set; } | No estoy seguro acerca de este. La referencia de automatización de Microsoft Word sugiere que esto especifica que la consulta se ejecuta cada vez que se abre el documento en Microsoft Word. Pero la especificación OOXML sugiere que esto especifica que la consulta contiene una referencia a un archivo de consulta externo que contiene la consulta real. El valor predeterminado es`FALSO` . |
| [MailAsAttachment](../../aspose.words.settings/mailmergesettings/mailasattachment/) { get; set; } | Especifica que los documentos generados durante una operación de combinación de correspondencia deben enviarse por correo electrónico como un archivo adjunto en lugar de y no como el cuerpo del correo electrónico real. El valor predeterminado es`FALSO` . |
| [MailSubject](../../aspose.words.settings/mailmergesettings/mailsubject/) { get; set; } | Especifica el texto que aparecerá en la línea de asunto de los correos electrónicos o faxes generados durante la combinación de correspondencia. El valor predeterminado es una cadena vacía. |
| [MainDocumentType](../../aspose.words.settings/mailmergesettings/maindocumenttype/) { get; set; } | Especifica el tipo de documento principal de combinación de correspondencia. El valor predeterminado esDefault . |
| [Odso](../../aspose.words.settings/mailmergesettings/odso/) { get; set; } | Obtiene o establece el objeto que especifica la configuración del objeto de origen de datos de Office (ODSO). |
| [Query](../../aspose.words.settings/mailmergesettings/query/) { get; set; } | Contiene la cadena del lenguaje de consulta estructurado que se ejecutará en la fuente de datos externa especificada para devolver el conjunto de registros que se importarán al documento cuando se realice la operación de combinación de correspondencia. El valor predeterminado es una cadena vacía. |
| [ViewMergedData](../../aspose.words.settings/mailmergesettings/viewmergeddata/) { get; set; } | Especifica que Microsoft Word mostrará los datos de la fuente de datos externa especificada donde se han insertado los campos de combinación (por ejemplo, vista previa de los datos combinados). El valor predeterminado es`FALSO` . |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Clear](../../aspose.words.settings/mailmergesettings/clear/)() | Borra la configuración de combinación de correspondencia de tal manera que cuando se guarde el documento, no se guardará ninguna configuración de combinación de correspondencia y se convertirá en un documento normal. |
| [Clone](../../aspose.words.settings/mailmergesettings/clone/)() | Devuelve un clon profundo de este objeto. |

### Observaciones

Puede usar este objeto para especificar una fuente de datos de combinación de correspondencia para un documento y esta información (junto con los campos de datos disponibles) aparecerá en Microsoft Word cuando el usuario abra este documento. O puede usar este objeto para consultar la configuración de combinación de correspondencia que el usuario ha especificado en Microsoft Word para este documento.

Normalmente no es necesario crear objetos de esta clase directamente porque la configuración de combinación de correspondencia de un documento siempre está disponible a través del[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) propiedad.

Para detectar si este documento es un documento principal de combinación de correspondencia, verifique el valor de [`MainDocumentType`](./maindocumenttype/) propiedad.

Para eliminar la configuración de combinación de correspondencia y la información de la fuente de datos de un documento, puede utilizar el [`Clear`](./clear/) método. Aspose.Words no escribirá configuraciones de combinación de correspondencia en un documento si el[`MainDocumentType`](./maindocumenttype/) la propiedad está establecida enNotAMergeDocument o el[`DataType`](./datatype/) la propiedad está establecida enNone.

La mejor manera de aprender a usar las propiedades de este objeto es crear un documento con una fuente de datos deseada manualmente en Microsoft Word y luego abrir ese documento usando Aspose.Words y examinar las propiedades del[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) y[`Odso`](./odso/) objetos. Este es un buen enfoque si desea aprender a configurar mediante programación una fuente de datos, por ejemplo.

Aspose.Words conserva la información de combinación de correspondencia al cargar, guardar y convertir documentos entre diferentes formatos, pero no utiliza esta información cuando realiza su propia combinación de correspondencia usando el[`MailMerge`](../../aspose.words.mailmerging/mailmerge/) objeto.

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


