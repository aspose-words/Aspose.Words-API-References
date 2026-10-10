---
title: "PdfPermissions"
linktitle: "PdfPermissions"
second_title: "Aspose.Words für Java"
description: "Gibt die Vorgänge an, die einem Benutzer an einem verschlüsselten PDF-Dokument in Java erlaubt sind."
type: docs
weight: 541
url: /de/java/com.aspose.words/pdfpermissions/
---

**Inheritance:**
java.lang.Object
```
public class PdfPermissions
```

Gibt die Vorgänge an, die einem Benutzer bei einem verschlüsselten PDF-Dokument erlaubt sind.

 **Examples:** 

Zeigt, wie Berechtigungen für ein gespeichertes PDF-Dokument festgelegt werden.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [ALLOW_ALL](#ALLOW-ALL) | Erlaubt alle Vorgänge am PDF-Dokument. |
| [CONTENT_COPY](#CONTENT-COPY) | Kopieren oder anderweitiges Extrahieren von Text und Grafiken aus dem Dokument durch Vorgänge, die nicht von [CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions/\#CONTENT-COPY-FOR-ACCESSIBILITY) gesteuert werden. |
| [CONTENT_COPY_FOR_ACCESSIBILITY](#CONTENT-COPY-FOR-ACCESSIBILITY) | Extrahieren von Text und Grafiken (zur Unterstützung der Barrierefreiheit für Benutzer mit Behinderungen oder zu anderen Zwecken). |
| [DISALLOW_ALL](#DISALLOW-ALL) | Verweigert alle Vorgänge am PDF-Dokument. |
| [DOCUMENT_ASSEMBLY](#DOCUMENT-ASSEMBLY) | Zusammenstellen des Dokuments (Einfügen, Drehen oder Löschen von Seiten und Erstellen von Dokumentenübersichts‑Einträgen oder Vorschaubildern), selbst wenn [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) deaktiviert ist. |
| [FILL_IN](#FILL-IN) | Ausfüllen vorhandener interaktiver Formularfelder (einschließlich Signaturfelder), selbst wenn [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) deaktiviert ist. |
| [HIGH_RESOLUTION_PRINTING](#HIGH-RESOLUTION-PRINTING) | Drucken des Dokuments zu einer Darstellung, aus der eine getreue digitale Kopie des PDF-Inhalts erzeugt werden kann, basierend auf einem implementierungsabhängigen Algorithmus. |
| [MODIFY_ANNOTATIONS](#MODIFY-ANNOTATIONS) | Hinzufügen oder Ändern von Textanmerkungen, Ausfüllen interaktiver Formularfelder und, falls [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) ebenfalls gesetzt ist, Erstellen oder Ändern interaktiver Formularfelder (einschließlich Signaturfelder). |
| [MODIFY_CONTENTS](#MODIFY-CONTENTS) | Ändern des Inhalts des Dokuments durch Vorgänge, die nicht von [MODIFY\_ANNOTATIONS](../../com.aspose.words/pdfpermissions/\#MODIFY-ANNOTATIONS), [FILL\_IN](../../com.aspose.words/pdfpermissions/\#FILL-IN) und [DOCUMENT\_ASSEMBLY](../../com.aspose.words/pdfpermissions/\#DOCUMENT-ASSEMBLY) gesteuert werden. |
| [PRINTING](#PRINTING) | Drucken des Dokuments (möglicherweise nicht in höchster Qualität, abhängig davon, ob [HIGH\_RESOLUTION\_PRINTING](../../com.aspose.words/pdfpermissions/\#HIGH-RESOLUTION-PRINTING) ebenfalls gesetzt ist). |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String pdfPermissionsName)](#fromName-java.lang.String) |  |
| [fromNames(Set pdfPermissionsNames)](#fromNames-java.util.Set) |  |
| [getName(int pdfPermissions)](#getName-int) |  |
| [getNames(int pdfPermissions)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfPermissions)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### ALLOW_ALL {#ALLOW-ALL}
```
public static int ALLOW_ALL
```


Erlaubt alle Vorgänge am PDF-Dokument.

### CONTENT_COPY {#CONTENT-COPY}
```
public static int CONTENT_COPY
```


Kopieren oder anderweitiges Extrahieren von Text und Grafiken aus dem Dokument durch Vorgänge, die nicht von [CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions/\#CONTENT-COPY-FOR-ACCESSIBILITY) gesteuert werden.

### CONTENT_COPY_FOR_ACCESSIBILITY {#CONTENT-COPY-FOR-ACCESSIBILITY}
```
public static int CONTENT_COPY_FOR_ACCESSIBILITY
```


Extrahieren von Text und Grafiken (zur Unterstützung der Barrierefreiheit für Benutzer mit Behinderungen oder zu anderen Zwecken).

### DISALLOW_ALL {#DISALLOW-ALL}
```
public static int DISALLOW_ALL
```


Verweigert alle Vorgänge am PDF-Dokument. Dies ist der Standardwert.

### DOCUMENT_ASSEMBLY {#DOCUMENT-ASSEMBLY}
```
public static int DOCUMENT_ASSEMBLY
```


Zusammenstellen des Dokuments (Einfügen, Drehen oder Löschen von Seiten und Erstellen von Dokumentenübersichts‑Einträgen oder Vorschaubildern), selbst wenn [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) deaktiviert ist.

### FILL_IN {#FILL-IN}
```
public static int FILL_IN
```


Ausfüllen vorhandener interaktiver Formularfelder (einschließlich Signaturfelder), selbst wenn [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) deaktiviert ist.

### HIGH_RESOLUTION_PRINTING {#HIGH-RESOLUTION-PRINTING}
```
public static int HIGH_RESOLUTION_PRINTING
```


Drucken des Dokuments zu einer Darstellung, aus der eine getreue digitale Kopie des PDF-Inhalts erzeugt werden kann, basierend auf einem implementierungsabhängigen Algorithmus. Wenn dieses Flag deaktiviert ist (und [PRINTING](../../com.aspose.words/pdfpermissions/\#PRINTING) gesetzt ist), soll das Drucken auf eine niedrigstufige Darstellung des Erscheinungsbildes beschränkt werden, möglicherweise von verminderter Qualität.

### MODIFY_ANNOTATIONS {#MODIFY-ANNOTATIONS}
```
public static int MODIFY_ANNOTATIONS
```


Hinzufügen oder Ändern von Textanmerkungen, Ausfüllen interaktiver Formularfelder und, falls [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) ebenfalls gesetzt ist, Erstellen oder Ändern interaktiver Formularfelder (einschließlich Signaturfelder).

### MODIFY_CONTENTS {#MODIFY-CONTENTS}
```
public static int MODIFY_CONTENTS
```


Ändern des Inhalts des Dokuments durch Vorgänge, die nicht von [MODIFY\_ANNOTATIONS](../../com.aspose.words/pdfpermissions/\#MODIFY-ANNOTATIONS), [FILL\_IN](../../com.aspose.words/pdfpermissions/\#FILL-IN) und [DOCUMENT\_ASSEMBLY](../../com.aspose.words/pdfpermissions/\#DOCUMENT-ASSEMBLY) gesteuert werden.

### PRINTING {#PRINTING}
```
public static int PRINTING
```


Drucken des Dokuments (möglicherweise nicht in höchster Qualität, abhängig davon, ob [HIGH\_RESOLUTION\_PRINTING](../../com.aspose.words/pdfpermissions/\#HIGH-RESOLUTION-PRINTING) ebenfalls gesetzt ist).

### length {#length}
```
public static int length
```


### fromName(String pdfPermissionsName) {#fromName-java.lang.String}
```
public static int fromName(String pdfPermissionsName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pdfPermissionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set pdfPermissionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set pdfPermissionsNames)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pdfPermissionsNames | java.util.Set |  |

**Returns:**
int
### getName(int pdfPermissions) {#getName-int}
```
public static String getName(int pdfPermissions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pdfPermissions | int |  |

**Returns:**
java.lang.String
### getNames(int pdfPermissions) {#getNames-int}
```
public static Set getNames(int pdfPermissions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pdfPermissions | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfPermissions) {#toString-int}
```
public static String toString(int pdfPermissions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pdfPermissions | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
