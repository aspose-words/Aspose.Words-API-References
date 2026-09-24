---
title: "ReportingEngine"
linktitle: "ReportingEngine"
second_title: "Aspose.Words para Java"
description: "Proporciona rutinas para rellenar documentos de plantilla con datos y un conjunto de configuraciones para controlar estas rutinas en Java."
type: docs
weight: 574
url: /es/java/com.aspose.words/reportingengine/
---

**Inheritance:**
java.lang.Object
```
public class ReportingEngine
```

Proporciona rutinas para rellenar documentos plantilla con datos y un conjunto de configuraciones para controlar estas rutinas.

Para obtener más información, visite el artículo de documentación [ LINQ Reporting Engine ][LINQ Reporting Engine].


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Constructores

| Constructor | Descripción |
| --- | --- |
| [ReportingEngine()](#ReportingEngine) | Inicializa una nueva instancia de esta clase. |
## Métodos

| Método | Descripción |
| --- | --- |
| [buildReport(Document document, Object dataSource)](#buildReport-com.aspose.words.Document-java.lang.Object) | Rellena el documento de plantilla especificado con datos de la fuente especificada, convirtiéndolo en un informe listo. |
| [buildReport(Document document, Object dataSource, String dataSourceName)](#buildReport-com.aspose.words.Document-java.lang.Object-java.lang.String) | Rellena el documento de plantilla especificado con datos de la fuente especificada, convirtiéndolo en un informe listo. |
| [buildReport(Document document, Object[] dataSources, String[] dataSourceNames)](#buildReport-com.aspose.words.Document-java.lang.Object---java.lang.String) | Rellena el documento de plantilla especificado con datos de las fuentes especificadas, convirtiéndolo en un informe listo. |
| [equals(Object obj)](#equals-java.lang.Object) |  |
| [getKnownTypes()](#getKnownTypes) | Obtiene un conjunto no ordenado (p.ej. |
| [getMissingMemberMessage()](#getMissingMemberMessage) | Obtiene un valor de cadena impreso en lugar de una expresión de plantilla que representa una referencia simple a un miembro faltante de un objeto. |
| [getOptions()](#getOptions) | Obtiene un conjunto de indicadores que controlan el comportamiento de esta instancia de [ReportingEngine](../../com.aspose.words/reportingengine/) al generar un informe. |
| [getRestrictedTypes()](#getRestrictedTypes) | Devuelve tipos, cuyos miembros, así como los miembros de los tipos derivados, deben ser inaccesibles para el motor mediante la sintaxis de plantilla. |
| [getUseReflectionOptimization()](#getUseReflectionOptimization) | Obtiene un valor que indica si las invocaciones de miembros de tipos personalizados realizadas a través de la API de reflexión están optimizadas mediante generación dinámica de clases o no. |
| [hashCode()](#hashCode) |  |
| [setMissingMemberMessage(String value)](#setMissingMemberMessage-java.lang.String) | Establece un valor de cadena impreso en lugar de una expresión de plantilla que representa una referencia simple a un miembro faltante de un objeto. |
| [setOptions(int value)](#setOptions-int) | Establece un conjunto de indicadores que controlan el comportamiento de esta instancia de [ReportingEngine](../../com.aspose.words/reportingengine/) al generar un informe. |
| [setRestrictedTypes(Class[] types)](#setRestrictedTypes-java.lang.Class...) | Especifica tipos, cuyos miembros, así como los miembros de los tipos derivados, deben ser inaccesibles para el motor mediante la sintaxis de plantilla. |
| [setUseReflectionOptimization(boolean value)](#setUseReflectionOptimization-boolean) | Establece un valor que indica si las invocaciones de miembros de tipos personalizados realizadas a través de la API de reflexión están optimizadas mediante generación dinámica de clases o no. |
### ReportingEngine() {#ReportingEngine}
```
public ReportingEngine()
```


Inicializa una nueva instancia de esta clase.

### buildReport(Document document, Object dataSource) {#buildReport-com.aspose.words.Document-java.lang.Object}
```
public boolean buildReport(Document document, Object dataSource)
```


Rellena el documento de plantilla especificado con datos de la fuente especificada, convirtiéndolo en un informe listo.

 **Remarks:** 

Usando esta sobrecarga puedes referenciar los miembros de la fuente de datos en el documento de plantilla, pero no puedes referenciar el propio objeto de la fuente de datos. Debes usar la [buildReport(com.aspose.words.Document, java.lang.Object, java.lang.String)](../../com.aspose.words/reportingengine/\#buildReport-com.aspose.words.Document--java.lang.Object--java.lang.String) sobrecarga para lograr esto.

Un objeto de fuente de datos puede ser de uno de los siguientes tipos:

 *  [XmlDataSource](../../com.aspose.words/xmldatasource/)
 *  [JsonDataSource](../../com.aspose.words/jsondatasource/)
 *  [CsvDataSource](../../com.aspose.words/csvdatasource/)
 *  [DataSet](../../com.aspose.words.net.system.data/dataset/)
 *  [DataTable](../../com.aspose.words.net.system.data/datatable/)
 *  [DataRow](../../com.aspose.words.net.system.data/datarow/)
 *  [IDataReader](../../com.aspose.words.net.system.data/idatareader/)
 *  [IDataRecord](../../com.aspose.words.net.system.data/idatarecord/)
 *  [DataView](../../com.aspose.words.net.system.data/dataview/)
 *  [DataRowView](../../com.aspose.words.net.system.data/datarowview/)
 *  Any other arbitrary Java type

Para obtener información sobre cómo trabajar con fuentes de datos de diferentes tipos en documentos de plantilla, consulte la referencia de sintaxis de plantilla(https://docs.aspose.com/display/wordsjava/Template+Syntax).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) | Un documento de plantilla que será rellenado con datos. |
| dataSource | java.lang.Object | Un objeto de fuente de datos. |

**Returns:**
boolean - Un indicador que muestra si el análisis del documento de plantilla fue exitoso. El indicador devuelto solo tiene sentido si un valor de la propiedad [getOptions()](../../com.aspose.words/reportingengine/\#getOptions) / [setOptions(int)](../../com.aspose.words/reportingengine/\#setOptions-int) incluye la opción [ReportBuildOptions.INLINE\_ERROR\_MESSAGES](../../com.aspose.words/reportbuildoptions/\#INLINE-ERROR-MESSAGES).
### buildReport(Document document, Object dataSource, String dataSourceName) {#buildReport-com.aspose.words.Document-java.lang.Object-java.lang.String}
```
public boolean buildReport(Document document, Object dataSource, String dataSourceName)
```


Rellena el documento de plantilla especificado con datos de la fuente especificada, convirtiéndolo en un informe listo.

 **Remarks:** 

Usando esta sobrecarga puedes referenciar los miembros de la fuente de datos y el propio objeto de la fuente de datos en la plantilla. Si no vas a referenciar el propio objeto de la fuente de datos, puedes omitir  dataSourceName  pasando  null  o usar la [buildReport(com.aspose.words.Document, java.lang.Object)](../../com.aspose.words/reportingengine/\#buildReport-com.aspose.words.Document--java.lang.Object) sobrecarga.

Un objeto de fuente de datos puede ser de uno de los siguientes tipos:

 *  [XmlDataSource](../../com.aspose.words/xmldatasource/)
 *  [JsonDataSource](../../com.aspose.words/jsondatasource/)
 *  [CsvDataSource](../../com.aspose.words/csvdatasource/)
 *  [DataSet](../../com.aspose.words.net.system.data/dataset/)
 *  [DataTable](../../com.aspose.words.net.system.data/datatable/)
 *  [DataRow](../../com.aspose.words.net.system.data/datarow/)
 *  [IDataReader](../../com.aspose.words.net.system.data/idatareader/)
 *  [IDataRecord](../../com.aspose.words.net.system.data/idatarecord/)
 *  [DataView](../../com.aspose.words.net.system.data/dataview/)
 *  [DataRowView](../../com.aspose.words.net.system.data/datarowview/)
 *  Any other arbitrary Java type

Para obtener información sobre cómo trabajar con fuentes de datos de diferentes tipos en documentos de plantilla, consulte la referencia de sintaxis de plantilla(https://docs.aspose.com/display/wordsjava/Template+Syntax).

 **Examples:** 

Muestra cómo permitir miembros faltantes.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

Muestra cómo mostrar valores como texto en dólares.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("<<[ds.getValue1()]:dollarText>>\r<<[ds.getValue2()]:dollarText>>");

 NumericTestClass testData = new NumericTestBuilder().withValues(1234, 5621718.589).build();

 ReportingEngine report = new ReportingEngine();
 report.getKnownTypes().add(NumericTestClass.class);
 report.buildReport(doc, testData, "ds");

 doc.save(getArtifactsDir() + "ReportingEngine.DollarTextFormat.docx");
 
```

Muestra cómo eliminar párrafos de forma selectiva.

```

 // Template contains tags with an exclamation mark. For such tags, empty paragraphs will be removed.
 Document doc = new Document(getMyDir() + "Reporting engine template - Selective remove paragraphs.docx");

 ReportingEngine engine = new ReportingEngine();
 engine.buildReport(doc, false, "value");

 doc.save(getArtifactsDir() + "ReportingEngine.SelectiveDeletionOfParagraphs.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) | Un documento de plantilla que será rellenado con datos. |
| dataSource | java.lang.Object | Un objeto de fuente de datos. |
| dataSourceName | java.lang.String | Un nombre para referenciar el objeto de fuente de datos en la plantilla. |

**Returns:**
boolean - Un indicador que muestra si el análisis del documento de plantilla fue exitoso. El indicador devuelto solo tiene sentido si un valor de la propiedad [getOptions()](../../com.aspose.words/reportingengine/\#getOptions) / [setOptions(int)](../../com.aspose.words/reportingengine/\#setOptions-int) incluye la opción [ReportBuildOptions.INLINE\_ERROR\_MESSAGES](../../com.aspose.words/reportbuildoptions/\#INLINE-ERROR-MESSAGES).
### buildReport(Document document, Object[] dataSources, String[] dataSourceNames) {#buildReport-com.aspose.words.Document-java.lang.Object---java.lang.String}
```
public boolean buildReport(Document document, Object[] dataSources, String[] dataSourceNames)
```


Rellena el documento de plantilla especificado con datos de las fuentes especificadas, convirtiéndolo en un informe listo.

 **Remarks:** 

Usando esta sobrecarga puedes referenciar múltiples objetos de fuente de datos y sus miembros en la plantilla. El nombre de la primera fuente de datos puede omitirse (es decir, ser una cadena vacía o  null ) si vas a referenciar los miembros de la fuente de datos pero no el propio objeto de la fuente de datos. Los nombres de las demás fuentes de datos deben especificarse y ser únicos.

Si vas a usar una única fuente de datos, considera usar la [buildReport(com.aspose.words.Document, java.lang.Object)](../../com.aspose.words/reportingengine/\#buildReport-com.aspose.words.Document--java.lang.Object) y la [buildReport(com.aspose.words.Document, java.lang.Object, java.lang.String)](../../com.aspose.words/reportingengine/\#buildReport-com.aspose.words.Document--java.lang.Object--java.lang.String) sobrecargas en su lugar.

Un objeto de fuente de datos puede ser de uno de los siguientes tipos:

 *  [XmlDataSource](../../com.aspose.words/xmldatasource/)
 *  [JsonDataSource](../../com.aspose.words/jsondatasource/)
 *  [CsvDataSource](../../com.aspose.words/csvdatasource/)
 *  [DataSet](../../com.aspose.words.net.system.data/dataset/)
 *  [DataTable](../../com.aspose.words.net.system.data/datatable/)
 *  [DataRow](../../com.aspose.words.net.system.data/datarow/)
 *  [IDataReader](../../com.aspose.words.net.system.data/idatareader/)
 *  [IDataRecord](../../com.aspose.words.net.system.data/idatarecord/)
 *  [DataView](../../com.aspose.words.net.system.data/dataview/)
 *  [DataRowView](../../com.aspose.words.net.system.data/datarowview/)
 *  Any other arbitrary Java type

Para obtener información sobre cómo trabajar con fuentes de datos de diferentes tipos en documentos de plantilla, consulte la referencia de sintaxis de plantilla(https://docs.aspose.com/display/wordsjava/Template+Syntax).

 **Examples:** 

Muestra cómo mantener la numeración insertada tal como está.

```

 // By default, numbered lists from a template document are continued when their identifiers match those from a document being inserted.
 // With "-sourceNumbering" numbering should be separated and kept as is.
 Document template = DocumentHelper.createSimpleDocument("<>" + System.lineSeparator() + "<>");

 DocumentTestClass doc = new DocumentTestBuilder()
         .withDocument(new Document(getMyDir() + "List item.docx")).build();

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.REMOVE_EMPTY_PARAGRAPHS); }
 engine.buildReport(template, new Object[] { doc }, new String[] { "src" });

 template.save(getArtifactsDir() + "ReportingEngine.SourseListNumbering.docx");
 
```

Muestra cómo trabajar con gráficos de Word 2016.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Word 2016 Charts (Java).docx");

 ReportingEngine engine = new ReportingEngine();
 engine.buildReport(doc, new Object[] { Common.getShares(), Common.getShareQuotes() },
         new String[] { "shares", "quotes" });

 doc.save(getArtifactsDir() + "ReportingEngine.Word2016Charts.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) | Un documento de plantilla que será rellenado con datos. |
| dataSources | java.lang.Object[] | Una matriz de objetos de origen de datos. |
| dataSourceNames | java.lang.String[] | Una matriz de nombres para referenciar los objetos de origen de datos dentro de la plantilla. |

**Returns:**
boolean - Un indicador que muestra si el análisis del documento de plantilla fue exitoso. El indicador devuelto solo tiene sentido si un valor de la propiedad [getOptions()](../../com.aspose.words/reportingengine/\#getOptions) / [setOptions(int)](../../com.aspose.words/reportingengine/\#setOptions-int) incluye la opción [ReportBuildOptions.INLINE\_ERROR\_MESSAGES](../../com.aspose.words/reportbuildoptions/\#INLINE-ERROR-MESSAGES).
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getKnownTypes() {#getKnownTypes}
```
public KnownTypeSet getKnownTypes()
```


Obtiene un conjunto no ordenado (p.ej., una colección de elementos únicos) que contiene objetos java.lang.Class cuyos nombres totalmente o parcialmente calificados pueden usarse dentro de plantillas de informe procesadas por esta instancia del motor para invocar los miembros estáticos de los tipos correspondientes, realizar conversiones de tipo, etc.

**Returns:**
[KnownTypeSet](../../com.aspose.words/knowntypeset/) - An unordered set (i.e.
### getMissingMemberMessage() {#getMissingMemberMessage}
```
public String getMissingMemberMessage()
```


Obtiene un valor de cadena impreso en lugar de una expresión de plantilla que representa una referencia simple a un miembro faltante de un objeto. El valor predeterminado es una cadena vacía.

 **Remarks:** 

La propiedad debe usarse junto con la opción [ReportBuildOptions.ALLOW\_MISSING\_MEMBERS](../../com.aspose.words/reportbuildoptions/\#ALLOW-MISSING-MEMBERS). De lo contrario, se lanza una excepción cuando se encuentra un miembro faltante de un objeto.

La propiedad afecta solo la impresión de una expresión de plantilla que representa una referencia simple a un miembro faltante del objeto. Por ejemplo, la impresión de un operador binario, cuyo uno de los operandos hace referencia a un miembro faltante del objeto, no se ve afectada.

El valor de esta propiedad no puede establecerse en null.

 **Examples:** 

Muestra cómo permitir miembros faltantes.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

**Returns:**
java.lang.String - Un valor de cadena impreso en lugar de una expresión de plantilla que representa una referencia simple a un miembro faltante de un objeto.
### getOptions() {#getOptions}
```
public int getOptions()
```


Obtiene un conjunto de indicadores que controlan el comportamiento de esta instancia de [ReportingEngine](../../com.aspose.words/reportingengine/) al generar un informe.

 **Examples:** 

Muestra cómo permitir miembros faltantes.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

Muestra cómo establecer opciones para Reporting Engine

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Fields (Java).docx");

 // Note that enabling of the option makes the engine to update fields while building a report,
 // so there is no need to update fields separately after that.
 ReportingEngine engine = new ReportingEngine();
 engine.setOptions(ReportBuildOptions.UPDATE_FIELDS_SYNTAX_AWARE);
 engine.buildReport(doc, new String[] { "First topic", "Second topic", "Third topic" }, "topics");

 doc.save(getArtifactsDir() + "ReportingEngine.UpdateFieldsSyntaxAware.docx");
 
```

**Returns:**
int - Un conjunto de indicadores que controlan el comportamiento de esta instancia de [ReportingEngine](../../com.aspose.words/reportingengine/) al generar un informe. El valor devuelto es una combinación bit a bit de las constantes de [ReportBuildOptions](../../com.aspose.words/reportbuildoptions/).
### getRestrictedTypes() {#getRestrictedTypes}
```
public static Class[] getRestrictedTypes()
```


Devuelve tipos, cuyos miembros, así como los miembros de los tipos derivados, deben ser inaccesibles para el motor mediante la sintaxis de plantilla.

 **Remarks:** 

El arreglo devuelto contiene elementos previamente establecidos usando [setRestrictedTypes(java.lang.Class[])](../../com.aspose.words/reportingengine/\#setRestrictedTypes-java.lang.Class).

Cambiar los elementos del arreglo devuelto no tiene efecto sobre los tipos restringidos. Para cambiar los tipos restringidos, use [setRestrictedTypes(java.lang.Class[])](../../com.aspose.words/reportingengine/\#setRestrictedTypes-java.lang.Class) en su lugar.

**Returns:**
java.lang.Class[] - Tipos cuyos miembros, así como los miembros de los tipos derivados, deben ser inaccesibles para el motor mediante la sintaxis de plantilla.
### getUseReflectionOptimization() {#getUseReflectionOptimization}
```
public static boolean getUseReflectionOptimization()
```


Obtiene un valor que indica si las invocaciones de miembros de tipos personalizados realizadas a través de la API de reflexión están optimizadas mediante generación dinámica de clases o no. El valor predeterminado es  true .

 **Remarks:** 

Hay algunos escenarios en los que es preferible desactivar esta optimización. Por ejemplo, si está trabajando con pequeñas colecciones de elementos de datos todo el tiempo, entonces una sobrecarga de generación dinámica de clases puede ser más notable que una sobrecarga de llamadas directas a la API de reflexión. La opción no tiene efecto cuando se ejecuta en iOS y no se utiliza la optimización de reflexión.

**Returns:**
boolean - Un valor que indica si las invocaciones de miembros de tipos personalizados realizadas a través de la API de reflexión están optimizadas mediante generación dinámica de clases o no.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### setMissingMemberMessage(String value) {#setMissingMemberMessage-java.lang.String}
```
public void setMissingMemberMessage(String value)
```


Establece un valor de cadena impreso en lugar de una expresión de plantilla que representa una referencia simple a un miembro faltante de un objeto. El valor predeterminado es una cadena vacía.

 **Remarks:** 

La propiedad debe usarse junto con la opción [ReportBuildOptions.ALLOW\_MISSING\_MEMBERS](../../com.aspose.words/reportbuildoptions/\#ALLOW-MISSING-MEMBERS). De lo contrario, se lanza una excepción cuando se encuentra un miembro faltante de un objeto.

La propiedad afecta solo la impresión de una expresión de plantilla que representa una referencia simple a un miembro faltante del objeto. Por ejemplo, la impresión de un operador binario, cuyo uno de los operandos hace referencia a un miembro faltante del objeto, no se ve afectada.

El valor de esta propiedad no puede establecerse en null.

 **Examples:** 

Muestra cómo permitir miembros faltantes.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | Un valor de cadena impreso en lugar de una expresión de plantilla que representa una referencia simple a un miembro faltante de un objeto. |

### setOptions(int value) {#setOptions-int}
```
public void setOptions(int value)
```


Establece un conjunto de indicadores que controlan el comportamiento de esta instancia de [ReportingEngine](../../com.aspose.words/reportingengine/) al generar un informe.

 **Examples:** 

Muestra cómo permitir miembros faltantes.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

Muestra cómo establecer opciones para Reporting Engine

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Fields (Java).docx");

 // Note that enabling of the option makes the engine to update fields while building a report,
 // so there is no need to update fields separately after that.
 ReportingEngine engine = new ReportingEngine();
 engine.setOptions(ReportBuildOptions.UPDATE_FIELDS_SYNTAX_AWARE);
 engine.buildReport(doc, new String[] { "First topic", "Second topic", "Third topic" }, "topics");

 doc.save(getArtifactsDir() + "ReportingEngine.UpdateFieldsSyntaxAware.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | Un conjunto de indicadores que controlan el comportamiento de esta instancia de [ReportingEngine](../../com.aspose.words/reportingengine/) al generar un informe. El valor debe ser una combinación bit a bit de las constantes de [ReportBuildOptions](../../com.aspose.words/reportbuildoptions/). |

### setRestrictedTypes(Class[] types) {#setRestrictedTypes-java.lang.Class...}
```
public static void setRestrictedTypes(Class[] types)
```


Especifica tipos, cuyos miembros, así como los miembros de los tipos derivados, deben ser inaccesibles para el motor mediante la sintaxis de plantilla.

 **Remarks:** 

Los tipos restringidos deben establecerse antes de la primera generación de un informe. Después de que se invoque  BuildReportbuildReport , los tipos restringidos no pueden modificarse y se lanza una excepción al intentar hacerlo. El mejor lugar para establecer los tipos restringidos es al iniciar la aplicación.

Tenga en cuenta que una gran cantidad de tipos restringidos puede afectar el rendimiento, por lo que es mejor restringir solo aquellos tipos cuyo acceso a los miembros es realmente sensible.

Lanza java.lang.IllegalArgumentException en los siguientes casos:

\-  types  es nulo.

\- Uno de los elementos de  types  es  nulo .

\- Uno de los elementos de  types  representa un tipo invisible, es decir, un tipo no público o un tipo anidado público que tiene un tipo externo no público.

\- Uno de los elementos de  types  representa un tipo de matriz.

\-  types  contiene entradas duplicadas.

 **Examples:** 

Muestra cómo negar el acceso a los miembros de tipos considerados inseguros.

```

 Document doc =
         DocumentHelper.createSimpleDocument(
                 "<><<[typeVar]>>");

 // Note, that you can't set restricted types during or after building a report.
 ReportingEngine.setRestrictedTypes(Class.class);
 // We set "AllowMissingMembers" option to avoid exceptions during building a report.
 ReportingEngine engine = new ReportingEngine();
 engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
 engine.buildReport(doc, new Object());

 // We get an empty string because we can't access the GetType() method.
 Assert.assertEquals(doc.getText().trim(), "");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| types | java.lang.Class[] | Tipos a restringir. |

### setUseReflectionOptimization(boolean value) {#setUseReflectionOptimization-boolean}
```
public static void setUseReflectionOptimization(boolean value)
```


Establece un valor que indica si las invocaciones de miembros de tipos personalizados realizadas a través de la API de reflexión están optimizadas mediante generación dinámica de clases o no. El valor predeterminado es  true .

 **Remarks:** 

Hay algunos escenarios en los que es preferible desactivar esta optimización. Por ejemplo, si está trabajando con pequeñas colecciones de elementos de datos todo el tiempo, entonces una sobrecarga de generación dinámica de clases puede ser más notable que una sobrecarga de llamadas directas a la API de reflexión. La opción no tiene efecto cuando se ejecuta en iOS y no se utiliza la optimización de reflexión.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Un valor que indica si las invocaciones de miembros de tipos personalizados realizadas a través de la API de reflexión están optimizadas mediante generación dinámica de clases o no. |

