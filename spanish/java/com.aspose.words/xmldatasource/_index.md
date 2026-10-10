---
title: "XmlDataSource"
linktitle: "XmlDataSource"
second_title: "Aspose.Words para Java"
description: "Proporciona acceso a los datos de un archivo XML o flujo para ser usado dentro de un informe en Java."
type: docs
weight: 746
url: /es/java/com.aspose.words/xmldatasource/
---

**Inheritance:**
java.lang.Object
```
public class XmlDataSource
```

Proporciona acceso a los datos de un archivo XML o flujo para ser utilizado dentro de un informe.

Para obtener más información, visite el artículo de documentación [ LINQ Reporting Engine ][LINQ Reporting Engine].

 **Remarks:** 

Para acceder a los datos del archivo o flujo correspondiente al generar un informe, pase una instancia de esta clase como origen de datos a una de las sobrecargas de [ReportingEngine](../../com.aspose.words/reportingengine/). buildReport.

En los documentos de plantilla, si un elemento XML de nivel superior contiene solo una lista de elementos del mismo tipo, una instancia de [XmlDataSource](../../com.aspose.words/xmldatasource/) debe tratarse de la misma manera que si fuera una instancia de [DataTable](../../com.aspose.words.net.system.data/datatable/). De lo contrario, una instancia de [XmlDataSource](../../com.aspose.words/xmldatasource/) debe tratarse de la misma manera que si fuera una instancia de [DataRow](../../com.aspose.words.net.system.data/datarow/). Para obtener más información, vea la referencia de sintaxis de plantillas(https://docs.aspose.com/display/wordsjava/Template+Syntax).

Cuando se pasa una Definición de Esquema XML al constructor de esta clase, los tipos de datos de los valores de los elementos y atributos XML simples se determinan según el esquema. Por lo tanto, en los documentos de plantilla, puede trabajar con valores tipados en lugar de solo cadenas.

Cuando no se pasa una Definición de Esquema XML al constructor de esta clase, los tipos de datos de los valores de los elementos y atributos XML simples se determinan automáticamente a partir de sus representaciones en cadena. Por lo tanto, en los documentos de plantilla, también puede trabajar con valores tipados en este caso. El motor es capaz de reconocer automáticamente los valores de los siguientes tipos:

 *  long
 *  double
 *  boolean
 *  java.util.Date
 *  java.lang.String

Tenga en cuenta que, para que funcione el reconocimiento automático de tipos de datos, las representaciones en cadena de los valores de los elementos y atributos XML simples deben formarse utilizando configuraciones de cultura invariantes.

Para sobrescribir el comportamiento predeterminado de la carga de datos XML, inicialice y pase una instancia de [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) a un constructor de esta clase.

 **Examples:** 

Muestra cómo usar XML como fuente de datos (cadena).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - XML data destination (Java).docx");

 XmlDataSource dataSource = new XmlDataSource(getMyDir() + "List of people.xml");
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.XmlDataString.docx");
 
```

Muestra cómo usar XML como fuente de datos (stream).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - XML data destination (Java).docx");

 InputStream stream = new FileInputStream(getMyDir() + "List of people.xml");
 try {
     XmlDataSource dataSource = new XmlDataSource(stream);
     buildReport(doc, dataSource, "persons");
 } finally {
     stream.close();
 }

 doc.save(getArtifactsDir() + "ReportingEngine.XmlDataStream.docx");
 
```


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Constructores

| Constructor | Descripción |
| --- | --- |
| [XmlDataSource(String xmlPath)](#XmlDataSource-java.lang.String) | Crea una nueva fuente de datos con datos de un archivo XML usando las opciones predeterminadas para la carga de datos XML. |
| [XmlDataSource(InputStream xmlStream)](#XmlDataSource-java.io.InputStream) | Inicializa una nueva instancia de esta clase. |
| [XmlDataSource(String xmlPath, String xmlSchemaPath)](#XmlDataSource-java.lang.String-java.lang.String) | Crea una nueva fuente de datos con datos de un archivo XML usando un archivo de Definición de Esquema XML. |
| [XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream)](#XmlDataSource-java.io.InputStream-java.io.InputStream) | Inicializa una nueva instancia de esta clase. |
| [XmlDataSource(String xmlPath, XmlDataLoadOptions options)](#XmlDataSource-java.lang.String-com.aspose.words.XmlDataLoadOptions) | Crea una nueva fuente de datos con datos de un archivo XML usando las opciones especificadas para la carga de datos XML. |
| [XmlDataSource(InputStream xmlStream, XmlDataLoadOptions options)](#XmlDataSource-java.io.InputStream-com.aspose.words.XmlDataLoadOptions) | Inicializa una nueva instancia de esta clase. |
| [XmlDataSource(String xmlPath, String xmlSchemaPath, XmlDataLoadOptions options)](#XmlDataSource-java.lang.String-java.lang.String-com.aspose.words.XmlDataLoadOptions) | Crea una nueva fuente de datos con datos de un archivo XML usando un archivo de Definición de Esquema XML. |
| [XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream, XmlDataLoadOptions options)](#XmlDataSource-java.io.InputStream-java.io.InputStream-com.aspose.words.XmlDataLoadOptions) | Inicializa una nueva instancia de esta clase. |
### XmlDataSource(String xmlPath) {#XmlDataSource-java.lang.String}
```
public XmlDataSource(String xmlPath)
```


Crea una nueva fuente de datos con datos de un archivo XML usando las opciones predeterminadas para la carga de datos XML.

 **Examples:** 

Muestra cómo usar XML como fuente de datos (cadena).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - XML data destination (Java).docx");

 XmlDataSource dataSource = new XmlDataSource(getMyDir() + "List of people.xml");
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.XmlDataString.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| xmlPath | java.lang.String | La ruta al archivo XML que se usará como fuente de datos. |

### XmlDataSource(InputStream xmlStream) {#XmlDataSource-java.io.InputStream}
```
public XmlDataSource(InputStream xmlStream)
```


Inicializa una nueva instancia de esta clase.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |

### XmlDataSource(String xmlPath, String xmlSchemaPath) {#XmlDataSource-java.lang.String-java.lang.String}
```
public XmlDataSource(String xmlPath, String xmlSchemaPath)
```


Crea una nueva fuente de datos con datos de un archivo XML usando un archivo de Definición de Esquema XML. Se usan las opciones predeterminadas para la carga de datos XML.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| xmlPath | java.lang.String | La ruta al archivo XML que se usará como fuente de datos. |
| xmlSchemaPath | java.lang.String | La ruta al archivo de Definición de Esquema XML que proporciona el esquema para el archivo XML. |

### XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream) {#XmlDataSource-java.io.InputStream-java.io.InputStream}
```
public XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream)
```


Inicializa una nueva instancia de esta clase.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |
| xmlSchemaStream | java.io.InputStream |  |

### XmlDataSource(String xmlPath, XmlDataLoadOptions options) {#XmlDataSource-java.lang.String-com.aspose.words.XmlDataLoadOptions}
```
public XmlDataSource(String xmlPath, XmlDataLoadOptions options)
```


Crea una nueva fuente de datos con datos de un archivo XML usando las opciones especificadas para la carga de datos XML.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| xmlPath | java.lang.String | La ruta al archivo XML que se usará como fuente de datos. |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) | Opciones para la carga de datos XML. |

### XmlDataSource(InputStream xmlStream, XmlDataLoadOptions options) {#XmlDataSource-java.io.InputStream-com.aspose.words.XmlDataLoadOptions}
```
public XmlDataSource(InputStream xmlStream, XmlDataLoadOptions options)
```


Inicializa una nueva instancia de esta clase.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) |  |

### XmlDataSource(String xmlPath, String xmlSchemaPath, XmlDataLoadOptions options) {#XmlDataSource-java.lang.String-java.lang.String-com.aspose.words.XmlDataLoadOptions}
```
public XmlDataSource(String xmlPath, String xmlSchemaPath, XmlDataLoadOptions options)
```


Crea una nueva fuente de datos con datos de un archivo XML usando un archivo de Definición de Esquema XML. Se usan las opciones especificadas para la carga de datos XML.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| xmlPath | java.lang.String | La ruta al archivo XML que se usará como fuente de datos. |
| xmlSchemaPath | java.lang.String | La ruta al archivo de Definición de Esquema XML que proporciona el esquema para el archivo XML. |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) | Opciones para la carga de datos XML. |

### XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream, XmlDataLoadOptions options) {#XmlDataSource-java.io.InputStream-java.io.InputStream-com.aspose.words.XmlDataLoadOptions}
```
public XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream, XmlDataLoadOptions options)
```


Inicializa una nueva instancia de esta clase.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |
| xmlSchemaStream | java.io.InputStream |  |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) |  |

