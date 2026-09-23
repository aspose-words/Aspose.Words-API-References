---
title: "VbaReferenceType"
linktitle: "VbaReferenceType"
second_title: "Aspose.Words für Java"
description: "Ermöglicht die Angabe des Typs eines VbaReference-Objekts in Java."
type: docs
weight: 712
url: /de/java/com.aspose.words/vbareferencetype/
---

**Inheritance:**
java.lang.Object
```
public class VbaReferenceType
```

Ermöglicht die Angabe des Typs eines [VbaReference](../../com.aspose.words/vbareference/) Objekts.

 **Examples:** 

Zeigt, wie man ein Element aus der VBA-Referenzsammlung abruft/entfernt.

```

 public void removeVbaReference() throws Exception {
     final String BROKEN_PATH = "X:\\broken.dll";
     Document doc = new Document(getMyDir() + "VBA project.docm");

     VbaReferenceCollection references = doc.getVbaProject().getReferences();
     Assert.assertEquals(5, references.getCount());

     for (int i = references.getCount() - 1; i >= 0; i--) {
         VbaReference reference = doc.getVbaProject().getReferences().get(i);
         String path = getLibIdPath(reference);

         if (BROKEN_PATH.equals(path))
             references.removeAt(i);
     }
     Assert.assertEquals(4, references.getCount());

     references.remove(references.get(1));
     Assert.assertEquals(3, references.getCount());

     doc.save(getArtifactsDir() + "VbaProject.RemoveVbaReference.docm");
 }

 /// 
 /// Returns string representing LibId path of a specified reference.
 /// 
 private static String getLibIdPath(VbaReference reference) {
     switch (reference.getType()) {
         case VbaReferenceType.REGISTERED:
         case VbaReferenceType.ORIGINAL:
         case VbaReferenceType.CONTROL:
             return getLibIdReferencePath(reference.getLibId());
         case VbaReferenceType.PROJECT:
             return getLibIdProjectPath(reference.getLibId());
         default:
             throw new IllegalArgumentException();
     }
 }

 /// 
 /// Returns path from a specified identifier of an Automation type library.
 /// 
 private static String getLibIdReferencePath(String libIdReference) {
     if (libIdReference != null) {
         String[] refParts = libIdReference.split("#");
         if (refParts.length > 3)
             return refParts[3];
     }

     return "";
 }

 /// 
 /// Returns path from a specified identifier of an Automation type library.
 /// 
 private static String getLibIdProjectPath(String libIdProject) {
     return libIdProject != null ? libIdProject.substring(3) : "";
 }
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [CONTROL](#CONTROL) | Gibt einen manipulierten Typbibliotheksreferenztyp an. |
| [ORIGINAL](#ORIGINAL) | Gibt einen ursprünglichen Automation-Typbibliotheksreferenztyp an. |
| [PROJECT](#PROJECT) | Gibt einen externen VBA-Projektreferenztyp an. |
| [REGISTERED](#REGISTERED) | Gibt einen Automation-Typbibliotheksreferenztyp an. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String vbaReferenceTypeName)](#fromName-java.lang.String) |  |
| [getName(int vbaReferenceType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int vbaReferenceType)](#toString-int) |  |
### CONTROL {#CONTROL}
```
public static int CONTROL
```


Gibt einen manipulierten Typbibliotheksreferenztyp an.

 **Remarks:** 

Dieser Typ entspricht dem REFERENCECONTROL-Eintrag 2.3.4.2.2.3 von [MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office\_file\_formats/ms-ovba/d64485fa-8562-4726-9c5e-11e8f01a81c0

### ORIGINAL {#ORIGINAL}
```
public static int ORIGINAL
```


Gibt einen ursprünglichen Automation-Typbibliotheksreferenztyp an.

 **Remarks:** 

Dieser Typ entspricht dem 2.3.4.2.2.4 REFERENCEORIGINAL Record von [MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office\_file\_formats/ms-ovba/3ba66994-8c7a-4634-b2da-f9331ace6686

### PROJECT {#PROJECT}
```
public static int PROJECT
```


Gibt einen externen VBA-Projektreferenztyp an.

 **Remarks:** 

Dieser Typ entspricht dem 2.3.4.2.2.6 REFERENCEPROJECT Record von [MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office\_file\_formats/ms-ovba/08280eb0-d628-495c-867f-5985ed020142

### REGISTERED {#REGISTERED}
```
public static int REGISTERED
```


Gibt einen Automation-Typbibliotheksreferenztyp an.

 **Remarks:** 

Dieser Typ entspricht dem 2.3.4.2.2.5 REFERENCEREGISTERED Record von [MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office\_file\_formats/ms-ovba/6c39388e-96f5-4b93-b90a-ae625a063fcf

### length {#length}
```
public static int length
```


### fromName(String vbaReferenceTypeName) {#fromName-java.lang.String}
```
public static int fromName(String vbaReferenceTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| vbaReferenceTypeName | java.lang.String |  |

**Returns:**
int
### getName(int vbaReferenceType) {#getName-int}
```
public static String getName(int vbaReferenceType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| vbaReferenceType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int vbaReferenceType) {#toString-int}
```
public static String toString(int vbaReferenceType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| vbaReferenceType | int |  |

**Returns:**
java.lang.String
