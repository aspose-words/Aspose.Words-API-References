---
title: "Comparer"
linktitle: "Comparer"
second_title: "Aspose.Words für Java"
description: "Stellt Methoden bereit, die zum Vergleichen von Dokumenten in Java gedacht sind."
type: docs
weight: 114
url: /de/java/com.aspose.words/comparer/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class Comparer extends Processor
```

Stellt Methoden zum Vergleich von Dokumenten bereit.
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [compare(InputStream v1, InputStream v2, OutputStream outputStream, SaveOptions saveOptions, String author, Date dateTime)](#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.util.Date) |  |
| [compare(InputStream v1, InputStream v2, OutputStream outputStream, SaveOptions saveOptions, String author, Date dateTime, CompareOptions compareOptions)](#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) |  |
| [compare(InputStream v1, InputStream v2, OutputStream outputStream, int saveFormat, String author, Date dateTime)](#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.util.Date) |  |
| [compare(InputStream v1, InputStream v2, OutputStream outputStream, int saveFormat, String author, Date dateTime, CompareOptions compareOptions)](#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) |  |
| [compare(String v1, String v2, String outputFileName, SaveOptions saveOptions, String author, Date dateTime)](#compare-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.util.Date) | Vergleicht zwei Dokumente mit zusätzlichen Optionen und speichert die Unterschiede in die angegebene Ausgabedatei im bereitgestellten Speicherformat, wobei Änderungen als eine Reihe von Bearbeitungs‑ und Formatierungsrevisionen erzeugt werden. |
| [compare(String v1, String v2, String outputFileName, SaveOptions saveOptions, String author, Date dateTime, CompareOptions compareOptions)](#compare-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) | Vergleicht zwei Dokumente mit zusätzlichen Optionen und speichert die Unterschiede in die angegebene Ausgabedatei im bereitgestellten Speicherformat, wobei Änderungen als eine Reihe von Bearbeitungs‑ und Formatierungsrevisionen erzeugt werden. |
| [compare(String v1, String v2, String outputFileName, int saveFormat, String author, Date dateTime)](#compare-java.lang.String-java.lang.String-java.lang.String-int-java.lang.String-java.util.Date) |  |
| [compare(String v1, String v2, String outputFileName, int saveFormat, String author, Date dateTime, CompareOptions compareOptions)](#compare-java.lang.String-java.lang.String-java.lang.String-int-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) |  |
| [compare(String v1, String v2, String outputFileName, String author, Date dateTime)](#compare-java.lang.String-java.lang.String-java.lang.String-java.lang.String-java.util.Date) | Vergleicht zwei Dokumente mit zusätzlichen Optionen und speichert die Unterschiede in die angegebene Ausgabedatei, wobei Änderungen als eine Reihe von Bearbeitungs‑ und Formatierungsrevisionen erzeugt werden. |
| [compare(String v1, String v2, String outputFileName, String author, Date dateTime, CompareOptions compareOptions)](#compare-java.lang.String-java.lang.String-java.lang.String-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) | Vergleicht zwei Dokumente mit zusätzlichen Optionen und speichert die Unterschiede in die angegebene Ausgabedatei, wobei Änderungen als eine Reihe von Bearbeitungs‑ und Formatierungsrevisionen erzeugt werden. |
| [compareToImages(InputStream v1, InputStream v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime)](#compareToImages-java.io.InputStream-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date) | Vergleicht zwei Dokumente und speichert die Unterschiede als Bilder. |
| [compareToImages(InputStream v1, InputStream v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime, CompareOptions compareOptions)](#compareToImages-java.io.InputStream-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) | Vergleicht zwei Dokumente und speichert die Unterschiede als Bilder. |
| [compareToImages(String v1, String v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime)](#compareToImages-java.lang.String-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date) | Vergleicht zwei Dokumente und speichert die Unterschiede als Bilder. |
| [compareToImages(String v1, String v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime, CompareOptions compareOptions)](#compareToImages-java.lang.String-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) | Vergleicht zwei Dokumente und speichert die Unterschiede als Bilder. |
| [create()](#create) | Erstellt eine neue Instanz des Converter‑Prozessors. |
| [create(ComparerContext context)](#create-com.aspose.words.ComparerContext) | Erstellt eine neue Instanz des Comparer‑Prozessors. |
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
### compare(InputStream v1, InputStream v2, OutputStream outputStream, SaveOptions saveOptions, String author, Date dateTime) {#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.util.Date}
```
public static void compare(InputStream v1, InputStream v2, OutputStream outputStream, SaveOptions saveOptions, String author, Date dateTime)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | java.io.InputStream |  |
| v2 | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| Autor | java.lang.String |  |
| dateTime | java.util.Date |  |

