---
title: "ImportFormatMode"
linktitle: "ImportFormatMode"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie die Formatierung beim Importieren von Inhalten aus einem anderen Dokument in Java zusammengeführt wird."
type: docs
weight: 400
url: /de/java/com.aspose.words/importformatmode/
---

**Inheritance:**
java.lang.Object
```
public class ImportFormatMode
```

Gibt an, wie Formatierungen beim Importieren von Inhalten aus einem anderen Dokument zusammengeführt werden.

 **Remarks:** 

Wenn Sie Knoten von einem Dokument in ein anderes kopieren, legt diese Option fest, wie die Formatierung aufgelöst wird, wenn beide Dokumente einen Stil mit demselben Namen, aber unterschiedlicher Formatierung besitzen.

Die Formatierung wird wie folgt aufgelöst:

1.  Eingebaute Stile werden anhand ihrer lokalinvarianten Stilkennung abgeglichen. Benutzerdefinierte Stile werden anhand des case‑sensitiven Stilsnamens abgeglichen.
2.  Wenn kein passender Stil im Zieldokument gefunden wird, wird der Stil (und alle von ihm referenzierten Stile) in das Zieldokument kopiert und die importierten Knoten werden aktualisiert, um auf den neuen Stil zu verweisen.
3.  Wenn ein passender Stil bereits im Zieldokument existiert, hängt das Ergebnis vom Parameter  importFormatMode  ab, der an **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** übergeben wird, wie unten beschrieben.

Beim Verwenden der Option [USE\_DESTINATION\_STYLES](../../com.aspose.words/importformatmode/\#USE-DESTINATION-STYLES) wird, wenn ein passender Stil bereits im Zieldokument existiert, der Stil nicht kopiert und die importierten Knoten werden aktualisiert, um auf den vorhandenen Stil zu verweisen.

Der Nachteil der Verwendung von [USE\_DESTINATION\_STYLES](../../com.aspose.words/importformatmode/\#USE-DESTINATION-STYLES) besteht darin, dass der importierte Text im Zieldokument im Vergleich zum Quelldokument anders aussehen kann. Zum Beispiel verwendet der Stil \"Heading 1\" im Quelldokument die Schriftart Arial 16pt und der Stil \"Heading 1\" im Zieldokument die Schriftart Times New Roman 14pt. Beim Importieren von Text im Stil \"Heading 1\" ohne weitere direkte Formatierung wird er im Zieldokument als Times New Roman 14pt angezeigt.

[KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) option allows to make sure the imported content looks the same in the destination document like it looks in the source document. If a matching style already exists in the destination document, the source style formatting is expanded into direct Node attributes and the style is changed to Normal. If the style does not exist in the destination document, then the source style is imported into the destination document and applied to the imported node. Note, that it is not always possible to preserve the source style even if it does not exist in the destination document. In this case formatting of such style will be expanded into direct Node attributes in favor of preserving original Node formatting.

Der Nachteil der Verwendung von [KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) besteht darin, dass bei mehreren Importen viele Stile im Zieldokument entstehen können, was die konsistente Stilformatierung in Microsoft Word für dieses Dokument erschwert.

Die Verwendung der Option [KEEP\_DIFFERENT\_STYLES](../../com.aspose.words/importformatmode/\#KEEP-DIFFERENT-STYLES) ermöglicht die Wiederverwendung von Zieldokument-Stilen, wenn deren Formatierung identisch mit den Stilen im Quelldokument ist. Ist der Stil im Zieldokument jedoch vom Quellstil abweichend, wird er importiert.

 **Examples:** 

Zeigt, wie ein Dokument in ein anderes Dokument eingefügt wird.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.insertBreak(BreakType.PAGE_BREAK);

 Document docToInsert = new Document(getMyDir() + "Formatted elements.docx");

 builder.insertDocument(docToInsert, ImportFormatMode.KEEP_SOURCE_FORMATTING);
 builder.getDocument().save(getArtifactsDir() + "DocumentBuilder.InsertDocument.docx");
 
```

**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**
## Felder

| Feld | Beschreibung |
| --- | --- |
| [KEEP_DIFFERENT_STYLES](#KEEP-DIFFERENT-STYLES) | Nur Stile kopieren, die von denen im Quelldokument abweichen. |
| [KEEP_SOURCE_FORMATTING](#KEEP-SOURCE-FORMATTING) | Kopieren Sie alle erforderlichen Formatvorlagen in das Zieldokument und erzeugen Sie bei Bedarf eindeutige Formatvorlagennamen. |
| [USE_DESTINATION_STYLES](#USE-DESTINATION-STYLES) | Verwenden Sie die Formatvorlagen des Zieldokuments und kopieren Sie neue Formatvorlagen. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String importFormatModeName)](#fromName-java.lang.String) |  |
| [getName(int importFormatMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int importFormatMode)](#toString-int) |  |
### KEEP_DIFFERENT_STYLES {#KEEP-DIFFERENT-STYLES}
```
public static int KEEP_DIFFERENT_STYLES
```


Nur Stile kopieren, die von denen im Quelldokument abweichen.

### KEEP_SOURCE_FORMATTING {#KEEP-SOURCE-FORMATTING}
```
public static int KEEP_SOURCE_FORMATTING
```


Kopieren Sie alle erforderlichen Formatvorlagen in das Zieldokument und erzeugen Sie bei Bedarf eindeutige Formatvorlagennamen.

### USE_DESTINATION_STYLES {#USE-DESTINATION-STYLES}
```
public static int USE_DESTINATION_STYLES
```


Verwenden Sie die Formatvorlagen des Zieldokuments und kopieren Sie neue Formatvorlagen. Dies ist die Standardoption.

### length {#length}
```
public static int length
```


### fromName(String importFormatModeName) {#fromName-java.lang.String}
```
public static int fromName(String importFormatModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| importFormatModeName | java.lang.String |  |

**Returns:**
int
### getName(int importFormatMode) {#getName-int}
```
public static String getName(int importFormatMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| importFormatMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int importFormatMode) {#toString-int}
```
public static String toString(int importFormatMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| importFormatMode | int |  |

**Returns:**
java.lang.String
