---
title: VbaReference
linktitle: VbaReference
second_title: Aspose.Words for Java
description: Implements a reference to an Automation type library or VBA project in Java.
type: docs
weight: 646
url: /java/com.aspose.words/vbareference/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public abstract class VbaReference implements Cloneable
```

Implements a reference to an Automation type library or VBA project.

To learn more, visit the [ Working with VBA Macros ][Working with VBA Macros] documentation article.

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


[Working with VBA Macros]: https://docs.aspose.com/words/java/working-with-vba-macros/
## Constructors

| Constructor | Description |
| --- | --- |
| [VbaReference()](#VbaReference) |  |
## Methods

| Method | Description |
| --- | --- |
| [getLibId()](#getLibId) | Gets a string value containing the identifier of an Automation type library. |
| [getType()](#getType) | Gets [VbaReferenceType](../../com.aspose.words/vbareferencetype/) object that indicates the type of reference that a [VbaReference](../../com.aspose.words/vbareference/) object represents. |
### VbaReference() {#VbaReference}
```
public VbaReference()
```


### getLibId() {#getLibId}
```
public abstract String getLibId()
```


Gets a string value containing the identifier of an Automation type library.

 **Remarks:** 

Depending on reference type, the value of this property can be:

 *  a LibidReference specified at 2.1.1.8 LibidReference of [MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office\_file\_formats/ms-ovba/3737ef6e-d819-4186-a5f2-6e258ddf66a5
 *  a ProjectReference specified at 2.1.1.12 ProjectReference of [MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office\_file\_formats/ms-ovba/9a45ac1a-f1ff-4ebd-958e-537701aa8131

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

**Returns:**
java.lang.String - A string value containing the identifier of an Automation type library.
### getType() {#getType}
```
public abstract int getType()
```


Gets [VbaReferenceType](../../com.aspose.words/vbareferencetype/) object that indicates the type of reference that a [VbaReference](../../com.aspose.words/vbareference/) object represents.

**Returns:**
int - [VbaReferenceType](../../com.aspose.words/vbareferencetype/) object that indicates the type of reference that a [VbaReference](../../com.aspose.words/vbareference/) object represents. The returned value is one of [VbaReferenceType](../../com.aspose.words/vbareferencetype/) constants.