### compare(InputStream v1, InputStream v2, OutputStream outputStream, SaveOptions saveOptions, String author, Date dateTime, CompareOptions compareOptions) {#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static void compare(InputStream v1, InputStream v2, OutputStream outputStream, SaveOptions saveOptions, String author, Date dateTime, CompareOptions compareOptions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | java.io.InputStream |  |
| v2 | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| Autor | java.lang.String |  |
| dateTime | java.util.Date |  |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) |  |

### compare(InputStream v1, InputStream v2, OutputStream outputStream, int saveFormat, String author, Date dateTime) {#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.util.Date}
```
public static void compare(InputStream v1, InputStream v2, OutputStream outputStream, int saveFormat, String author, Date dateTime)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | java.io.InputStream |  |
| v2 | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| Autor | java.lang.String |  |
| dateTime | java.util.Date |  |

### compare(InputStream v1, InputStream v2, OutputStream outputStream, int saveFormat, String author, Date dateTime, CompareOptions compareOptions) {#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static void compare(InputStream v1, InputStream v2, OutputStream outputStream, int saveFormat, String author, Date dateTime, CompareOptions compareOptions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | java.io.InputStream |  |
| v2 | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| Autor | java.lang.String |  |
| dateTime | java.util.Date |  |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) |  |

### compare(String v1, String v2, String outputFileName, SaveOptions saveOptions, String author, Date dateTime) {#compare-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.util.Date}
```
public static void compare(String v1, String v2, String outputFileName, SaveOptions saveOptions, String author, Date dateTime)
```


Vergleicht zwei Dokumente mit zusätzlichen Optionen und speichert die Unterschiede in die angegebene Ausgabedatei im bereitgestellten Speicherformat, wobei Änderungen als eine Reihe von Bearbeitungs‑ und Formatierungsrevisionen erzeugt werden.

 **Remarks:** 

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel zu erzeugen: outputFile\_partIndex.extension.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne mehrseitige TIFF-Datei gespeichert.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | java.lang.String | Das ursprüngliche Dokument. |
| v2 | java.lang.String | Das geänderte Dokument. |
| outputFileName | java.lang.String | Der Ausgabedateiname. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Die Speicheroptionen der Ausgabe. |
| Autor | java.lang.String | Initialen des Autors, die für Revisionen verwendet werden. |
| dateTime | java.util.Date | Datum und Uhrzeit, die für Revisionen verwendet werden. |

### compare(String v1, String v2, String outputFileName, SaveOptions saveOptions, String author, Date dateTime, CompareOptions compareOptions) {#compare-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static void compare(String v1, String v2, String outputFileName, SaveOptions saveOptions, String author, Date dateTime, CompareOptions compareOptions)
```


Vergleicht zwei Dokumente mit zusätzlichen Optionen und speichert die Unterschiede in die angegebene Ausgabedatei im bereitgestellten Speicherformat, wobei Änderungen als eine Reihe von Bearbeitungs‑ und Formatierungsrevisionen erzeugt werden.

 **Remarks:** 

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel zu erzeugen: outputFile\_partIndex.extension.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne mehrseitige TIFF-Datei gespeichert.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | java.lang.String | Das ursprüngliche Dokument. |
| v2 | java.lang.String | Das geänderte Dokument. |
| outputFileName | java.lang.String | Der Ausgabedateiname. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Die Speicheroptionen der Ausgabe. |
| Autor | java.lang.String | Initialen des Autors, die für Revisionen verwendet werden. |
| dateTime | java.util.Date | Datum und Uhrzeit, die für Revisionen verwendet werden. |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) | Optionen für den Dokumentvergleich. |

### compare(String v1, String v2, String outputFileName, int saveFormat, String author, Date dateTime) {#compare-java.lang.String-java.lang.String-java.lang.String-int-java.lang.String-java.util.Date}
```
public static void compare(String v1, String v2, String outputFileName, int saveFormat, String author, Date dateTime)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | java.lang.String |  |
| v2 | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| Autor | java.lang.String |  |
| dateTime | java.util.Date |  |

### compare(String v1, String v2, String outputFileName, int saveFormat, String author, Date dateTime, CompareOptions compareOptions) {#compare-java.lang.String-java.lang.String-java.lang.String-int-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static void compare(String v1, String v2, String outputFileName, int saveFormat, String author, Date dateTime, CompareOptions compareOptions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | java.lang.String |  |
| v2 | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| Autor | java.lang.String |  |
| dateTime | java.util.Date |  |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) |  |

### compare(String v1, String v2, String outputFileName, String author, Date dateTime) {#compare-java.lang.String-java.lang.String-java.lang.String-java.lang.String-java.util.Date}
```
public static void compare(String v1, String v2, String outputFileName, String author, Date dateTime)
```


Vergleicht zwei Dokumente mit zusätzlichen Optionen und speichert die Unterschiede in die angegebene Ausgabedatei, wobei Änderungen als eine Reihe von Bearbeitungs‑ und Formatierungsrevisionen erzeugt werden.

 **Remarks:** 

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel zu erzeugen: outputFile\_partIndex.extension.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne mehrseitige TIFF-Datei gespeichert.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | java.lang.String | Das ursprüngliche Dokument. |
| v2 | java.lang.String | Das geänderte Dokument. |
| outputFileName | java.lang.String | Der Ausgabedateiname. |
| Autor | java.lang.String | Initialen des Autors, die für Revisionen verwendet werden. |
| dateTime | java.util.Date | Datum und Uhrzeit, die für Revisionen verwendet werden. |

### compare(String v1, String v2, String outputFileName, String author, Date dateTime, CompareOptions compareOptions) {#compare-java.lang.String-java.lang.String-java.lang.String-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static void compare(String v1, String v2, String outputFileName, String author, Date dateTime, CompareOptions compareOptions)
```


