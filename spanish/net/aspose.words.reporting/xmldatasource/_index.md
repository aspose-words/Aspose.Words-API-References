---
title: XmlDataSource Class
linktitle: XmlDataSource
articleTitle: XmlDataSource
second_title: Aspose.Words para .NET
description: Desbloquee informes potentes con Aspose.Words.XmlDataSource. Acceda fácilmente a datos XML para una integración perfecta en sus informes y mejore la visualización de datos.
type: docs
weight: 5490
url: /es/net/aspose.words.reporting/xmldatasource/
---
## XmlDataSource class

Proporciona acceso a los datos de un archivo o secuencia XML para ser utilizados dentro de un informe.

Para obtener más información, visite el[Motor de informes LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) Artículo de documentación.

```csharp
public class XmlDataSource
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [XmlDataSource](xmldatasource/#constructor)(*Stream*) | Crea una nueva fuente de datos con datos de un flujo XML utilizando las opciones predeterminadas para la carga de datos XML. |
| [XmlDataSource](xmldatasource/#constructor_4)(*string*) | Crea una nueva fuente de datos con datos de un archivo XML utilizando las opciones predeterminadas para la carga de datos XML. |
| [XmlDataSource](xmldatasource/#constructor_2)(*Stream, Stream*) | Crea una nueva fuente de datos con datos de un flujo XML mediante un flujo de definición de esquema XML. Las opciones predeterminadas se utilizan para la carga de datos XML. |
| [XmlDataSource](xmldatasource/#constructor_1)(*Stream, [XmlDataLoadOptions](../xmldataloadoptions/)*) | Crea una nueva fuente de datos con datos de una secuencia XML utilizando las opciones especificadas para la carga de datos XML. |
| [XmlDataSource](xmldatasource/#constructor_6)(*string, string*) | Crea una nueva fuente de datos con datos de un archivo XML mediante un archivo de definición de esquema XML. Las opciones predeterminadas se utilizan para la carga de datos XML. |
| [XmlDataSource](xmldatasource/#constructor_5)(*string, [XmlDataLoadOptions](../xmldataloadoptions/)*) | Crea una nueva fuente de datos con datos de un archivo XML utilizando las opciones especificadas para la carga de datos XML. |
| [XmlDataSource](xmldatasource/#constructor_3)(*Stream, Stream, [XmlDataLoadOptions](../xmldataloadoptions/)*) | Crea una nueva fuente de datos con datos de una secuencia XML mediante una secuencia de definición de esquema XML. Las opciones especificadas se utilizan para la carga de datos XML. |
| [XmlDataSource](xmldatasource/#constructor_7)(*string, string, [XmlDataLoadOptions](../xmldataloadoptions/)*) | Crea una nueva fuente de datos con datos de un archivo XML mediante un archivo de definición de esquema XML. Las opciones especificadas se utilizan para la carga de datos XML. |

## Observaciones

Para acceder a los datos del archivo o flujo correspondiente mientras se genera un informe, pase una instancia de esta clase como una fuente de datos a uno de[`ReportingEngine`](../reportingengine/) Sobrecargas de .BuildReport.

En los documentos de plantilla, si un elemento XML de nivel superior contiene solo una lista de elementos del mismo tipo, `XmlDataSource` La instancia debe tratarse de la misma manera que si fuera unaDataTable instancia . De lo contrario, una`XmlDataSource` La instancia debe tratarse de la misma manera que si fuera unaDataRow Instancia . Para más información, consulte la referencia de sintaxis de plantillas (https://docs.aspose.com/display/wordsnet/Template+Syntax).

Cuando se pasa la definición de esquema XML a un constructor de esta clase, los tipos de datos de los valores de elementos XML simples y atributos se determinan según el esquema. Por lo tanto, en los documentos de plantilla, se puede trabajar con valores tipificados en lugar de solo cadenas.

Cuando la definición de esquema XML no se pasa a un constructor de esta clase, los tipos de datos de los valores de elementos XML simples y atributos se determinan automáticamente a partir de sus representaciones de cadena. Por lo tanto, en los documentos de plantilla, también se puede trabajar con valores tipificados en este caso. El motor puede reconocer automáticamente valores de los siguientes tipos:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Tenga en cuenta que para que funcione el reconocimiento automático de tipos de datos, las representaciones de cadena de valores de elementos XML simples y atributos deben formarse utilizando configuraciones culturales invariables.

Para anular el comportamiento predeterminado de la carga de datos XML, inicialice y pase un[`XmlDataLoadOptions`](../xmldataloadoptions/) instancia a un constructor de esta clase.

## Ejemplos

Muestra cómo utilizar XML como fuente de datos (cadena).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

XmlDataSource dataSource = new XmlDataSource(MyDir + "List of people.xml");
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataString.docx");
```

Muestra cómo utilizar XML como fuente de datos (flujo).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

using (FileStream stream = File.OpenRead(MyDir + "List of people.xml"))
{
    XmlDataSource dataSource = new XmlDataSource(stream);
    BuildReport(doc, dataSource, "persons");
}

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataStream.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Reporting](../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../)
