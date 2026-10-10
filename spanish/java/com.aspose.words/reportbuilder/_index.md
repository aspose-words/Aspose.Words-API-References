---
title: "ReportBuilder"
linktitle: "ReportBuilder"
second_title: "Aspose.Words para Java"
description: "Proporciona métodos destinados a rellenar la plantilla con datos usando LINQ Reporting Engine en Java."
type: docs
weight: 571
url: /es/java/com.aspose.words/reportbuilder/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class ReportBuilder extends Processor
```

Proporciona métodos destinados a rellenar la plantilla con datos usando LINQ Reporting Engine.
## Métodos

| Método | Descripción |
| --- | --- |
| [buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data)](#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object) |  |
| [buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object-com.aspose.words.ReportBuilderOptions) |  |
| [buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, String dataSourceName)](#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object-java.lang.String) |  |
| [buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions) |  |
| [buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object[] data, String[] dataSourceNames)](#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object---java.lang.String) |  |
| [buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions) |  |
| [buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data)](#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object) |  |
| [buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object-com.aspose.words.ReportBuilderOptions) |  |
| [buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, String dataSourceName)](#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object-java.lang.String) |  |
| [buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions) |  |
| [buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object[] data, String[] dataSourceNames)](#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object---java.lang.String) |  |
| [buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions) |  |
| [buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data)](#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object) | Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con el formato de salida especificado y opciones adicionales. |
| [buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object-com.aspose.words.ReportBuilderOptions) | Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con el formato de salida especificado y opciones adicionales. |
| [buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, String dataSourceName)](#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object-java.lang.String) | Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con el formato de salida especificado, una referencia de fuente de datos con nombre y opciones adicionales. |
| [buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions) | Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con el formato de salida especificado, una referencia de fuente de datos con nombre y opciones adicionales. |
| [buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object[] data, String[] dataSourceNames)](#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object---java.lang.String) | Rellena el documento de plantilla con datos de múltiples fuentes, generando un informe completo con un formato de salida especificado y opciones adicionales. |
| [buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions) | Rellena el documento de plantilla con datos de múltiples fuentes, generando un informe completo con un formato de salida especificado y opciones adicionales. |
| [buildReport(String inputFileName, String outputFileName, int saveFormat, Object data)](#buildReport-java.lang.String-java.lang.String-int-java.lang.Object) |  |
| [buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-int-java.lang.Object-com.aspose.words.ReportBuilderOptions) |  |
| [buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, String dataSourceName)](#buildReport-java.lang.String-java.lang.String-int-java.lang.Object-java.lang.String) |  |
| [buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-int-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions) |  |
| [buildReport(String inputFileName, String outputFileName, int saveFormat, Object[] data, String[] dataSourceNames)](#buildReport-java.lang.String-java.lang.String-int-java.lang.Object---java.lang.String) |  |
| [buildReport(String inputFileName, String outputFileName, int saveFormat, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-int-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions) |  |
| [buildReport(String inputFileName, String outputFileName, Object data)](#buildReport-java.lang.String-java.lang.String-java.lang.Object) | Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con opciones adicionales. |
| [buildReport(String inputFileName, String outputFileName, Object data, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-java.lang.Object-com.aspose.words.ReportBuilderOptions) | Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con opciones adicionales. |
| [buildReport(String inputFileName, String outputFileName, Object data, String dataSourceName)](#buildReport-java.lang.String-java.lang.String-java.lang.Object-java.lang.String) | Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con una referencia de fuente de datos con nombre y opciones adicionales. |
| [buildReport(String inputFileName, String outputFileName, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions) | Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con una referencia de fuente de datos con nombre y opciones adicionales. |
| [buildReport(String inputFileName, String outputFileName, Object[] data, String[] dataSourceNames)](#buildReport-java.lang.String-java.lang.String-java.lang.Object---java.lang.String) | Rellena el documento de plantilla con datos de múltiples fuentes, generando un informe completo con opciones adicionales. |
| [buildReport(String inputFileName, String outputFileName, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions) | Rellena el documento de plantilla con datos de múltiples fuentes, generando un informe completo con opciones adicionales. |
| [buildReportToImages(InputStream inputStream, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames)](#buildReportToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.Object---java.lang.String) | Rellena el documento de plantilla con datos de múltiples fuentes. |
| [buildReportToImages(InputStream inputStream, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)](#buildReportToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions) | Rellena el documento de plantilla con datos de múltiples fuentes. |
| [buildReportToImages(String inputFileName, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames)](#buildReportToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.Object---java.lang.String) | Rellena el documento de plantilla con datos de múltiples fuentes. |
| [buildReportToImages(String inputFileName, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)](#buildReportToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions) | Rellena el documento de plantilla con datos de múltiples fuentes. |
| [create()](#create) | Crea una nueva instancia del procesador de creación de informes. |
| [create(ReportBuilderContext context)](#create-com.aspose.words.ReportBuilderContext) | Crea una nueva instancia del procesador de creación de informes. |
| [execute()](#execute) | Ejecuta la acción del procesador. |
| [from(InputStream input)](#from-java.io.InputStream) | Especifica el documento de entrada para el procesamiento. |
| [from(InputStream input, LoadOptions loadOptions)](#from-java.io.InputStream-com.aspose.words.LoadOptions) | Especifica el documento de entrada para el procesamiento. |
| [from(String input)](#from-java.lang.String) | Especifica el documento de entrada para el procesamiento. |
| [from(String input, LoadOptions loadOptions)](#from-java.lang.String-com.aspose.words.LoadOptions) | Especifica el documento de entrada para el procesamiento. |
| [to(OutputStream output, SaveOptions saveOptions)](#to-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [to(OutputStream output, int saveFormat)](#to-java.io.OutputStream-int) |  |
| [to(String output)](#to-java.lang.String) | Especifica el archivo de salida para el procesador. |
| [to(String output, SaveOptions saveOptions)](#to-java.lang.String-com.aspose.words.SaveOptions) | Especifica el archivo de salida para el procesador. |
| [to(String output, int saveFormat)](#to-java.lang.String-int) |  |
| [to(ArrayList output, SaveOptions saveOptions)](#to-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [to(ArrayList output, int saveFormat)](#to-java.util.ArrayList-int) |  |
| [toOutput(ArrayList output, SaveOptions saveOptions)](#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [toOutput(ArrayList output, int saveFormat)](#toOutput-java.util.ArrayList-int) |  |
### buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data) {#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| datos | java.lang.Object |  |

### buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| datos | java.lang.Object |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, String dataSourceName) {#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object-java.lang.String}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, String dataSourceName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| datos | java.lang.Object |  |
| dataSourceName | java.lang.String |  |

### buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| datos | java.lang.Object |  |
| dataSourceName | java.lang.String |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object[] data, String[] dataSourceNames) {#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object---java.lang.String}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object[] data, String[] dataSourceNames)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| datos | java.lang.Object[] |  |
| dataSourceNames | java.lang.String[] |  |

### buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| datos | java.lang.Object[] |  |
| dataSourceNames | java.lang.String[] |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data) {#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| datos | java.lang.Object |  |

### buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| datos | java.lang.Object |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, String dataSourceName) {#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object-java.lang.String}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, String dataSourceName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| datos | java.lang.Object |  |
| dataSourceName | java.lang.String |  |

### buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| datos | java.lang.Object |  |
| dataSourceName | java.lang.String |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object[] data, String[] dataSourceNames) {#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object---java.lang.String}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object[] data, String[] dataSourceNames)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| datos | java.lang.Object[] |  |
| dataSourceNames | java.lang.String[] |  |

### buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| datos | java.lang.Object[] |  |
| dataSourceNames | java.lang.String[] |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data) {#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object}
```
public static void buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data)
```


Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con el formato de salida especificado y opciones adicionales.

 **Remarks:** 

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar nombres de archivo para cada parte siguiendo la regla: outputFile\_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | java.lang.String | El nombre del archivo de entrada. |
| outputFileName | java.lang.String | El nombre del archivo de salida. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Las opciones de guardado de la salida. |
| datos | java.lang.Object | Un objeto de fuente de datos. |

### buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, ReportBuilderOptions reportBuilderOptions)
```


Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con el formato de salida especificado y opciones adicionales.

 **Remarks:** 

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar nombres de archivo para cada parte siguiendo la regla: outputFile\_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | java.lang.String | El nombre del archivo de entrada. |
| outputFileName | java.lang.String | El nombre del archivo de salida. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Las opciones de guardado de la salida. |
| datos | java.lang.Object | Un objeto de fuente de datos. |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | Opciones adicionales de generación de informes. |

### buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, String dataSourceName) {#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object-java.lang.String}
```
public static void buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, String dataSourceName)
```


Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con el formato de salida especificado, una referencia de fuente de datos con nombre y opciones adicionales.

 **Remarks:** 

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar nombres de archivo para cada parte siguiendo la regla: outputFile\_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | java.lang.String | El nombre del archivo de entrada. |
| outputFileName | java.lang.String | El nombre del archivo de salida. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Las opciones de guardado de la salida. |
| datos | java.lang.Object | Un objeto de fuente de datos. |
| dataSourceName | java.lang.String | Un nombre para referenciar el objeto de fuente de datos en la plantilla. |

### buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)
```


Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con el formato de salida especificado, una referencia de fuente de datos con nombre y opciones adicionales.

 **Remarks:** 

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar nombres de archivo para cada parte siguiendo la regla: outputFile\_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | java.lang.String | El nombre del archivo de entrada. |
| outputFileName | java.lang.String | El nombre del archivo de salida. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Las opciones de guardado de la salida. |
| datos | java.lang.Object | Un objeto de fuente de datos. |
| dataSourceName | java.lang.String | Un nombre para referenciar el objeto de fuente de datos en la plantilla. |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | Opciones adicionales de generación de informes. |

### buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object[] data, String[] dataSourceNames) {#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object---java.lang.String}
```
public static void buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object[] data, String[] dataSourceNames)
```


Rellena el documento de plantilla con datos de múltiples fuentes, generando un informe completo con un formato de salida especificado y opciones adicionales.

 **Remarks:** 

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar nombres de archivo para cada parte siguiendo la regla: outputFile\_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | java.lang.String | El nombre del archivo de entrada. |
| outputFileName | java.lang.String | El nombre del archivo de salida. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Las opciones de guardado de la salida. |
| datos | java.lang.Object[] | Una matriz de objetos de origen de datos. |
| dataSourceNames | java.lang.String[] | Una matriz de nombres para referenciar los objetos de origen de datos dentro de la plantilla. |

### buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)
```