Vergleicht zwei Dokumente mit zusätzlichen Optionen und speichert die Unterschiede in die angegebene Ausgabedatei, wobei Änderungen als eine Reihe von Bearbeitungs‑ und Formatierungsrevisionen erzeugt werden.

 **Remarks:** 

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel zu erzeugen: outputFile\_partIndex.extension.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne mehrseitige TIFF-Datei gespeichert.

 **Examples:** 

Zeigt, wie man Dokumente einfach vergleicht.

```

 // There is a several ways to compare documents:
 String firstDoc = getMyDir() + "Table column bookmarks.docx";
 String secondDoc = getMyDir() + "Table column bookmarks.doc";

 Comparer.compare(firstDoc, secondDoc, getArtifactsDir() + "LowCode.CompareDocuments.1.docx", "Author", new Date());
 Comparer.compare(firstDoc, secondDoc, getArtifactsDir() + "LowCode.CompareDocuments.2.docx", SaveFormat.DOCX, "Author", new Date());
 CompareOptions options = new CompareOptions();
 options.setIgnoreCaseChanges(true);
 Comparer.compare(firstDoc, secondDoc, getArtifactsDir() + "LowCode.CompareDocuments.3.docx", "Author", new Date(), options);
 Comparer.compare(firstDoc, secondDoc, getArtifactsDir() + "LowCode.CompareDocuments.4.docx", SaveFormat.DOCX, "Author", new Date(), options);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | java.lang.String | Das ursprüngliche Dokument. |
| v2 | java.lang.String | Das geänderte Dokument. |
| outputFileName | java.lang.String | Der Ausgabedateiname. |
| Autor | java.lang.String | Initialen des Autors, die für Revisionen verwendet werden. |
| dateTime | java.util.Date | Datum und Uhrzeit, die für Revisionen verwendet werden. |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) | Optionen für den Dokumentvergleich. |

### compareToImages(InputStream v1, InputStream v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime) {#compareToImages-java.io.InputStream-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date}
```
public static OutputStream[] compareToImages(InputStream v1, InputStream v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime)
```


Vergleicht zwei Dokumente und speichert die Unterschiede als Bilder. Jeder Eintrag im zurückgegebenen Array stellt eine einzelne Seite der Ausgabe dar, die als Bild gerendert wird.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | java.io.InputStream | Das ursprüngliche Dokument. |
| v2 | java.io.InputStream | Das geänderte Dokument. |
| imageSaveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Bildspeicheroptionen der Ausgabe. |
| Autor | java.lang.String | Initialen des Autors, die für Revisionen verwendet werden. |
| dateTime | java.util.Date | Datum und Uhrzeit, die für Revisionen verwendet werden. |

**Returns:**
java.io.OutputStream[]
### compareToImages(InputStream v1, InputStream v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime, CompareOptions compareOptions) {#compareToImages-java.io.InputStream-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static OutputStream[] compareToImages(InputStream v1, InputStream v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime, CompareOptions compareOptions)
```


Vergleicht zwei Dokumente und speichert die Unterschiede als Bilder. Jeder Eintrag im zurückgegebenen Array stellt eine einzelne Seite der Ausgabe dar, die als Bild gerendert wird.

 **Examples:** 

Zeigt, wie man Dokumente vergleicht und Ergebnisse als Bilder speichert.

