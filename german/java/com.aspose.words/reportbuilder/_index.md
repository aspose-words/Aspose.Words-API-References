---
title: "ReportBuilder"
linktitle: "ReportBuilder"
second_title: "Aspose.Words für Java"
description: "Stellt Methoden bereit, die dazu dienen, Vorlagen mit Daten mithilfe der LINQ Reporting Engine in Java zu füllen."
type: docs
weight: 571
url: /de/java/com.aspose.words/reportbuilder/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class ReportBuilder extends Processor
```

Stellt Methoden bereit, die dazu dienen, Vorlagen mit Daten mithilfe der LINQ Reporting Engine zu füllen.
## Methoden

| Methode | Beschreibung |
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
| [buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data)](#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object) | Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und erzeugt einen fertigen Bericht mit dem angegebenen Ausgabeformat und zusätzlichen Optionen. |
| [buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object-com.aspose.words.ReportBuilderOptions) | Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und erzeugt einen fertigen Bericht mit dem angegebenen Ausgabeformat und zusätzlichen Optionen. |
| [buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, String dataSourceName)](#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object-java.lang.String) | Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und erzeugt einen fertigen Bericht mit dem angegebenen Ausgabeformat, einer benannten Datenquellenreferenz und zusätzlichen Optionen. |
| [buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions) | Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und erzeugt einen fertigen Bericht mit dem angegebenen Ausgabeformat, einer benannten Datenquellenreferenz und zusätzlichen Optionen. |
| [buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object[] data, String[] dataSourceNames)](#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object---java.lang.String) | Füllt das Vorlagendokument mit Daten aus mehreren Quellen und erzeugt einen fertigen Bericht mit einem angegebenen Ausgabeformat und zusätzlichen Optionen. |
| [buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions) | Füllt das Vorlagendokument mit Daten aus mehreren Quellen und erzeugt einen fertigen Bericht mit einem angegebenen Ausgabeformat und zusätzlichen Optionen. |
| [buildReport(String inputFileName, String outputFileName, int saveFormat, Object data)](#buildReport-java.lang.String-java.lang.String-int-java.lang.Object) |  |
| [buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-int-java.lang.Object-com.aspose.words.ReportBuilderOptions) |  |
| [buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, String dataSourceName)](#buildReport-java.lang.String-java.lang.String-int-java.lang.Object-java.lang.String) |  |
| [buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-int-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions) |  |
| [buildReport(String inputFileName, String outputFileName, int saveFormat, Object[] data, String[] dataSourceNames)](#buildReport-java.lang.String-java.lang.String-int-java.lang.Object---java.lang.String) |  |
| [buildReport(String inputFileName, String outputFileName, int saveFormat, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-int-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions) |  |
| [buildReport(String inputFileName, String outputFileName, Object data)](#buildReport-java.lang.String-java.lang.String-java.lang.Object) | Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und erzeugt einen fertigen Bericht mit zusätzlichen Optionen. |
| [buildReport(String inputFileName, String outputFileName, Object data, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-java.lang.Object-com.aspose.words.ReportBuilderOptions) | Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und erzeugt einen fertigen Bericht mit zusätzlichen Optionen. |
| [buildReport(String inputFileName, String outputFileName, Object data, String dataSourceName)](#buildReport-java.lang.String-java.lang.String-java.lang.Object-java.lang.String) | Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und erzeugt einen fertigen Bericht mit einer benannten Datenquellenreferenz und zusätzlichen Optionen. |
| [buildReport(String inputFileName, String outputFileName, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions) | Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und erzeugt einen fertigen Bericht mit einer benannten Datenquellenreferenz und zusätzlichen Optionen. |
| [buildReport(String inputFileName, String outputFileName, Object[] data, String[] dataSourceNames)](#buildReport-java.lang.String-java.lang.String-java.lang.Object---java.lang.String) | Füllt das Vorlagendokument mit Daten aus mehreren Quellen und erzeugt einen fertigen Bericht mit zusätzlichen Optionen. |
| [buildReport(String inputFileName, String outputFileName, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions) | Füllt das Vorlagendokument mit Daten aus mehreren Quellen und erzeugt einen fertigen Bericht mit zusätzlichen Optionen. |
| [buildReportToImages(InputStream inputStream, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames)](#buildReportToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.Object---java.lang.String) | Füllt das Vorlagendokument mit Daten aus mehreren Quellen. |
| [buildReportToImages(InputStream inputStream, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)](#buildReportToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions) | Füllt das Vorlagendokument mit Daten aus mehreren Quellen. |
| [buildReportToImages(String inputFileName, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames)](#buildReportToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.Object---java.lang.String) | Füllt das Vorlagendokument mit Daten aus mehreren Quellen. |
| [buildReportToImages(String inputFileName, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)](#buildReportToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions) | Füllt das Vorlagendokument mit Daten aus mehreren Quellen. |
| [create()](#create) | Erstellt eine neue Instanz des Report-Builder-Processors. |
| [create(ReportBuilderContext context)](#create-com.aspose.words.ReportBuilderContext) | Erstellt eine neue Instanz des Report-Builder-Processors. |
| [execute()](#execute) | Führt die Prozessor‑Aktion aus. |
| [from(InputStream input)](#from-java.io.InputStream) | Gibt das Eingabedokument für die Verarbeitung an. |
| [from(InputStream input, LoadOptions loadOptions)](#from-java.io.InputStream-com.aspose.words.LoadOptions) | Gibt das Eingabedokument für die Verarbeitung an. |
| [from(String input)](#from-java.lang.String) | Gibt das Eingabedokument für die Verarbeitung an. |
| [from(String input, LoadOptions loadOptions)](#from-java.lang.String-com.aspose.words.LoadOptions) | Gibt das Eingabedokument für die Verarbeitung an. |
| [to(OutputStream output, SaveOptions saveOptions)](#to-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [to(OutputStream output, int saveFormat)](#to-java.io.OutputStream-int) |  |
| [to(String output)](#to-java.lang.String) | Gibt die Ausgabedatei für den Prozessor an. |
| [to(String output, SaveOptions saveOptions)](#to-java.lang.String-com.aspose.words.SaveOptions) | Gibt die Ausgabedatei für den Prozessor an. |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| Daten | java.lang.Object |  |

### buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| Daten | java.lang.Object |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, String dataSourceName) {#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object-java.lang.String}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, String dataSourceName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| Daten | java.lang.Object |  |
| dataSourceName | java.lang.String |  |

### buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| Daten | java.lang.Object |  |
| dataSourceName | java.lang.String |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object[] data, String[] dataSourceNames) {#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object---java.lang.String}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object[] data, String[] dataSourceNames)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| Daten | java.lang.Object[] |  |
| dataSourceNames | java.lang.String[] |  |

### buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| Daten | java.lang.Object[] |  |
| dataSourceNames | java.lang.String[] |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data) {#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| Daten | java.lang.Object |  |

### buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| Daten | java.lang.Object |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, String dataSourceName) {#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object-java.lang.String}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, String dataSourceName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| Daten | java.lang.Object |  |
| dataSourceName | java.lang.String |  |

### buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| Daten | java.lang.Object |  |
| dataSourceName | java.lang.String |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object[] data, String[] dataSourceNames) {#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object---java.lang.String}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object[] data, String[] dataSourceNames)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| Daten | java.lang.Object[] |  |
| dataSourceNames | java.lang.String[] |  |

### buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| Daten | java.lang.Object[] |  |
| dataSourceNames | java.lang.String[] |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data) {#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object}
```
public static void buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data)
```


Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und erzeugt einen fertigen Bericht mit dem angegebenen Ausgabeformat und zusätzlichen Optionen.

 **Remarks:** 

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel zu erzeugen: outputFile\_partIndex.extension.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne mehrseitige TIFF-Datei gespeichert.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | java.lang.String | Der Eingabedateiname. |
| outputFileName | java.lang.String | Der Ausgabedateiname. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Die Speicheroptionen der Ausgabe. |
| Daten | java.lang.Object | Ein Datenquellenobjekt. |

### buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, ReportBuilderOptions reportBuilderOptions)
```


Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und erzeugt einen fertigen Bericht mit dem angegebenen Ausgabeformat und zusätzlichen Optionen.

 **Remarks:** 

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel zu erzeugen: outputFile\_partIndex.extension.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne mehrseitige TIFF-Datei gespeichert.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | java.lang.String | Der Eingabedateiname. |
| outputFileName | java.lang.String | Der Ausgabedateiname. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Die Speicheroptionen der Ausgabe. |
| Daten | java.lang.Object | Ein Datenquellenobjekt. |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | Zusätzliche Optionen zum Erstellen des Berichts. |

### buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, String dataSourceName) {#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object-java.lang.String}
```
public static void buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, String dataSourceName)
```


Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und erzeugt einen fertigen Bericht mit dem angegebenen Ausgabeformat, einer benannten Datenquellenreferenz und zusätzlichen Optionen.

 **Remarks:** 

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel zu erzeugen: outputFile\_partIndex.extension.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne mehrseitige TIFF-Datei gespeichert.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | java.lang.String | Der Eingabedateiname. |
| outputFileName | java.lang.String | Der Ausgabedateiname. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Die Speicheroptionen der Ausgabe. |
| Daten | java.lang.Object | Ein Datenquellenobjekt. |
| dataSourceName | java.lang.String | Ein Name, um das Datenquellenobjekt in der Vorlage zu referenzieren. |

### buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)
```


Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und erzeugt einen fertigen Bericht mit dem angegebenen Ausgabeformat, einer benannten Datenquellenreferenz und zusätzlichen Optionen.

 **Remarks:** 

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel zu erzeugen: outputFile\_partIndex.extension.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne mehrseitige TIFF-Datei gespeichert.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | java.lang.String | Der Eingabedateiname. |
| outputFileName | java.lang.String | Der Ausgabedateiname. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Die Speicheroptionen der Ausgabe. |
| Daten | java.lang.Object | Ein Datenquellenobjekt. |
| dataSourceName | java.lang.String | Ein Name, um das Datenquellenobjekt in der Vorlage zu referenzieren. |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | Zusätzliche Optionen zum Erstellen des Berichts. |

### buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object[] data, String[] dataSourceNames) {#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object---java.lang.String}
```
public static void buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object[] data, String[] dataSourceNames)
```


Füllt das Vorlagendokument mit Daten aus mehreren Quellen und erzeugt einen fertigen Bericht mit einem angegebenen Ausgabeformat und zusätzlichen Optionen.

 **Remarks:** 

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel zu erzeugen: outputFile\_partIndex.extension.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne mehrseitige TIFF-Datei gespeichert.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | java.lang.String | Der Eingabedateiname. |
| outputFileName | java.lang.String | Der Ausgabedateiname. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Die Speicheroptionen der Ausgabe. |
| Daten | java.lang.Object[] | Ein Array von Datenquellenobjekten. |
| dataSourceNames | java.lang.String[] | Ein Array von Namen, um die Datenquellenobjekte innerhalb der Vorlage zu referenzieren. |

### buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)
```