Rellena el documento de plantilla con datos de múltiples fuentes, generando un informe completo con un formato de salida especificado y opciones adicionales.

 **Remarks:** 

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar nombres de archivo para cada parte siguiendo la regla: outputFile\_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | java.lang.String | El nombre del archivo de entrada. |
| outputFileName | java.lang.String | El nombre del archivo de salida. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Las opciones de guardado de la salida. |
| datos | java.lang.Object[] | Una matriz de objetos de origen de datos. |
| dataSourceNames | java.lang.String[] | Una matriz de nombres para referenciar los objetos de origen de datos dentro de la plantilla. |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | Opciones adicionales de generación de informes. |

### buildReport(String inputFileName, String outputFileName, int saveFormat, Object data) {#buildReport-java.lang.String-java.lang.String-int-java.lang.Object}
```
public static void buildReport(String inputFileName, String outputFileName, int saveFormat, Object data)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| datos | java.lang.Object |  |

### buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-int-java.lang.Object-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| datos | java.lang.Object |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, String dataSourceName) {#buildReport-java.lang.String-java.lang.String-int-java.lang.Object-java.lang.String}
```
public static void buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, String dataSourceName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| datos | java.lang.Object |  |
| dataSourceName | java.lang.String |  |

### buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-int-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| datos | java.lang.Object |  |
| dataSourceName | java.lang.String |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(String inputFileName, String outputFileName, int saveFormat, Object[] data, String[] dataSourceNames) {#buildReport-java.lang.String-java.lang.String-int-java.lang.Object---java.lang.String}
```
public static void buildReport(String inputFileName, String outputFileName, int saveFormat, Object[] data, String[] dataSourceNames)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| datos | java.lang.Object[] |  |
| dataSourceNames | java.lang.String[] |  |

### buildReport(String inputFileName, String outputFileName, int saveFormat, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-int-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, int saveFormat, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| datos | java.lang.Object[] |  |
| dataSourceNames | java.lang.String[] |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(String inputFileName, String outputFileName, Object data) {#buildReport-java.lang.String-java.lang.String-java.lang.Object}
```
public static void buildReport(String inputFileName, String outputFileName, Object data)
```


Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con opciones adicionales.

 **Remarks:** 

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar nombres de archivo para cada parte siguiendo la regla: outputFile\_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | java.lang.String | El nombre del archivo de entrada. |
| outputFileName | java.lang.String | El nombre del archivo de salida. |
| datos | java.lang.Object | Un objeto de fuente de datos. |

### buildReport(String inputFileName, String outputFileName, Object data, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-java.lang.Object-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, Object data, ReportBuilderOptions reportBuilderOptions)
```


Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con opciones adicionales.

 **Remarks:** 

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar nombres de archivo para cada parte siguiendo la regla: outputFile\_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

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
| inputFileName | java.lang.String | El nombre del archivo de entrada. |
| outputFileName | java.lang.String | El nombre del archivo de salida. |
| datos | java.lang.Object | Un objeto de fuente de datos. |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | Opciones adicionales de generación de informes. |

### buildReport(String inputFileName, String outputFileName, Object data, String dataSourceName) {#buildReport-java.lang.String-java.lang.String-java.lang.Object-java.lang.String}
```
public static void buildReport(String inputFileName, String outputFileName, Object data, String dataSourceName)
```


Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con una referencia de fuente de datos con nombre y opciones adicionales.

 **Remarks:** 

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar nombres de archivo para cada parte siguiendo la regla: outputFile\_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | java.lang.String | El nombre del archivo de entrada. |
| outputFileName | java.lang.String | El nombre del archivo de salida. |
| datos | java.lang.Object | Un objeto de fuente de datos. |
| dataSourceName | java.lang.String | Un nombre para referenciar el objeto de fuente de datos en la plantilla. |

### buildReport(String inputFileName, String outputFileName, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)
```


Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con una referencia de fuente de datos con nombre y opciones adicionales.

 **Remarks:** 

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar nombres de archivo para cada parte siguiendo la regla: outputFile\_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

 **Examples:** 

Muestra cómo rellenar el documento con fuentes de datos.

```

 public void buildReportDataSource() throws Exception {
     // There is a several ways to populate document with data sources:
     String doc = getMyDir() + "Report building.docx";

     MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);

     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.1.docx", sender, "s");
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.2.docx", new Object[]{sender}, new String[]{"s"});
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.3.docx", sender, "s", options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.4.docx", SaveFormat.DOCX, sender, "s");
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.5.docx", SaveFormat.DOCX, new Object[]{sender}, new String[]{"s"});
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.6.docx", SaveFormat.DOCX, sender, "s", options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.7.docx", SaveFormat.DOCX, new Object[]{sender}, new String[]{"s"}, options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.8.docx", new Object[]{sender}, new String[]{"s"}, options);

     options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     OutputStream[] images = ReportBuilder.buildReportToImages(doc, new ImageSaveOptions(SaveFormat.PNG), new Object[]{sender}, new String[]{"s"}, options);

     ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
     reportBuilderContext.getReportBuilderOptions().setMissingMemberMessage("Missed members");
     reportBuilderContext.getDataSources().put(sender, "s");

     ReportBuilder.create(reportBuilderContext)
             .from(doc)
             .to(getArtifactsDir() + "LowCode.BuildReportDataSource.9.docx")
             .execute();
 }

 public static class MessageTestClass {
     public String getName() {
         return mName;
     }

     public void setName(String value) {
         mName = value;
     }

     private String mName;

     public String getMessage() {
         return mMessage;
     }

     public void setMessage(String value) {
         mMessage = value;
     }

     private String mMessage;

     public MessageTestClass(String name, String message) {
         setName(name);
         setMessage(message);
     }
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | java.lang.String | El nombre del archivo de entrada. |
| outputFileName | java.lang.String | El nombre del archivo de salida. |
| datos | java.lang.Object | Un objeto de fuente de datos. |
| dataSourceName | java.lang.String | Un nombre para referenciar el objeto de fuente de datos en la plantilla. |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | Opciones adicionales de generación de informes. |

### buildReport(String inputFileName, String outputFileName, Object[] data, String[] dataSourceNames) {#buildReport-java.lang.String-java.lang.String-java.lang.Object---java.lang.String}
```
public static void buildReport(String inputFileName, String outputFileName, Object[] data, String[] dataSourceNames)
```


Rellena el documento de plantilla con datos de múltiples fuentes, generando un informe completo con opciones adicionales. Esta sobrecarga determina automáticamente el formato de guardado en función de la extensión del archivo de salida.

 **Remarks:** 

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar nombres de archivo para cada parte siguiendo la regla: outputFile\_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | java.lang.String | El nombre del archivo de entrada. |
| outputFileName | java.lang.String | El nombre del archivo de salida. |
| datos | java.lang.Object[] | Una matriz de objetos de origen de datos. |
| dataSourceNames | java.lang.String[] | Una matriz de nombres para referenciar los objetos de origen de datos dentro de la plantilla. |

### buildReport(String inputFileName, String outputFileName, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)
```


Rellena el documento de plantilla con datos de múltiples fuentes, generando un informe completo con opciones adicionales. Esta sobrecarga determina automáticamente el formato de guardado en función de la extensión del archivo de salida.

 **Remarks:** 

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar nombres de archivo para cada parte siguiendo la regla: outputFile\_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

 **Examples:** 

Muestra cómo rellenar el documento con fuentes de datos.

```

 public void buildReportDataSource() throws Exception {
     // There is a several ways to populate document with data sources:
     String doc = getMyDir() + "Report building.docx";

     MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);

     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.1.docx", sender, "s");
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.2.docx", new Object[]{sender}, new String[]{"s"});
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.3.docx", sender, "s", options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.4.docx", SaveFormat.DOCX, sender, "s");
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.5.docx", SaveFormat.DOCX, new Object[]{sender}, new String[]{"s"});
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.6.docx", SaveFormat.DOCX, sender, "s", options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.7.docx", SaveFormat.DOCX, new Object[]{sender}, new String[]{"s"}, options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.8.docx", new Object[]{sender}, new String[]{"s"}, options);

     options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     OutputStream[] images = ReportBuilder.buildReportToImages(doc, new ImageSaveOptions(SaveFormat.PNG), new Object[]{sender}, new String[]{"s"}, options);

     ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
     reportBuilderContext.getReportBuilderOptions().setMissingMemberMessage("Missed members");
     reportBuilderContext.getDataSources().put(sender, "s");

     ReportBuilder.create(reportBuilderContext)
             .from(doc)
             .to(getArtifactsDir() + "LowCode.BuildReportDataSource.9.docx")
             .execute();
 }

 public static class MessageTestClass {
     public String getName() {
         return mName;
     }

     public void setName(String value) {
         mName = value;
     }

     private String mName;

     public String getMessage() {
         return mMessage;
     }

     public void setMessage(String value) {
         mMessage = value;
     }

     private String mMessage;

     public MessageTestClass(String name, String message) {
         setName(name);
         setMessage(message);
     }
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | java.lang.String | El nombre del archivo de entrada. |
| outputFileName | java.lang.String | El nombre del archivo de salida. |
| datos | java.lang.Object[] | Una matriz de objetos de origen de datos. |
| dataSourceNames | java.lang.String[] | Una matriz de nombres para referenciar los objetos de origen de datos dentro de la plantilla. |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | Opciones adicionales de generación de informes. |

### buildReportToImages(InputStream inputStream, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames) {#buildReportToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.Object---java.lang.String}
```
public static OutputStream[] buildReportToImages(InputStream inputStream, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames)
```


Rellena el documento de plantilla con datos de múltiples fuentes. Renderiza la salida a imágenes.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | java.io.InputStream | El flujo de archivo de entrada. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Las opciones de guardado de la salida. |
| datos | java.lang.Object[] | Una matriz de objetos de origen de datos. |
| dataSourceNames | java.lang.String[] | Una matriz de nombres para referenciar los objetos de origen de datos dentro de la plantilla. |

**Returns:**
java.io.OutputStream[]
### buildReportToImages(InputStream inputStream, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions) {#buildReportToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions}
```
public static OutputStream[] buildReportToImages(InputStream inputStream, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)
```


Rellena el documento de plantilla con datos de múltiples fuentes. Renderiza la salida a imágenes.

 **Examples:** 

Muestra cómo rellenar el documento con fuentes de datos usando documentos del flujo.

```

 // There is a several ways to populate document with data sources using documents from the stream:
 MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Report building.docx")) {
     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.BuildReportDataSourceStream.1.docx")) {
         ReportBuilder.buildReport(streamIn, streamOut, SaveFormat.DOCX, new Object[]{sender}, new String[]{"s"});
     }

     try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.BuildReportDataSourceStream.2.docx")) {
         ReportBuilder.buildReport(streamIn, streamOut1, SaveFormat.DOCX, sender, "s");
     }

     try (FileOutputStream streamOut2 = new FileOutputStream(getArtifactsDir() + "LowCode.BuildReportDataSourceStream.3.docx")) {
         ReportBuilderOptions options = new ReportBuilderOptions();
         options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
         ReportBuilder.buildReport(streamIn, streamOut2, SaveFormat.DOCX, sender, "s", options);
     }

     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     OutputStream[] images = ReportBuilder.buildReportToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), new Object[]{sender}, new String[]{"s"}, options);

     ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
     reportBuilderContext.getReportBuilderOptions().setMissingMemberMessage("Missed members");
     reportBuilderContext.getDataSources().put(sender, "s");

     try (FileOutputStream streamOut3 = new FileOutputStream(getArtifactsDir() + "LowCode.BuildReportDataSourceStream.4.docx")) {
         ReportBuilder.create(reportBuilderContext)
                 .from(streamIn)
                 .to(streamOut3, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | java.io.InputStream | El flujo de archivo de entrada. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Las opciones de guardado de la salida. |
| datos | java.lang.Object[] | Una matriz de objetos de origen de datos. |
| dataSourceNames | java.lang.String[] | Una matriz de nombres para referenciar los objetos de origen de datos dentro de la plantilla. |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | Opciones adicionales de generación de informes. |

**Returns:**
java.io.OutputStream[]
### buildReportToImages(String inputFileName, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames) {#buildReportToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.Object---java.lang.String}
```
public static OutputStream[] buildReportToImages(String inputFileName, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames)
```


Rellena el documento de plantilla con datos de múltiples fuentes. Renderiza la salida a imágenes.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | java.lang.String | El nombre del archivo de entrada. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Las opciones de guardado de la salida. |
| datos | java.lang.Object[] | Una matriz de objetos de origen de datos. |
| dataSourceNames | java.lang.String[] | Una matriz de nombres para referenciar los objetos de origen de datos dentro de la plantilla. |

**Returns:**
java.io.OutputStream[]
### buildReportToImages(String inputFileName, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions) {#buildReportToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions}
```
public static OutputStream[] buildReportToImages(String inputFileName, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)
```


Rellena el documento de plantilla con datos de múltiples fuentes. Renderiza la salida a imágenes.

 **Examples:** 

Muestra cómo rellenar el documento con fuentes de datos.

```

 public void buildReportDataSource() throws Exception {
     // There is a several ways to populate document with data sources:
     String doc = getMyDir() + "Report building.docx";

     MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);

     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.1.docx", sender, "s");
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.2.docx", new Object[]{sender}, new String[]{"s"});
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.3.docx", sender, "s", options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.4.docx", SaveFormat.DOCX, sender, "s");
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.5.docx", SaveFormat.DOCX, new Object[]{sender}, new String[]{"s"});
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.6.docx", SaveFormat.DOCX, sender, "s", options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.7.docx", SaveFormat.DOCX, new Object[]{sender}, new String[]{"s"}, options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.8.docx", new Object[]{sender}, new String[]{"s"}, options);

     options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     OutputStream[] images = ReportBuilder.buildReportToImages(doc, new ImageSaveOptions(SaveFormat.PNG), new Object[]{sender}, new String[]{"s"}, options);

     ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
     reportBuilderContext.getReportBuilderOptions().setMissingMemberMessage("Missed members");
     reportBuilderContext.getDataSources().put(sender, "s");

     ReportBuilder.create(reportBuilderContext)
             .from(doc)
             .to(getArtifactsDir() + "LowCode.BuildReportDataSource.9.docx")
             .execute();
 }

 public static class MessageTestClass {
     public String getName() {
         return mName;
     }

     public void setName(String value) {
         mName = value;
     }

     private String mName;

     public String getMessage() {
         return mMessage;
     }

     public void setMessage(String value) {
         mMessage = value;
     }

     private String mMessage;

     public MessageTestClass(String name, String message) {
         setName(name);
         setMessage(message);
     }
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | java.lang.String | El nombre del archivo de entrada. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Las opciones de guardado de la salida. |
| datos | java.lang.Object[] | Una matriz de objetos de origen de datos. |
| dataSourceNames | java.lang.String[] | Una matriz de nombres para referenciar los objetos de origen de datos dentro de la plantilla. |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | Opciones adicionales de generación de informes. |

**Returns:**
java.io.OutputStream[]
### create() {#create}
```
public static ReportBuilder create()
```


Crea una nueva instancia del procesador de creación de informes.

**Returns:**
[ReportBuilder](../../com.aspose.words/reportbuilder/)
### create(ReportBuilderContext context) {#create-com.aspose.words.ReportBuilderContext}
```
public static ReportBuilder create(ReportBuilderContext context)
```


Crea una nueva instancia del procesador de creación de informes.

 **Examples:** 

Muestra cómo rellenar el documento con fuentes de datos.

```

 public void buildReportDataSource() throws Exception {
     // There is a several ways to populate document with data sources:
     String doc = getMyDir() + "Report building.docx";

     MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);

     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.1.docx", sender, "s");
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.2.docx", new Object[]{sender}, new String[]{"s"});
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.3.docx", sender, "s", options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.4.docx", SaveFormat.DOCX, sender, "s");
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.5.docx", SaveFormat.DOCX, new Object[]{sender}, new String[]{"s"});
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.6.docx", SaveFormat.DOCX, sender, "s", options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.7.docx", SaveFormat.DOCX, new Object[]{sender}, new String[]{"s"}, options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.8.docx", new Object[]{sender}, new String[]{"s"}, options);

     options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     OutputStream[] images = ReportBuilder.buildReportToImages(doc, new ImageSaveOptions(SaveFormat.PNG), new Object[]{sender}, new String[]{"s"}, options);

     ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
     reportBuilderContext.getReportBuilderOptions().setMissingMemberMessage("Missed members");
     reportBuilderContext.getDataSources().put(sender, "s");

     ReportBuilder.create(reportBuilderContext)
             .from(doc)
             .to(getArtifactsDir() + "LowCode.BuildReportDataSource.9.docx")
             .execute();
 }

 public static class MessageTestClass {
     public String getName() {
         return mName;
     }

     public void setName(String value) {
         mName = value;
     }

     private String mName;

     public String getMessage() {
         return mMessage;
     }

     public void setMessage(String value) {
         mMessage = value;
     }

     private String mMessage;

     public MessageTestClass(String name, String message) {
         setName(name);
         setMessage(message);
     }
 }
 
```

Muestra cómo rellenar el documento con fuentes de datos usando documentos del flujo.

```

 // There is a several ways to populate document with data sources using documents from the stream:
 MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Report building.docx")) {
     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.BuildReportDataSourceStream.1.docx")) {
         ReportBuilder.buildReport(streamIn, streamOut, SaveFormat.DOCX, new Object[]{sender}, new String[]{"s"});
     }

     try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.BuildReportDataSourceStream.2.docx")) {
         ReportBuilder.buildReport(streamIn, streamOut1, SaveFormat.DOCX, sender, "s");
     }

     try (FileOutputStream streamOut2 = new FileOutputStream(getArtifactsDir() + "LowCode.BuildReportDataSourceStream.3.docx")) {
         ReportBuilderOptions options = new ReportBuilderOptions();
         options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
         ReportBuilder.buildReport(streamIn, streamOut2, SaveFormat.DOCX, sender, "s", options);
     }

     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     OutputStream[] images = ReportBuilder.buildReportToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), new Object[]{sender}, new String[]{"s"}, options);

     ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
     reportBuilderContext.getReportBuilderOptions().setMissingMemberMessage("Missed members");
     reportBuilderContext.getDataSources().put(sender, "s");

     try (FileOutputStream streamOut3 = new FileOutputStream(getArtifactsDir() + "LowCode.BuildReportDataSourceStream.4.docx")) {
         ReportBuilder.create(reportBuilderContext)
                 .from(streamIn)
                 .to(streamOut3, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| context | [ReportBuilderContext](../../com.aspose.words/reportbuildercontext/) |  |

**Returns:**
[ReportBuilder](../../com.aspose.words/reportbuilder/)
### execute() {#execute}
```
public void execute()
```


Ejecuta la acción del procesador.

 **Examples:** 

Muestra cómo combinar documentos en un único documento de salida usando el contexto.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.1.docx")
         .execute();

 LoadOptions firstLoadOptions = new LoadOptions();
 {
     firstLoadOptions.setIgnoreOleData(true);
 }
 LoadOptions secondLoadOptions = new LoadOptions();
 {
     secondLoadOptions.setIgnoreOleData(false);
 }
 Merger.create(mergerContext)
         .from(inputDoc1, firstLoadOptions)
         .from(inputDoc2, secondLoadOptions)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.2.docx", SaveFormat.DOCX)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.3.docx", saveOptions)
         .execute();
 
```

Muestra cómo combinar documentos del flujo en un único documento de salida usando el contexto.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 try (FileInputStream firstStreamIn = new FileInputStream(inputDoc1)) {
     try (FileInputStream secondStreamIn = new FileInputStream(inputDoc2)) {
         OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
         {
             saveOptions.setPassword("Aspose.Words");
         }
         try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.MergeStreamContextDocuments.1.docx")) {
             Merger.create(mergerContext)
                     .from(firstStreamIn)
                     .from(secondStreamIn)
                     .to(streamOut, saveOptions)
                     .execute();
         }

         LoadOptions firstLoadOptions = new LoadOptions();
         {
             firstLoadOptions.setIgnoreOleData(true);
         }
         LoadOptions secondLoadOptions = new LoadOptions();
         {
             secondLoadOptions.setIgnoreOleData(false);
         }
         try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.MergeStreamContextDocuments.2.docx")) {
             Merger.create(mergerContext)
                     .from(firstStreamIn, firstLoadOptions)
                     .from(secondStreamIn, secondLoadOptions)
                     .to(streamOut1, SaveFormat.DOCX)
                     .execute();
         }
     }
 }
 
