---
title: "ReportBuilderOptions"
linktitle: "ReportBuilderOptions"
second_title: "Aspose.Words para Java"
description: "Representa opciones para la funcionalidad del LINQ Reporting Engine en Java."
type: docs
weight: 573
url: /es/java/com.aspose.words/reportbuilderoptions/
---

**Inheritance:**
java.lang.Object
```
public class ReportBuilderOptions
```

Representa opciones para la funcionalidad de LINQ Reporting Engine.

 **Examples:** 

Muestra cómo rellenar el documento con datos.

```

 public void buildReportData() throws Exception {
     // There is a several ways to populate document with data:
     String doc = getMyDir() + "Reporting engine template - If greedy (Java).docx";

     AsposeData obj = new AsposeData();
     {
         obj.setList(new ArrayList<>());
         {
             obj.getList().add("abc");
         }
     }

     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.1.docx", obj);
     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.2.docx", obj, options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.3.docx", SaveFormat.DOCX, obj);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.4.docx", SaveFormat.DOCX, obj, options);
 }

 public static class AsposeData {
     public ArrayList getList() {
         return mList;
     }

     ;

     public void setList(ArrayList value) {
         mList = value;
     }

     ;

     private ArrayList mList;
 }
 
```
## Constructores

| Constructor | Descripción |
| --- | --- |
| [ReportBuilderOptions()](#ReportBuilderOptions) | Inicializa una nueva instancia de esta clase. |
## Métodos

| Método | Descripción |
| --- | --- |
| [getKnownTypes()](#getKnownTypes) | Obtiene un conjunto no ordenado (p.ej. |
| [getMissingMemberMessage()](#getMissingMemberMessage) | Obtiene un valor de cadena impreso en lugar de una expresión de plantilla que representa una referencia simple a un miembro faltante de un objeto. |
| [getOptions()](#getOptions) | Obtiene un conjunto de indicadores que controlan el comportamiento de esta instancia de [ReportingEngine](../../com.aspose.words/reportingengine/) al generar un informe. |
| [setMissingMemberMessage(String value)](#setMissingMemberMessage-java.lang.String) | Establece un valor de cadena impreso en lugar de una expresión de plantilla que representa una referencia simple a un miembro faltante de un objeto. |
| [setOptions(int value)](#setOptions-int) | Establece un conjunto de indicadores que controlan el comportamiento de esta instancia de [ReportingEngine](../../com.aspose.words/reportingengine/) al generar un informe. |
### ReportBuilderOptions() {#ReportBuilderOptions}
```
public ReportBuilderOptions()
```


Inicializa una nueva instancia de esta clase.

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

**Returns:**
java.lang.String - Un valor de cadena impreso en lugar de una expresión de plantilla que representa una referencia simple a un miembro faltante de un objeto.
### getOptions() {#getOptions}
```
public int getOptions()
```


Obtiene un conjunto de indicadores que controlan el comportamiento de esta instancia de [ReportingEngine](../../com.aspose.words/reportingengine/) al generar un informe.

 **Examples:** 

Muestra cómo rellenar el documento con datos.

```

 public void buildReportData() throws Exception {
     // There is a several ways to populate document with data:
     String doc = getMyDir() + "Reporting engine template - If greedy (Java).docx";

     AsposeData obj = new AsposeData();
     {
         obj.setList(new ArrayList<>());
         {
             obj.getList().add("abc");
         }
     }

     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.1.docx", obj);
     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.2.docx", obj, options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.3.docx", SaveFormat.DOCX, obj);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.4.docx", SaveFormat.DOCX, obj, options);
 }

 public static class AsposeData {
     public ArrayList getList() {
         return mList;
     }

     ;

     public void setList(ArrayList value) {
         mList = value;
     }

     ;

     private ArrayList mList;
 }
 
```

**Returns:**
int - Un conjunto de indicadores que controlan el comportamiento de esta instancia de [ReportingEngine](../../com.aspose.words/reportingengine/) al generar un informe. El valor devuelto es una combinación bit a bit de las constantes de [ReportBuildOptions](../../com.aspose.words/reportbuildoptions/).
### setMissingMemberMessage(String value) {#setMissingMemberMessage-java.lang.String}
```
public void setMissingMemberMessage(String value)
```


Establece un valor de cadena impreso en lugar de una expresión de plantilla que representa una referencia simple a un miembro faltante de un objeto. El valor predeterminado es una cadena vacía.

 **Remarks:** 

La propiedad debe usarse junto con la opción [ReportBuildOptions.ALLOW\_MISSING\_MEMBERS](../../com.aspose.words/reportbuildoptions/\#ALLOW-MISSING-MEMBERS). De lo contrario, se lanza una excepción cuando se encuentra un miembro faltante de un objeto.

La propiedad afecta solo la impresión de una expresión de plantilla que representa una referencia simple a un miembro faltante del objeto. Por ejemplo, la impresión de un operador binario, cuyo uno de los operandos hace referencia a un miembro faltante del objeto, no se ve afectada.

El valor de esta propiedad no puede establecerse en null.

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

Muestra cómo rellenar el documento con datos.

```

 public void buildReportData() throws Exception {
     // There is a several ways to populate document with data:
     String doc = getMyDir() + "Reporting engine template - If greedy (Java).docx";

     AsposeData obj = new AsposeData();
     {
         obj.setList(new ArrayList<>());
         {
             obj.getList().add("abc");
         }
     }

     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.1.docx", obj);
     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.2.docx", obj, options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.3.docx", SaveFormat.DOCX, obj);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.4.docx", SaveFormat.DOCX, obj, options);
 }

 public static class AsposeData {
     public ArrayList getList() {
         return mList;
     }

     ;

     public void setList(ArrayList value) {
         mList = value;
     }

     ;

     private ArrayList mList;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | Un conjunto de indicadores que controlan el comportamiento de esta instancia de [ReportingEngine](../../com.aspose.words/reportingengine/) al generar un informe. El valor debe ser una combinación bit a bit de las constantes de [ReportBuildOptions](../../com.aspose.words/reportbuildoptions/). |

