---
title: "VbaReferenceType"
linktitle: "VbaReferenceType"
second_title: "Aspose.Words pour Java"
description: "Permet de spécifier le type d'un objet VbaReference en Java."
type: docs
weight: 712
url: /fr/java/com.aspose.words/vbareferencetype/
---

**Inheritance:**
java.lang.Object
```
public class VbaReferenceType
```

Permet de spécifier le type d'un objet [VbaReference](../../com.aspose.words/vbareference/).

 **Examples:** 

Montre comment obtenir/supprimer un élément de la collection de références VBA.

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
## Champs

| Champ | Description |
| --- | --- |
| [CONTROL](#CONTROL) | Spécifie un type de référence de bibliothèque de types modifié. |
| [ORIGINAL](#ORIGINAL) | Spécifie un type de référence de bibliothèque de types Automation original. |
| [PROJECT](#PROJECT) | Spécifie un type de référence de projet VBA externe. |
| [REGISTERED](#REGISTERED) | Spécifie un type de référence de bibliothèque de types Automation. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String vbaReferenceTypeName)](#fromName-java.lang.String) |  |
| [getName(int vbaReferenceType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int vbaReferenceType)](#toString-int) |  |
### CONTROL {#CONTROL}
```
public static int CONTROL
```


Spécifie un type de référence de bibliothèque de types modifié.

 **Remarks:** 

Ce type correspond à l'enregistrement REFERENCECONTROL 2.3.4.2.2.3 du [MS-OVBA] : https://docs.microsoft.com/en-us/openspecs/office\_file\_formats/ms-ovba/d64485fa-8562-4726-9c5e-11e8f01a81c0

### ORIGINAL {#ORIGINAL}
```
public static int ORIGINAL
```


Spécifie un type de référence de bibliothèque de types Automation original.

 **Remarks:** 

Ce type correspond à l'enregistrement REFERENCEORIGINAL 2.3.4.2.2.4 du [MS-OVBA] : https://docs.microsoft.com/en-us/openspecs/office\_file\_formats/ms-ovba/3ba66994-8c7a-4634-b2da-f9331ace6686

### PROJECT {#PROJECT}
```
public static int PROJECT
```


Spécifie un type de référence de projet VBA externe.

 **Remarks:** 

Ce type correspond à l'enregistrement REFERENCEPROJECT 2.3.4.2.2.6 de [MS-OVBA] : https://docs.microsoft.com/en-us/openspecs/office\\_file\\_formats/ms-ovba/08280eb0-d628-495c-867f-5985ed020142

### REGISTERED {#REGISTERED}
```
public static int REGISTERED
```


Spécifie un type de référence de bibliothèque de types Automation.

 **Remarks:** 

Ce type correspond à l'enregistrement REFERENCEREGISTERED 2.3.4.2.2.5 de [MS-OVBA] : https://docs.microsoft.com/en-us/openspecs/office\\_file\\_formats/ms-ovba/6c39388e-96f5-4b93-b90a-ae625a063fcf

### length {#length}
```
public static int length
```


### fromName(String vbaReferenceTypeName) {#fromName-java.lang.String}
```
public static int fromName(String vbaReferenceTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| vbaReferenceTypeName | java.lang.String |  |

**Returns:**
int
### getName(int vbaReferenceType) {#getName-int}
```
public static String getName(int vbaReferenceType)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| vbaReferenceType | int |  |

**Returns:**
java.lang.String