```

Muestra cómo convertir documentos con una sola línea de código usando el contexto.

```

 String doc = getMyDir() + "Big document.docx";

 ConverterContext converterContext = new ConverterContext();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.1.pdf")
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.2.pdf", SaveFormat.RTF)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(true);
 }
 Converter.create(converterContext)
         .from(doc, loadOptions)
         .to(getArtifactsDir() + "LowCode.ConvertContext.3.docx", saveOptions)
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.4.png", new ImageSaveOptions(SaveFormat.PNG))
         .execute();
 
```

Muestra cómo convertir documentos del flujo con una sola línea de código usando el contexto.

```

 String doc = getMyDir() + "Document.docx";
 ConverterContext converterContext = new ConverterContext();

 try (FileInputStream streamIn = new FileInputStream(doc)) {
     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ConvertContextStream.1.docx")) {
         Converter.create(converterContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.RTF)
                 .execute();
     }

     OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
     {
         saveOptions.setPassword("Aspose.Words");
     }
     LoadOptions loadOptions = new LoadOptions();
     {
         loadOptions.setIgnoreOleData(true);
     }
     try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.ConvertContextStream.2.docx")) {
         Converter.create(converterContext)
                 .from(streamIn, loadOptions)
                 .to(streamOut1, saveOptions)
                 .execute();
     }
 }
 