```

 // There is a several ways to compare documents:
 String firstDoc = getMyDir() + "Table column bookmarks.docx";
 String secondDoc = getMyDir() + "Table column bookmarks.doc";

 OutputStream[] pages = Comparer.compareToImages(firstDoc, secondDoc, new ImageSaveOptions(SaveFormat.PNG), "Author", new Date());

 try (FileInputStream firstStreamIn = new FileInputStream(firstDoc)) {
     try (FileInputStream secondStreamIn = new FileInputStream(secondDoc)) {
         CompareOptions compareOptions = new CompareOptions();
         compareOptions.setIgnoreCaseChanges(true);
         pages = Comparer.compareToImages(firstStreamIn, secondStreamIn, new ImageSaveOptions(SaveFormat.PNG), "Author", new Date(), compareOptions);
     }
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | java.io.InputStream | Das ursprüngliche Dokument. |
| v2 | java.io.InputStream | Das geänderte Dokument. |
| imageSaveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Bildspeicheroptionen der Ausgabe. |
| Autor | java.lang.String | Initialen des Autors, die für Revisionen verwendet werden. |
| dateTime | java.util.Date | Datum und Uhrzeit, die für Revisionen verwendet werden. |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) | Optionen für den Dokumentvergleich. |

**Returns:**
java.io.OutputStream[]
### compareToImages(String v1, String v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime) {#compareToImages-java.lang.String-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date}
```
public static OutputStream[] compareToImages(String v1, String v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime)
```


Vergleicht zwei Dokumente und speichert die Unterschiede als Bilder. Jeder Eintrag im zurückgegebenen Array stellt eine einzelne Seite der Ausgabe dar, die als Bild gerendert wird.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | java.lang.String | Das ursprüngliche Dokument. |
| v2 | java.lang.String | Das geänderte Dokument. |
| imageSaveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Bildspeicheroptionen der Ausgabe. |
| Autor | java.lang.String | Initialen des Autors, die für Revisionen verwendet werden. |
| dateTime | java.util.Date | Datum und Uhrzeit, die für Revisionen verwendet werden. |

**Returns:**
java.io.OutputStream[]
### compareToImages(String v1, String v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime, CompareOptions compareOptions) {#compareToImages-java.lang.String-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static OutputStream[] compareToImages(String v1, String v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime, CompareOptions compareOptions)
```


Vergleicht zwei Dokumente und speichert die Unterschiede als Bilder. Jeder Eintrag im zurückgegebenen Array stellt eine einzelne Seite der Ausgabe dar, die als Bild gerendert wird.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | java.lang.String | Das ursprüngliche Dokument. |
| v2 | java.lang.String | Das geänderte Dokument. |
| imageSaveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Bildspeicheroptionen der Ausgabe. |
| Autor | java.lang.String | Initialen des Autors, die für Revisionen verwendet werden. |
| dateTime | java.util.Date | Datum und Uhrzeit, die für Revisionen verwendet werden. |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) | Optionen für den Dokumentvergleich. |

**Returns:**
java.io.OutputStream[]
### create() {#create}
```
public static Comparer create()
```


Erstellt eine neue Instanz des Converter‑Prozessors.

**Returns:**
[Comparer](../../com.aspose.words/comparer/)
### create(ComparerContext context) {#create-com.aspose.words.ComparerContext}
```
public static Comparer create(ComparerContext context)
```


Erstellt eine neue Instanz des Comparer‑Prozessors.

 **Examples:** 

Zeigt, wie man Dokumente einfach mithilfe von Kontext vergleicht.

```

 // There is a several ways to compare documents:
 String firstDoc = getMyDir() + "Table column bookmarks.docx";
 String secondDoc = getMyDir() + "Table column bookmarks.doc";

 ComparerContext comparerContext = new ComparerContext();
 comparerContext.getCompareOptions().setIgnoreCaseChanges(true);
 comparerContext.setAuthor("Author");
 comparerContext.setDateTime(new Date());

 Comparer.create(comparerContext)
         .from(firstDoc)
         .from(secondDoc)
         .to(getArtifactsDir() + "LowCode.CompareContextDocuments.docx")
         .execute();
 
```

Zeigt, wie man Dokumente aus dem Stream mithilfe von Kontext vergleicht.

```

 // There is a several ways to compare documents from the stream:
 try (FileInputStream firstStreamIn = new FileInputStream(getMyDir() + "Table column bookmarks.docx")) {
     try (FileInputStream secondStreamIn = new FileInputStream(getMyDir() + "Table column bookmarks.doc")) {
         ComparerContext comparerContext = new ComparerContext();
         comparerContext.getCompareOptions().setIgnoreCaseChanges(true);
         comparerContext.setAuthor("Author");
         comparerContext.setDateTime(new Date());

         try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.CompareContextStreamDocuments.docx")) {
             Comparer.create(comparerContext)
                     .from(firstStreamIn)
                     .from(secondStreamIn)
                     .to(streamOut, SaveFormat.DOCX)
                     .execute();
         }
     }
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| context | [ComparerContext](../../com.aspose.words/comparercontext/) |  |

**Returns:**
[Comparer](../../com.aspose.words/comparer/)
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