Füllt das Vorlagendokument mit Daten aus mehreren Quellen und erzeugt einen fertigen Bericht mit einem angegebenen Ausgabeformat und zusätzlichen Optionen.

 **Remarks:** 

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel zu erzeugen: outputFile\_partIndex.extension.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne mehrseitige TIFF-Datei gespeichert.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | java.lang.String | Der Eingabedateiname. |
| outputFileName | java.lang.String | Der Ausgabedateiname. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Die Speicheroptionen der Ausgabe. |
| Daten | java.lang.Object[] | Ein Array von Datenquellenobjekten. |
| dataSourceNames | java.lang.String[] | Ein Array von Namen, um die Datenquellenobjekte innerhalb der Vorlage zu referenzieren. |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | Zusätzliche Optionen zum Erstellen des Berichts. |

### buildReport(String inputFileName, String outputFileName, int saveFormat, Object data) {#buildReport-java.lang.String-java.lang.String-int-java.lang.Object}
```
public static void buildReport(String inputFileName, String outputFileName, int saveFormat, Object data)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| Daten | java.lang.Object |  |

### buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-int-java.lang.Object-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| Daten | java.lang.Object |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, String dataSourceName) {#buildReport-java.lang.String-java.lang.String-int-java.lang.Object-java.lang.String}
```
public static void buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, String dataSourceName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| Daten | java.lang.Object |  |
| dataSourceName | java.lang.String |  |

### buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-int-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| Daten | java.lang.Object |  |
| dataSourceName | java.lang.String |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(String inputFileName, String outputFileName, int saveFormat, Object[] data, String[] dataSourceNames) {#buildReport-java.lang.String-java.lang.String-int-java.lang.Object---java.lang.String}
```
public static void buildReport(String inputFileName, String outputFileName, int saveFormat, Object[] data, String[] dataSourceNames)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| Daten | java.lang.Object[] |  |
| dataSourceNames | java.lang.String[] |  |

### buildReport(String inputFileName, String outputFileName, int saveFormat, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-int-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, int saveFormat, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| Daten | java.lang.Object[] |  |
| dataSourceNames | java.lang.String[] |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(String inputFileName, String outputFileName, Object data) {#buildReport-java.lang.String-java.lang.String-java.lang.Object}
```
public static void buildReport(String inputFileName, String outputFileName, Object data)
```


Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und erzeugt einen fertigen Bericht mit zusätzlichen Optionen.

 **Remarks:** 

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel zu erzeugen: outputFile\_partIndex.extension.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne mehrseitige TIFF-Datei gespeichert.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | java.lang.String | Der Eingabedateiname. |
| outputFileName | java.lang.String | Der Ausgabedateiname. |
| Daten | java.lang.Object | Ein Datenquellenobjekt. |

### buildReport(String inputFileName, String outputFileName, Object data, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-java.lang.Object-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, Object data, ReportBuilderOptions reportBuilderOptions)
```


Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und erzeugt einen fertigen Bericht mit zusätzlichen Optionen.

 **Remarks:** 

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel zu erzeugen: outputFile\_partIndex.extension.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne mehrseitige TIFF-Datei gespeichert.

 **Examples:** 

Zeigt, wie ein Dokument mit Daten gefüllt wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | java.lang.String | Der Eingabedateiname. |
| outputFileName | java.lang.String | Der Ausgabedateiname. |
| Daten | java.lang.Object | Ein Datenquellenobjekt. |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | Zusätzliche Optionen zum Erstellen des Berichts. |

### buildReport(String inputFileName, String outputFileName, Object data, String dataSourceName) {#buildReport-java.lang.String-java.lang.String-java.lang.Object-java.lang.String}
```
public static void buildReport(String inputFileName, String outputFileName, Object data, String dataSourceName)
```


Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und erzeugt einen fertigen Bericht mit einer benannten Datenquellenreferenz und zusätzlichen Optionen.

 **Remarks:** 

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel zu erzeugen: outputFile\_partIndex.extension.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne mehrseitige TIFF-Datei gespeichert.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | java.lang.String | Der Eingabedateiname. |
| outputFileName | java.lang.String | Der Ausgabedateiname. |
| Daten | java.lang.Object | Ein Datenquellenobjekt. |
| dataSourceName | java.lang.String | Ein Name, um das Datenquellenobjekt in der Vorlage zu referenzieren. |

### buildReport(String inputFileName, String outputFileName, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)
```


Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und erzeugt einen fertigen Bericht mit einer benannten Datenquellenreferenz und zusätzlichen Optionen.

 **Remarks:** 

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel zu erzeugen: outputFile\_partIndex.extension.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne mehrseitige TIFF-Datei gespeichert.

 **Examples:** 

Zeigt, wie ein Dokument mit Datenquellen gefüllt wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | java.lang.String | Der Eingabedateiname. |
| outputFileName | java.lang.String | Der Ausgabedateiname. |
| Daten | java.lang.Object | Ein Datenquellenobjekt. |
| dataSourceName | java.lang.String | Ein Name, um das Datenquellenobjekt in der Vorlage zu referenzieren. |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | Zusätzliche Optionen zum Erstellen des Berichts. |

### buildReport(String inputFileName, String outputFileName, Object[] data, String[] dataSourceNames) {#buildReport-java.lang.String-java.lang.String-java.lang.Object---java.lang.String}
```
public static void buildReport(String inputFileName, String outputFileName, Object[] data, String[] dataSourceNames)
```


Füllt das Vorlagendokument mit Daten aus mehreren Quellen und erzeugt einen fertigen Bericht mit zusätzlichen Optionen. Diese Überladung bestimmt das Speicherformat automatisch anhand der Dateierweiterung der Ausgabedatei.

 **Remarks:** 

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel zu erzeugen: outputFile\_partIndex.extension.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne mehrseitige TIFF-Datei gespeichert.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | java.lang.String | Der Eingabedateiname. |
| outputFileName | java.lang.String | Der Ausgabedateiname. |
| Daten | java.lang.Object[] | Ein Array von Datenquellenobjekten. |
| dataSourceNames | java.lang.String[] | Ein Array von Namen, um die Datenquellenobjekte innerhalb der Vorlage zu referenzieren. |

### buildReport(String inputFileName, String outputFileName, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)
```


Füllt das Vorlagendokument mit Daten aus mehreren Quellen und erzeugt einen fertigen Bericht mit zusätzlichen Optionen. Diese Überladung bestimmt das Speicherformat automatisch anhand der Dateierweiterung der Ausgabedatei.

 **Remarks:** 

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel zu erzeugen: outputFile\_partIndex.extension.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne mehrseitige TIFF-Datei gespeichert.

 **Examples:** 

Zeigt, wie ein Dokument mit Datenquellen gefüllt wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | java.lang.String | Der Eingabedateiname. |
| outputFileName | java.lang.String | Der Ausgabedateiname. |
| Daten | java.lang.Object[] | Ein Array von Datenquellenobjekten. |
| dataSourceNames | java.lang.String[] | Ein Array von Namen, um die Datenquellenobjekte innerhalb der Vorlage zu referenzieren. |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | Zusätzliche Optionen zum Erstellen des Berichts. |

### buildReportToImages(InputStream inputStream, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames) {#buildReportToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.Object---java.lang.String}
```
public static OutputStream[] buildReportToImages(InputStream inputStream, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames)
```


Füllt das Vorlagendokument mit Daten aus mehreren Quellen. Gibt die Ausgabe als Bilder aus.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | java.io.InputStream | Der Eingabedateistream. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Die Speicheroptionen der Ausgabe. |
| Daten | java.lang.Object[] | Ein Array von Datenquellenobjekten. |
| dataSourceNames | java.lang.String[] | Ein Array von Namen, um die Datenquellenobjekte innerhalb der Vorlage zu referenzieren. |

**Returns:**
java.io.OutputStream[]
### buildReportToImages(InputStream inputStream, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions) {#buildReportToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions}
```
public static OutputStream[] buildReportToImages(InputStream inputStream, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)
```


Füllt das Vorlagendokument mit Daten aus mehreren Quellen. Gibt die Ausgabe als Bilder aus.

 **Examples:** 

Zeigt, wie ein Dokument mit Datenquellen gefüllt wird, indem Dokumente aus dem Stream verwendet werden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | java.io.InputStream | Der Eingabedateistream. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Die Speicheroptionen der Ausgabe. |
| Daten | java.lang.Object[] | Ein Array von Datenquellenobjekten. |
| dataSourceNames | java.lang.String[] | Ein Array von Namen, um die Datenquellenobjekte innerhalb der Vorlage zu referenzieren. |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | Zusätzliche Optionen zum Erstellen des Berichts. |

**Returns:**
java.io.OutputStream[]
### buildReportToImages(String inputFileName, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames) {#buildReportToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.Object---java.lang.String}
```
public static OutputStream[] buildReportToImages(String inputFileName, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames)
```


Füllt das Vorlagendokument mit Daten aus mehreren Quellen. Gibt die Ausgabe als Bilder aus.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | java.lang.String | Der Eingabedateiname. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Die Speicheroptionen der Ausgabe. |
| Daten | java.lang.Object[] | Ein Array von Datenquellenobjekten. |
| dataSourceNames | java.lang.String[] | Ein Array von Namen, um die Datenquellenobjekte innerhalb der Vorlage zu referenzieren. |

**Returns:**
java.io.OutputStream[]
### buildReportToImages(String inputFileName, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions) {#buildReportToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions}
```
public static OutputStream[] buildReportToImages(String inputFileName, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)
```


Füllt das Vorlagendokument mit Daten aus mehreren Quellen. Gibt die Ausgabe als Bilder aus.

 **Examples:** 

Zeigt, wie ein Dokument mit Datenquellen gefüllt wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | java.lang.String | Der Eingabedateiname. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Die Speicheroptionen der Ausgabe. |
| Daten | java.lang.Object[] | Ein Array von Datenquellenobjekten. |
| dataSourceNames | java.lang.String[] | Ein Array von Namen, um die Datenquellenobjekte innerhalb der Vorlage zu referenzieren. |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | Zusätzliche Optionen zum Erstellen des Berichts. |

**Returns:**
java.io.OutputStream[]
### create() {#create}
```
public static ReportBuilder create()
```


Erstellt eine neue Instanz des Report-Builder-Processors.

**Returns:**
[ReportBuilder](../../com.aspose.words/reportbuilder/)
### create(ReportBuilderContext context) {#create-com.aspose.words.ReportBuilderContext}
```
public static ReportBuilder create(ReportBuilderContext context)
```


Erstellt eine neue Instanz des Report-Builder-Processors.

 **Examples:** 

Zeigt, wie ein Dokument mit Datenquellen gefüllt wird.

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

Zeigt, wie ein Dokument mit Datenquellen gefüllt wird, indem Dokumente aus dem Stream verwendet werden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| context | [ReportBuilderContext](../../com.aspose.words/reportbuildercontext/) |  |

**Returns:**
[ReportBuilder](../../com.aspose.words/reportbuilder/)
### execute() {#execute}
```
public void execute()
```


Führt die Prozessor‑Aktion aus.

 **Examples:** 

Zeigt, wie man Dokumente zu einem einzigen Ausgabedokument im Kontext zusammenführt.

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

Zeigt, wie man Dokumente aus einem Stream zu einem einzigen Ausgabedokument im Kontext zusammenführt.

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

Zeigt, wie man Dokumente mit einer einzigen Codezeile im Kontext konvertiert.

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

Zeigt, wie man Dokumente aus einem Stream mit einer einzigen Codezeile im Kontext konvertiert.

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


Gibt das Eingabedokument für die Verarbeitung an.

 **Remarks:** 

Wenn der Prozessor nur eine Datei als Eingabe akzeptiert, wird nur die zuletzt angegebene Datei verarbeitet. Der [Merger](../../com.aspose.words/merger/) Prozessor akzeptiert mehrere Dateien als Eingabe, sodass alle angegebenen Dokumente zusammengeführt werden. Der [Converter](../../com.aspose.words/converter/) Prozessor akzeptiert nur eine Datei als Eingabe, daher wird nur die zuletzt angegebene Datei konvertiert.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Eingabe | java.io.InputStream | Eingabedokumenten‑Stream. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(InputStream input, LoadOptions loadOptions) {#from-java.io.InputStream-com.aspose.words.LoadOptions}
```
public Processor from(InputStream input, LoadOptions loadOptions)
```


Gibt das Eingabedokument für die Verarbeitung an.

 **Remarks:** 

Wenn der Prozessor nur eine Datei als Eingabe akzeptiert, wird nur die zuletzt angegebene Datei verarbeitet. Der [Merger](../../com.aspose.words/merger/) Prozessor akzeptiert mehrere Dateien als Eingabe, sodass alle angegebenen Dokumente zusammengeführt werden. Der [Converter](../../com.aspose.words/converter/) Prozessor akzeptiert nur eine Datei als Eingabe, daher wird nur die zuletzt angegebene Datei konvertiert.

 **Examples:** 

Zeigt, wie man Dokumente aus einem Stream zu einem einzigen Ausgabedokument im Kontext zusammenführt.

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

Zeigt, wie man Dokumente aus einem Stream mit einer einzigen Codezeile im Kontext konvertiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Eingabe | java.io.InputStream | Eingabedokumenten‑Stream. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Optionale Ladeoptionen, die zum Laden des Dokuments verwendet werden. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(String input) {#from-java.lang.String}
```
public Processor from(String input)
```


Gibt das Eingabedokument für die Verarbeitung an.

 **Remarks:** 

Wenn der Prozessor nur eine Datei als Eingabe akzeptiert, wird nur die zuletzt angegebene Datei verarbeitet. Der [Merger](../../com.aspose.words/merger/) Prozessor akzeptiert mehrere Dateien als Eingabe, sodass alle angegebenen Dokumente zusammengeführt werden. Der [Converter](../../com.aspose.words/converter/) Prozessor akzeptiert nur eine Datei als Eingabe, daher wird nur die zuletzt angegebene Datei konvertiert.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Eingabe | java.lang.String | Eingabedokumentdateiname. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### from(String input, LoadOptions loadOptions) {#from-java.lang.String-com.aspose.words.LoadOptions}
```
public Processor from(String input, LoadOptions loadOptions)
```


Gibt das Eingabedokument für die Verarbeitung an.

 **Remarks:** 

Wenn der Prozessor nur eine Datei als Eingabe akzeptiert, wird nur die zuletzt angegebene Datei verarbeitet. Der [Merger](../../com.aspose.words/merger/) Prozessor akzeptiert mehrere Dateien als Eingabe, sodass alle angegebenen Dokumente zusammengeführt werden. Der [Converter](../../com.aspose.words/converter/) Prozessor akzeptiert nur eine Datei als Eingabe, daher wird nur die zuletzt angegebene Datei konvertiert.

 **Examples:** 

Zeigt, wie man Dokumente zu einem einzigen Ausgabedokument im Kontext zusammenführt.

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

Zeigt, wie man Dokumente mit einer einzigen Codezeile im Kontext konvertiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Eingabe | java.lang.String | Eingabedokumentdateiname. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Optionale Ladeoptionen, die zum Laden des Dokuments verwendet werden. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### to(OutputStream output, SaveOptions saveOptions) {#to-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public Processor to(OutputStream output, SaveOptions saveOptions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Ausgabe | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(OutputStream output, int saveFormat) {#to-java.io.OutputStream-int}
```
public Processor to(OutputStream output, int saveFormat)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Ausgabe | java.io.OutputStream |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(String output) {#to-java.lang.String}
```
public Processor to(String output)
```


Gibt die Ausgabedatei für den Prozessor an.

 **Remarks:** 

Wenn die Ausgabe aus mehreren Dateien besteht, wird der angegebene Ausgabedateiname verwendet, um für jeden Teil gemäß der Regel 'outputFile\_partIndex.extension' einen Dateinamen zu erzeugen.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Ausgabe | java.lang.String | Ausgabedateiname. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, SaveOptions saveOptions) {#to-java.lang.String-com.aspose.words.SaveOptions}
```
public Processor to(String output, SaveOptions saveOptions)
```


Gibt die Ausgabedatei für den Prozessor an.

 **Remarks:** 

Wenn die Ausgabe aus mehreren Dateien besteht, wird der angegebene Ausgabedateiname verwendet, um für jeden Teil gemäß der Regel 'outputFile\_partIndex.extension' einen Dateinamen zu erzeugen.

 **Examples:** 

Zeigt, wie man Dokumente zu einem einzigen Ausgabedokument im Kontext zusammenführt.

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

Zeigt, wie man Dokumente mit einer einzigen Codezeile im Kontext konvertiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Ausgabe | java.lang.String | Ausgabedateiname. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Optionale Speicheroptionen. Wenn nicht angegeben, wird das Speicherformat anhand der Dateierweiterung bestimmt. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, int saveFormat) {#to-java.lang.String-int}
```
public Processor to(String output, int saveFormat)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Ausgabe | java.lang.String |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, SaveOptions saveOptions) {#to-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor to(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Ausgabe | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, int saveFormat) {#to-java.util.ArrayList-int}
```
public Processor to(ArrayList output, int saveFormat)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Ausgabe | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, SaveOptions saveOptions) {#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor toOutput(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Ausgabe | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, int saveFormat) {#toOutput-java.util.ArrayList-int}
```
public Processor toOutput(ArrayList output, int saveFormat)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Ausgabe | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
