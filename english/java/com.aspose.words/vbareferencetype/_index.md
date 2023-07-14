---
title: VbaReferenceType
linktitle: VbaReferenceType
second_title: Aspose.Words for Java
description: Allows to specify the type of a VbaReference object in Java.
type: docs
weight: 623
url: /java/com.aspose.words/vbareferencetype/
---

**Inheritance:**
java.lang.Object
```
public class VbaReferenceType
```

Allows to specify the type of a [VbaReference](../../com.aspose.words/vbareference/) object.

 **Examples:** 

Shows how to get/remove an element from the VBA reference collection.

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
## Fields

| Field | Description |
| --- | --- |
| [CONTROL](#CONTROL) | Specifies a twiddled type library reference type. |
| [ORIGINAL](#ORIGINAL) | Specifies an original Automation type library reference type. |
| [PROJECT](#PROJECT) | Specified an external VBA project reference type. |
| [REGISTERED](#REGISTERED) | Specifies an Automation type library reference type. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String vbaReferenceTypeName)](#fromName-java.lang.String) |  |
| [getName(int vbaReferenceType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int vbaReferenceType)](#toString-int) |  |
### CONTROL {#CONTROL}
```
public static int CONTROL
```


Specifies a twiddled type library reference type.

 **Remarks:** 

This type corresponds to 2.3.4.2.2.3 REFERENCECONTROL Record of [MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office\_file\_formats/ms-ovba/d64485fa-8562-4726-9c5e-11e8f01a81c0

### ORIGINAL {#ORIGINAL}
```
public static int ORIGINAL
```


Specifies an original Automation type library reference type.

 **Remarks:** 

This type corresponds to 2.3.4.2.2.4 REFERENCEORIGINAL Record of [MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office\_file\_formats/ms-ovba/3ba66994-8c7a-4634-b2da-f9331ace6686

### PROJECT {#PROJECT}
```
public static int PROJECT
```


Specified an external VBA project reference type.

 **Remarks:** 

This type corresponds to 2.3.4.2.2.6 REFERENCEPROJECT Record of [MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office\_file\_formats/ms-ovba/08280eb0-d628-495c-867f-5985ed020142

### REGISTERED {#REGISTERED}
```
public static int REGISTERED
```


Specifies an Automation type library reference type.

 **Remarks:** 

This type corresponds to 2.3.4.2.2.5 REFERENCEREGISTERED Record of [MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office\_file\_formats/ms-ovba/6c39388e-96f5-4b93-b90a-ae625a063fcf

### length {#length}
```
public static int length
```


### fromName(String vbaReferenceTypeName) {#fromName-java.lang.String}
```
public static int fromName(String vbaReferenceTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| vbaReferenceTypeName | java.lang.String |  |

**Returns:**
int
### getName(int vbaReferenceType) {#getName-int}
```
public static String getName(int vbaReferenceType)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| vbaReferenceType | int |  |

**Returns:**
java.lang.String
