---
title: "CustomPart"
linktitle: "CustomPart"
second_title: "Aspose.Words Java için"
description: "Java'da ISO/IEC 29500 standardı tarafından tanımlanmamış özel bir keyfi içerik bölümünü temsil eder."
type: docs
weight: 141
url: /tr/java/com.aspose.words/custompart/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class CustomPart implements Cloneable
```

ISO/IEC 29500 standardı tarafından tanımlanmamış bir özel (keyfi içerik) bölümü temsil eder.

Daha fazla bilgi için, [ Yapılandırılmış Belge Etiketleri veya İçerik Kontrolü ][Yapılandırılmış Belge Etiketleri veya İçerik Kontrolü] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Bu sınıf, bir "bilinmeyen ilişki" hedefi olan bir OOXML bölümünü temsil eder. ISO/IEC 29500 içinde tanımlanmamış tüm ilişkiler "bilinmeyen ilişkiler" olarak kabul edilir. Bilinmeyen ilişkiler, ilişki işaretleme yönergelerine uygun olduğu sürece bir Office Open XML belgesi içinde izin verilir.

Microsoft Word, açma/kaydetme döngüleri sırasında özel bölümleri korur. Burada ek bilgi bulunabilir http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx

Aspose.Words ayrıca özel bölümleri de döngü içinde tutar ve ek olarak, bu bölümlere programlı olarak [CustomPart](../../com.aspose.words/custompart/) ve [CustomPartCollection](../../com.aspose.words/custompartcollection/) nesneleri aracılığıyla erişim sağlar.

Özel bölümleri Custom XML Data ile karıştırmayın. Custom XML Data'ya erişmeniz gerekiyorsa [CustomXmlPart](../../com.aspose.words/customxmlpart/) kullanın.

 **Examples:** 

Bir belgenin keyfi özel bölümler koleksiyonuna nasıl erişileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```


