---
title: "VbaReference"
linktitle: "VbaReference"
second_title: "Aspose.Words für Java"
description: "Implementiert eine Referenz auf eine Automation-Typbibliothek oder ein VBA-Projekt in Java."
type: docs
weight: 710
url: /de/java/com.aspose.words/vbareference/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public abstract class VbaReference implements Cloneable
```

Implementiert eine Referenz auf eine Automation-Typbibliothek oder ein VBA-Projekt.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Working with VBA Macros ][Working with VBA Macros].

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


[Working with VBA Macros]: https://docs.aspose.com/words/java/working-with-vba-macros/
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [VbaReference()](#VbaReference) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getLibId()](#getLibId) | Gibt einen Zeichenkettenwert zurück, der den Bezeichner einer Automation-Typbibliothek enthält. |
| [getType()](#getType) | Gibt ein [VbaReferenceType](../../com.aspose.words/vbareferencetype/)-Objekt zurück, das den Referenztyp angibt, den ein [VbaReference](../../com.aspose.words/vbareference/)-Objekt darstellt. |
### VbaReference() {#VbaReference}
```
public VbaReference()
```


### getLibId() {#getLibId}
```
public abstract String getLibId()
```


Gibt einen Zeichenkettenwert zurück, der den Bezeichner einer Automation-Typbibliothek enthält.

 **Remarks:** 

Abhängig vom Referenztyp kann der Wert dieser Eigenschaft sein:

 *  a LibidReference specified at 2.1.1.8 LibidReference of [MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office\_file\_formats/ms-ovba/3737ef6e-d819-4186-a5f2-6e258ddf66a5
 *  a ProjectReference specified at 2.1.1.12 ProjectReference of [MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office\_file\_formats/ms-ovba/9a45ac1a-f1ff-4ebd-958e-537701aa8131

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

**Returns:**
java.lang.String – Ein Zeichenkettenwert, der den Bezeichner einer Automation-Typbibliothek enthält.
### getType() {#getType}
```
public abstract int getType()
```


Gibt ein [VbaReferenceType](../../com.aspose.words/vbareferencetype/)-Objekt zurück, das den Referenztyp angibt, den ein [VbaReference](../../com.aspose.words/vbareference/)-Objekt darstellt.

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

**Returns:**
int – Ein [VbaReferenceType](../../com.aspose.words/vbareferencetype/)-Objekt, das den Referenztyp angibt, den ein [VbaReference](../../com.aspose.words/vbareference/)-Objekt darstellt. Der zurückgegebene Wert ist einer der [VbaReferenceType](../../com.aspose.words/vbareferencetype/) Konstanten.