```

### from(InputStream input) {#from-java.io.InputStream}
```
public Processor from(InputStream input)
```


Especifica el documento de entrada para el procesamiento.

 **Remarks:** 

Si el procesador acepta solo un archivo como entrada, solo se procesará el último archivo especificado. El procesador [Merger](../../com.aspose.words/merger/) acepta varios archivos como entrada, como resultado todos los documentos especificados se combinarán. El procesador [Converter](../../com.aspose.words/converter/) acepta solo un archivo como entrada, por lo que solo se convertirá el último archivo especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| entrada | java.io.InputStream | Flujo del documento de entrada. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(InputStream input, LoadOptions loadOptions) {#from-java.io.InputStream-com.aspose.words.LoadOptions}
```
public Processor from(InputStream input, LoadOptions loadOptions)
```


Especifica el documento de entrada para el procesamiento.

 **Remarks:** 

Si el procesador acepta solo un archivo como entrada, solo se procesará el último archivo especificado. El procesador [Merger](../../com.aspose.words/merger/) acepta varios archivos como entrada, como resultado todos los documentos especificados se combinarán. El procesador [Converter](../../com.aspose.words/converter/) acepta solo un archivo como entrada, por lo que solo se convertirá el último archivo especificado.

 **Examples:** 

Muestra cómo combinar documentos del flujo en un único documento de salida usando el contexto.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 try (FileInputStream firstStreamIn = new FileInputStream(inputDoc1)) {
     try (FileInputStream secondStreamIn = new FileInputStream(inputDoc2)) {
         OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
         {
             saveOptions.setPassword("Aspose.Words");
         }
         try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.MergeStreamContextDocuments.1.docx")) {
             Merger.create(mergerContext)
                     .from(firstStreamIn)
                     .from(secondStreamIn)
                     .to(streamOut, saveOptions)
                     .execute();
         }

         LoadOptions firstLoadOptions = new LoadOptions();
         {
             firstLoadOptions.setIgnoreOleData(true);
         }
         LoadOptions secondLoadOptions = new LoadOptions();
         {
             secondLoadOptions.setIgnoreOleData(false);
         }
         try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.MergeStreamContextDocuments.2.docx")) {
             Merger.create(mergerContext)
                     .from(firstStreamIn, firstLoadOptions)
                     .from(secondStreamIn, secondLoadOptions)
                     .to(streamOut1, SaveFormat.DOCX)
                     .execute();
         }
     }
 }
 
```