[Structured Document Tags or Content Control]: https://docs.aspose.com/words/java/working-with-content-control-sdt/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [deepClone()](#deepClone) | Nesnenin "deep enough" bir kopyasını oluşturur. |
| [getContentType()](#getContentType) | Bu özel bölümün içerik türünü belirtir. |
| [getData()](#getData) | Bu özel bölümün verilerini içerir. |
| [getName()](#getName) | Bu bölümün OOXML paketindeki mutlak adını veya hedef URL'sini alır. |
| [getRelationshipType()](#getRelationshipType) | Üst bölümden bu özel bölüme olan ilişki türünü alır. |
| [isExternal()](#isExternal) | Bu özel bölüm OOXML paketi içinde depolanıyorsa false. |
| [isExternal(boolean value)](#isExternal-boolean) | Bu özel bölüm OOXML paketi içinde depolanıyorsa false. |
| [setContentType(String value)](#setContentType-java.lang.String) | Bu özel bölümün içerik türünü belirtir. |
| [setData(byte[] value)](#setData-byte) | Bu özel bölümün verilerini içerir. |
| [setName(String value)](#setName-java.lang.String) | Bu bölümün OOXML paketindeki mutlak adını veya hedef URL'sini ayarlar. |
| [setRelationshipType(String value)](#setRelationshipType-java.lang.String) | Üst bölümden bu özel bölüme olan ilişki türünü ayarlar. |
### deepClone() {#deepClone}
```
public CustomPart deepClone()
```


Nesnenin "yeterince derin" bir kopyasını oluşturur. [getData()](../../com.aspose.words/custompart/\#getData) / [setData(byte[])](../../com.aspose.words/custompart/\#setData-byte) değerinin baytlarını çoğaltmaz.

 **Examples:** 

Bir belgenin keyfi özel bölümler koleksiyonuna nasıl erişileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Returns:**
[CustomPart](../../com.aspose.words/custompart/)
### getContentType() {#getContentType}
```
public String getContentType()
```


Bu özel bölümün içerik türünü belirtir.

 **Remarks:** 

Bu özellik yalnızca [isExternal()](../../com.aspose.words/custompart/\#isExternal) / [isExternal(boolean)](../../com.aspose.words/custompart/\#isExternal-boolean) false olduğunda uygulanabilir.

Varsayılan değer boş bir dizedir. Geçerli bir değer boş olmayan bir dize olmalıdır.

 **Examples:** 

Bir belgenin keyfi özel bölümler koleksiyonuna nasıl erişileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getData() {#getData}
```
public byte[] getData()
```


Bu özel bölümün verilerini içerir.

 **Remarks:** 

Bu özellik yalnızca [isExternal()](../../com.aspose.words/custompart/\#isExternal) / [isExternal(boolean)](../../com.aspose.words/custompart/\#isExternal-boolean) false olduğunda uygulanabilir.

Varsayılan değer boş bir bayt dizisidir. Değer null olamaz.

 **Examples:** 

Bir belgenin keyfi özel bölümler koleksiyonuna nasıl erişileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Returns:**
byte[] - İlgili byte[] değeri.
### getName() {#getName}
```
public String getName()
```


Bu bölümün OOXML paketindeki mutlak adını veya hedef URL'sini alır.

 **Remarks:** 

İlişki hedefi içsel ise, bu özellik paketteki mutlak bölüm adıdır. İlişki hedefi dışsal ise, bu özellik hedef URL'dir.

Varsayılan değer boş bir dizedir. Geçerli bir değer boş olmayan bir dize olmalıdır.

 **Examples:** 

Bir belgenin keyfi özel bölümler koleksiyonuna nasıl erişileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Returns:**
java.lang.String - Bu bölümün OOXML paketindeki mutlak adı veya hedef URL.
### getRelationshipType() {#getRelationshipType}
```
public String getRelationshipType()
```


Üst bölümden bu özel bölüme olan ilişki türünü alır.

 **Remarks:** 

Bir özel bölüm için ilişki türü "unknown" olmalıdır; örneğin, ISO/IEC 29500 içinde tanımlanan ilişki türlerinden biri değil, özel bir ilişki türüdür.

Varsayılan değer boş bir dizedir. Geçerli bir değer boş olmayan bir dize olmalıdır.

 **Examples:** 

Bir belgenin keyfi özel bölümler koleksiyonuna nasıl erişileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Returns:**
java.lang.String - Üst bölümden bu özel bölüme olan ilişki türü.
### isExternal() {#isExternal}
```
public boolean isExternal()
```


Bu özel bölüm OOXML paketi içinde depolanıyorsa false. Bu özel bölüm dışsal bir hedefse true.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

Bir belgenin keyfi özel bölümler koleksiyonuna nasıl erişileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### isExternal(boolean value) {#isExternal-boolean}
```
public void isExternal(boolean value)
```


Bu özel bölüm OOXML paketi içinde depolanıyorsa false. Bu özel bölüm dışsal bir hedefse true.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

Bir belgenin keyfi özel bölümler koleksiyonuna nasıl erişileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setContentType(String value) {#setContentType-java.lang.String}
```
public void setContentType(String value)
```


Bu özel bölümün içerik türünü belirtir.

 **Remarks:** 

Bu özellik yalnızca [isExternal()](../../com.aspose.words/custompart/\#isExternal) / [isExternal(boolean)](../../com.aspose.words/custompart/\#isExternal-boolean) false olduğunda uygulanabilir.

Varsayılan değer boş bir dizedir. Geçerli bir değer boş olmayan bir dize olmalıdır.

 **Examples:** 

Bir belgenin keyfi özel bölümler koleksiyonuna nasıl erişileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setData(byte[] value) {#setData-byte}
```
public void setData(byte[] value)
```


Bu özel bölümün verilerini içerir.

 **Remarks:** 

Bu özellik yalnızca [isExternal()](../../com.aspose.words/custompart/\#isExternal) / [isExternal(boolean)](../../com.aspose.words/custompart/\#isExternal-boolean) false olduğunda uygulanabilir.

Varsayılan değer boş bir bayt dizisidir. Değer null olamaz.

 **Examples:** 

Bir belgenin keyfi özel bölümler koleksiyonuna nasıl erişileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | byte[] | İlgili byte[] değeri. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Bu bölümün OOXML paketindeki mutlak adını veya hedef URL'sini ayarlar.

 **Remarks:** 

İlişki hedefi içsel ise, bu özellik paketteki mutlak bölüm adıdır. İlişki hedefi dışsal ise, bu özellik hedef URL'dir.

Varsayılan değer boş bir dizedir. Geçerli bir değer boş olmayan bir dize olmalıdır.

 **Examples:** 

Bir belgenin keyfi özel bölümler koleksiyonuna nasıl erişileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Bu bölümün OOXML paketindeki mutlak adı veya hedef URL. |

### setRelationshipType(String value) {#setRelationshipType-java.lang.String}
```
public void setRelationshipType(String value)
```


Üst bölümden bu özel bölüme olan ilişki türünü ayarlar.

 **Remarks:** 

Bir özel bölüm için ilişki türü "unknown" olmalıdır; örneğin, ISO/IEC 29500 içinde tanımlanan ilişki türlerinden biri değil, özel bir ilişki türüdür.

Varsayılan değer boş bir dizedir. Geçerli bir değer boş olmayan bir dize olmalıdır.

 **Examples:** 

Bir belgenin keyfi özel bölümler koleksiyonuna nasıl erişileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Üst bölümden bu özel bölüme olan ilişki türü. |

