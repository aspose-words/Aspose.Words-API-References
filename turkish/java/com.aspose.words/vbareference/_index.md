---
title: "VbaReference"
linktitle: "VbaReference"
second_title: "Aspose.Words Java için"
description: "Java'da bir Automation tür kitaplığına veya VBA projesine referans uygular."
type: docs
weight: 710
url: /tr/java/com.aspose.words/vbareference/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public abstract class VbaReference implements Cloneable
```

Bir Automation tip kitaplığına veya VBA projesine referans uygular.

Daha fazla bilgi için, [ Working with VBA Macros ][Working with VBA Macros] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

VBA referans koleksiyonundan bir elemanı almayı/kaldırmayı nasıl yapacağınızı gösterir.

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
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [VbaReference()](#VbaReference) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getLibId()](#getLibId) | Automation tür kitaplığının tanımlayıcısını içeren bir dize değeri alır. |
| [getType()](#getType) | [VbaReference](../../com.aspose.words/vbareference/) nesnesinin temsil ettiği referans türünü gösteren bir [VbaReferenceType](../../com.aspose.words/vbareferencetype/) nesnesi alır. |
### VbaReference() {#VbaReference}
```
public VbaReference()
```


### getLibId() {#getLibId}
```
public abstract String getLibId()
```


Automation tür kitaplığının tanımlayıcısını içeren bir dize değeri alır.

 **Remarks:** 

Referans türüne bağlı olarak, bu özelliğin değeri şunlar olabilir:

 *  a LibidReference specified at 2.1.1.8 LibidReference of [MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office\_file\_formats/ms-ovba/3737ef6e-d819-4186-a5f2-6e258ddf66a5
 *  a ProjectReference specified at 2.1.1.12 ProjectReference of [MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office\_file\_formats/ms-ovba/9a45ac1a-f1ff-4ebd-958e-537701aa8131

 **Examples:** 

VBA referans koleksiyonundan bir elemanı almayı/kaldırmayı nasıl yapacağınızı gösterir.

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
java.lang.String - Automation tür kitaplığının tanımlayıcısını içeren bir dize değeri.
### getType() {#getType}
```
public abstract int getType()
```


[VbaReference](../../com.aspose.words/vbareference/) nesnesinin temsil ettiği referans türünü gösteren bir [VbaReferenceType](../../com.aspose.words/vbareferencetype/) nesnesi alır.

 **Examples:** 

VBA referans koleksiyonundan bir elemanı almayı/kaldırmayı nasıl yapacağınızı gösterir.

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
int - [VbaReferenceType](../../com.aspose.words/vbareferencetype/) nesnesi, bir [VbaReference](../../com.aspose.words/vbareference/) nesnesinin temsil ettiği referans türünü gösterir. Döndürülen değer, [VbaReferenceType](../../com.aspose.words/vbareferencetype/) sabitlerinden biridir.