Muestra cómo convertir documentos del flujo con una sola línea de código usando el contexto.

```

 String doc = getMyDir() + "Document.docx";
 ConverterContext converterContext = new ConverterContext();

 try (FileInputStream streamIn = new FileInputStream(doc)) {
     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ConvertContextStream.1.docx")) {
         Converter.create(converterContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.RTF)
                 .execute();
     }

     OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
     {
         saveOptions.setPassword("Aspose.Words");
     }
     LoadOptions loadOptions = new LoadOptions();
     {
         loadOptions.setIgnoreOleData(true);
     }
     try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.ConvertContextStream.2.docx")) {
         Converter.create(converterContext)
                 .from(streamIn, loadOptions)
                 .to(streamOut1, saveOptions)
                 .execute();
     }
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| entrada | java.io.InputStream | Flujo del documento de entrada. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Opciones de carga opcionales usadas para cargar el documento. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(String input) {#from-java.lang.String}
```
public Processor from(String input)
```


Especifica el documento de entrada para el procesamiento.

 **Remarks:** 

Si el procesador acepta solo un archivo como entrada, solo se procesará el último archivo especificado. El procesador [Merger](../../com.aspose.words/merger/) acepta varios archivos como entrada, como resultado todos los documentos especificados se combinarán. El procesador [Converter](../../com.aspose.words/converter/) acepta solo un archivo como entrada, por lo que solo se convertirá el último archivo especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| entrada | java.lang.String | Nombre de archivo del documento de entrada. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### from(String input, LoadOptions loadOptions) {#from-java.lang.String-com.aspose.words.LoadOptions}
```
public Processor from(String input, LoadOptions loadOptions)
```


Especifica el documento de entrada para el procesamiento.

 **Remarks:** 

Si el procesador acepta solo un archivo como entrada, solo se procesará el último archivo especificado. El procesador [Merger](../../com.aspose.words/merger/) acepta varios archivos como entrada, como resultado todos los documentos especificados se combinarán. El procesador [Converter](../../com.aspose.words/converter/) acepta solo un archivo como entrada, por lo que solo se convertirá el último archivo especificado.

 **Examples:** 

Muestra cómo combinar documentos en un único documento de salida usando el contexto.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.1.docx")
         .execute();

 LoadOptions firstLoadOptions = new LoadOptions();
 {
     firstLoadOptions.setIgnoreOleData(true);
 }
 LoadOptions secondLoadOptions = new LoadOptions();
 {
     secondLoadOptions.setIgnoreOleData(false);
 }
 Merger.create(mergerContext)
         .from(inputDoc1, firstLoadOptions)
         .from(inputDoc2, secondLoadOptions)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.2.docx", SaveFormat.DOCX)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.3.docx", saveOptions)
         .execute();
 
```

