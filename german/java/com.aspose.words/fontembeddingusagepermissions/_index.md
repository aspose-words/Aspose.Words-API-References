---
title: "FontEmbeddingUsagePermissions"
linktitle: "FontEmbeddingUsagePermissions"
second_title: "Aspose.Words für Java"
description: "Stellt die Berechtigungen für die Schriftart-Einbettung in Java dar."
type: docs
weight: 322
url: /de/java/com.aspose.words/fontembeddingusagepermissions/
---

**Inheritance:**
java.lang.Object
```
public class FontEmbeddingUsagePermissions
```

Stellt die Nutzungsberechtigungen für die Schrift‑Einbettung dar.

 **Examples:** 

Zeigt, wie man Lizenzrechtsinformationen für eingebettete Schriftarten (FontInfo) abruft.

```

 Document doc = new Document(getMyDir() + "Embedded font rights.docx");

 // Get the list of document fonts.
 FontInfoCollection fontInfos = doc.getFontInfos();
 for (FontInfo fontInfo : fontInfos)
 {
     if (fontInfo.getEmbeddingLicensingRights() != null)
     {
         System.out.println(fontInfo.getEmbeddingLicensingRights().getEmbeddingUsagePermissions());
         System.out.println(fontInfo.getEmbeddingLicensingRights().getBitmapEmbeddingOnly());
         System.out.println(fontInfo.getEmbeddingLicensingRights().getNoSubsetting());
     }
 }
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [EDITABLE](#EDITABLE) | Die Schriftart kann eingebettet werden und temporär auf anderen Systemen geladen werden. |
| [INSTALLABLE](#INSTALLABLE) | Die Schriftart kann eingebettet werden und dauerhaft auf entfernten Systemen installiert werden, oder von anderen Benutzern verwendet werden. |
| [PRINT_AND_PREVIEW](#PRINT-AND-PREVIEW) | Die Schriftart kann eingebettet werden und kann vorübergehend auf anderen Systemen geladen werden, um das Dokument anzuzeigen oder zu drucken. |
| [RESTRICTED_LICENSE](#RESTRICTED-LICENSE) | Die Schriftart darf nicht verändert, eingebettet oder ausgetauscht werden, ohne vorher die ausdrückliche Erlaubnis des rechtlichen Eigentümers einzuholen. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String fontEmbeddingUsagePermissionsName)](#fromName-java.lang.String) |  |
| [getName(int fontEmbeddingUsagePermissions)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontEmbeddingUsagePermissions)](#toString-int) |  |
### EDITABLE {#EDITABLE}
```
public static int EDITABLE
```


Die Schriftart kann eingebettet werden und temporär auf anderen Systemen geladen werden.

 **Remarks:** 

Wie beim Einbetten für Vorschau & Druck können Dokumente mit editierbaren Schriftarten zum Lesen geöffnet werden. Zusätzlich ist das Bearbeiten erlaubt, einschließlich der Möglichkeit, neuen Text mit der eingebetteten Schriftart zu formatieren, und Änderungen können gespeichert werden.

### INSTALLABLE {#INSTALLABLE}
```
public static int INSTALLABLE
```


Die Schriftart kann eingebettet werden und dauerhaft auf entfernten Systemen installiert werden, oder von anderen Benutzern verwendet werden.

### PRINT_AND_PREVIEW {#PRINT-AND-PREVIEW}
```
public static int PRINT_AND_PREVIEW
```


Die Schriftart kann eingebettet werden und kann vorübergehend auf anderen Systemen geladen werden, um das Dokument anzuzeigen oder zu drucken.

 **Remarks:** 

Dokumente, die Vorschau & Print‑Schriftarten enthalten, müssen \\u201cNur‑Lese‑Modus\\u201d geöffnet werden; es dürfen keine Änderungen am Dokument vorgenommen werden.

### RESTRICTED_LICENSE {#RESTRICTED-LICENSE}
```
public static int RESTRICTED_LICENSE
```


Die Schriftart darf nicht verändert, eingebettet oder ausgetauscht werden, ohne vorher die ausdrückliche Erlaubnis des rechtlichen Eigentümers einzuholen.

### length {#length}
```
public static int length
```


### fromName(String fontEmbeddingUsagePermissionsName) {#fromName-java.lang.String}
```
public static int fromName(String fontEmbeddingUsagePermissionsName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontEmbeddingUsagePermissionsName | java.lang.String |  |

**Returns:**
int
### getName(int fontEmbeddingUsagePermissions) {#getName-int}
```
public static String getName(int fontEmbeddingUsagePermissions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontEmbeddingUsagePermissions | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int fontEmbeddingUsagePermissions) {#toString-int}
```
public static String toString(int fontEmbeddingUsagePermissions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontEmbeddingUsagePermissions | int |  |

**Returns:**
java.lang.String