Muestra cómo convertir documentos con una sola línea de código usando el contexto.

```

 String doc = getMyDir() + "Big document.docx";

 ConverterContext converterContext = new ConverterContext();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.1.pdf")
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.2.pdf", SaveFormat.RTF)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(true);
 }
 Converter.create(converterContext)
         .from(doc, loadOptions)
         .to(getArtifactsDir() + "LowCode.ConvertContext.3.docx", saveOptions)
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.4.png", new ImageSaveOptions(SaveFormat.PNG))
         .execute();
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| entrada | java.lang.String | Nombre de archivo del documento de entrada. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Opciones de carga opcionales usadas para cargar el documento. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### to(OutputStream output, SaveOptions saveOptions) {#to-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public Processor to(OutputStream output, SaveOptions saveOptions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| salida | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(OutputStream output, int saveFormat) {#to-java.io.OutputStream-int}
```
public Processor to(OutputStream output, int saveFormat)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| salida | java.io.OutputStream |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(String output) {#to-java.lang.String}
```
public Processor to(String output)
```


Especifica el archivo de salida para el procesador.

 **Remarks:** 

Si la salida consiste en varios archivos, el nombre de archivo de salida especificado se usa para generar el nombre de archivo de cada parte siguiendo la regla: 'outputFile\_partIndex.extension'.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| salida | java.lang.String | Nombre del archivo de salida. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, SaveOptions saveOptions) {#to-java.lang.String-com.aspose.words.SaveOptions}
```
public Processor to(String output, SaveOptions saveOptions)
```


Especifica el archivo de salida para el procesador.

 **Remarks:** 

Si la salida consiste en varios archivos, el nombre de archivo de salida especificado se usa para generar el nombre de archivo de cada parte siguiendo la regla: 'outputFile\_partIndex.extension'.

 **Examples:** 

Muestra cómo combinar documentos en un único documento de salida usando el contexto.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.1.docx")
         .execute();

 LoadOptions firstLoadOptions = new LoadOptions();
 {
     firstLoadOptions.setIgnoreOleData(true);
 }
 LoadOptions secondLoadOptions = new LoadOptions();
 {
     secondLoadOptions.setIgnoreOleData(false);
 }
 Merger.create(mergerContext)
         .from(inputDoc1, firstLoadOptions)
         .from(inputDoc2, secondLoadOptions)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.2.docx", SaveFormat.DOCX)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.3.docx", saveOptions)
         .execute();
 
```

Muestra cómo convertir documentos con una sola línea de código usando el contexto.

```

 String doc = getMyDir() + "Big document.docx";

 ConverterContext converterContext = new ConverterContext();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.1.pdf")
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.2.pdf", SaveFormat.RTF)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(true);
 }
 Converter.create(converterContext)
         .from(doc, loadOptions)
         .to(getArtifactsDir() + "LowCode.ConvertContext.3.docx", saveOptions)
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.4.png", new ImageSaveOptions(SaveFormat.PNG))
         .execute();
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| salida | java.lang.String | Nombre del archivo de salida. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Opciones de guardado opcionales. Si no se especifican, el formato de guardado se determina por la extensión del archivo. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, int saveFormat) {#to-java.lang.String-int}
```
public Processor to(String output, int saveFormat)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| salida | java.lang.String |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, SaveOptions saveOptions) {#to-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor to(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| salida | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, int saveFormat) {#to-java.util.ArrayList-int}
```
public Processor to(ArrayList output, int saveFormat)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| salida | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, SaveOptions saveOptions) {#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor toOutput(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| salida | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, int saveFormat) {#toOutput-java.util.ArrayList-int}
```
public Processor toOutput(ArrayList output, int saveFormat)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| salida | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
