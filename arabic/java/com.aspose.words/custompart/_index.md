---
title: "CustomPart"
linktitle: "CustomPart"
second_title: "Aspose.Words لـ Java"
description: "يمثل جزء محتوى مخصص وعشوائي غير معرف في معيار ISO/IEC 29500 في Java."
type: docs
weight: 141
url: /ar/java/com.aspose.words/custompart/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class CustomPart implements Cloneable
```

يمثل جزءًا مخصصًا (محتوى تعسفي) غير معرف بمعيار ISO/IEC 29500.

لمزيد من المعلومات، زر مقالة الوثائق [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control].

 **Remarks:** 

هذه الفئة تمثل جزء OOXML هو هدف "علاقة غير معروفة". جميع العلاقات غير المعرفة ضمن ISO/IEC 29500 تُعتبر "علاقات غير معروفة". تُسمح بالعلاقات غير المعروفة داخل مستند Office Open XML بشرط أن تتوافق مع إرشادات توصيف العلاقات.

Microsoft Word يحافظ على الأجزاء المخصصة أثناء دورات الفتح/الحفظ. يمكن العثور على بعض المعلومات الإضافية هنا http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx

Aspose.Words يقوم أيضًا بتمرير الأجزاء المخصصة وإضافةً إلى ذلك، يسمح بالوصول البرمجي إلى هذه الأجزاء عبر كائنات [CustomPart](../../com.aspose.words/custompart/) و [CustomPartCollection](../../com.aspose.words/custompartcollection/).

لا تخلط بين الأجزاء المخصصة وبيانات XML المخصصة. استخدم [CustomXmlPart](../../com.aspose.words/customxmlpart/) إذا كنت بحاجة للوصول إلى بيانات XML المخصصة.

 **Examples:** 

يعرض كيفية الوصول إلى مجموعة الأجزاء المخصصة العشوائية في المستند.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [deepClone()](#deepClone) | ينشئ نسخة "deep enough" من الكائن. |
| [getContentType()](#getContentType) | يحدد نوع المحتوى لهذا الجزء المخصص. |
| [getData()](#getData) | يحتوي على بيانات هذا الجزء المخصص. |
| [getName()](#getName) | يحصل على الاسم المطلق لهذا الجزء داخل حزمة OOXML أو عنوان URL الهدف. |
| [getRelationshipType()](#getRelationshipType) | يحصل على نوع العلاقة من الجزء الأب إلى هذا الجزء المخصص. |
| [isExternal()](#isExternal) | خطأ إذا كان هذا الجزء المخصص مخزنًا داخل حزمة OOXML. |
| [isExternal(boolean value)](#isExternal-boolean) | خطأ إذا كان هذا الجزء المخصص مخزنًا داخل حزمة OOXML. |
| [setContentType(String value)](#setContentType-java.lang.String) | يحدد نوع المحتوى لهذا الجزء المخصص. |
| [setData(byte[] value)](#setData-byte) | يحتوي على بيانات هذا الجزء المخصص. |
| [setName(String value)](#setName-java.lang.String) | يضبط الاسم المطلق لهذا الجزء داخل حزمة OOXML أو عنوان URL الهدف. |
| [setRelationshipType(String value)](#setRelationshipType-java.lang.String) | يضبط نوع العلاقة من الجزء الأب إلى هذا الجزء المخصص. |
### deepClone() {#deepClone}
```
public CustomPart deepClone()
```


ينشئ نسخة "عميقة بما فيه الكفاية" من الكائن. لا يكرر بايتات قيمة [getData()](../../com.aspose.words/custompart/\#getData) / [setData(byte[])](../../com.aspose.words/custompart/\#setData-byte).

 **Examples:** 

يعرض كيفية الوصول إلى مجموعة الأجزاء المخصصة العشوائية في المستند.

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


يحدد نوع المحتوى لهذا الجزء المخصص.

 **Remarks:** 

هذه الخاصية قابلة للتطبيق فقط عندما يكون [isExternal()](../../com.aspose.words/custompart/\#isExternal) / [isExternal(boolean)](../../com.aspose.words/custompart/\#isExternal-boolean) غير صحيح.

القيمة الافتراضية هي سلسلة فارغة. يجب أن تكون القيمة صالحة غير فارغة.

 **Examples:** 

يعرض كيفية الوصول إلى مجموعة الأجزاء المخصصة العشوائية في المستند.

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
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getData() {#getData}
```
public byte[] getData()
```


يحتوي على بيانات هذا الجزء المخصص.

 **Remarks:** 

هذه الخاصية قابلة للتطبيق فقط عندما يكون [isExternal()](../../com.aspose.words/custompart/\#isExternal) / [isExternal(boolean)](../../com.aspose.words/custompart/\#isExternal-boolean) غير صحيح.

القيمة الافتراضية هي مصفوفة بايت فارغة. لا يمكن أن تكون القيمة null.

 **Examples:** 

يعرض كيفية الوصول إلى مجموعة الأجزاء المخصصة العشوائية في المستند.

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
byte[] - القيمة المقابلة من نوع byte[] .
### getName() {#getName}
```
public String getName()
```


يحصل على الاسم المطلق لهذا الجزء داخل حزمة OOXML أو عنوان URL الهدف.

 **Remarks:** 

إذا كان هدف العلاقة داخليًا، فإن هذه الخاصية هي اسم الجزء المطلق داخل الحزمة. إذا كان هدف العلاقة خارجيًا، فإن هذه الخاصية هي عنوان URL الهدف.

القيمة الافتراضية هي سلسلة فارغة. يجب أن تكون القيمة صالحة غير فارغة.

 **Examples:** 

يعرض كيفية الوصول إلى مجموعة الأجزاء المخصصة العشوائية في المستند.

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
java.lang.String - الاسم المطلق لهذا الجزء داخل حزمة OOXML أو عنوان URL الهدف.
### getRelationshipType() {#getRelationshipType}
```
public String getRelationshipType()
```


يحصل على نوع العلاقة من الجزء الأب إلى هذا الجزء المخصص.

 **Remarks:** 

نوع العلاقة لجزء مخصص يجب أن يكون "unknown" مثل علاقة مخصصة، وليس أحد أنواع العلاقات المعرفة ضمن ISO/IEC 29500.

القيمة الافتراضية هي سلسلة فارغة. يجب أن تكون القيمة صالحة غير فارغة.

 **Examples:** 

يعرض كيفية الوصول إلى مجموعة الأجزاء المخصصة العشوائية في المستند.

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
java.lang.String - نوع العلاقة من الجزء الأب إلى هذا الجزء المخصص.
### isExternal() {#isExternal}
```
public boolean isExternal()
```


خطأ إذا كان هذا الجزء المخصص مخزنًا داخل حزمة OOXML. صحيح إذا كان هذا الجزء المخصص هدفًا خارجيًا.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية الوصول إلى مجموعة الأجزاء المخصصة العشوائية في المستند.

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
boolean - القيمة المنطقية المقابلة.
### isExternal(boolean value) {#isExternal-boolean}
```
public void isExternal(boolean value)
```


خطأ إذا كان هذا الجزء المخصص مخزنًا داخل حزمة OOXML. صحيح إذا كان هذا الجزء المخصص هدفًا خارجيًا.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية الوصول إلى مجموعة الأجزاء المخصصة العشوائية في المستند.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setContentType(String value) {#setContentType-java.lang.String}
```
public void setContentType(String value)
```


يحدد نوع المحتوى لهذا الجزء المخصص.

 **Remarks:** 

هذه الخاصية قابلة للتطبيق فقط عندما يكون [isExternal()](../../com.aspose.words/custompart/\#isExternal) / [isExternal(boolean)](../../com.aspose.words/custompart/\#isExternal-boolean) غير صحيح.

القيمة الافتراضية هي سلسلة فارغة. يجب أن تكون القيمة صالحة غير فارغة.

 **Examples:** 

يعرض كيفية الوصول إلى مجموعة الأجزاء المخصصة العشوائية في المستند.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

### setData(byte[] value) {#setData-byte}
```
public void setData(byte[] value)
```


يحتوي على بيانات هذا الجزء المخصص.

 **Remarks:** 

هذه الخاصية قابلة للتطبيق فقط عندما يكون [isExternal()](../../com.aspose.words/custompart/\#isExternal) / [isExternal(boolean)](../../com.aspose.words/custompart/\#isExternal-boolean) غير صحيح.

القيمة الافتراضية هي مصفوفة بايت فارغة. لا يمكن أن تكون القيمة null.

 **Examples:** 

يعرض كيفية الوصول إلى مجموعة الأجزاء المخصصة العشوائية في المستند.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | byte[] | القيمة المقابلة من نوع byte[] . |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


يضبط الاسم المطلق لهذا الجزء داخل حزمة OOXML أو عنوان URL الهدف.

 **Remarks:** 

إذا كان هدف العلاقة داخليًا، فإن هذه الخاصية هي اسم الجزء المطلق داخل الحزمة. إذا كان هدف العلاقة خارجيًا، فإن هذه الخاصية هي عنوان URL الهدف.

القيمة الافتراضية هي سلسلة فارغة. يجب أن تكون القيمة صالحة غير فارغة.

 **Examples:** 

يعرض كيفية الوصول إلى مجموعة الأجزاء المخصصة العشوائية في المستند.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | الاسم المطلق لهذا الجزء داخل حزمة OOXML أو عنوان URL الهدف. |

### setRelationshipType(String value) {#setRelationshipType-java.lang.String}
```
public void setRelationshipType(String value)
```


يضبط نوع العلاقة من الجزء الأب إلى هذا الجزء المخصص.

 **Remarks:** 

نوع العلاقة لجزء مخصص يجب أن يكون "unknown" مثل علاقة مخصصة، وليس أحد أنواع العلاقات المعرفة ضمن ISO/IEC 29500.

القيمة الافتراضية هي سلسلة فارغة. يجب أن تكون القيمة صالحة غير فارغة.

 **Examples:** 

يعرض كيفية الوصول إلى مجموعة الأجزاء المخصصة العشوائية في المستند.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | نوع العلاقة من الجزء الأب إلى هذا الجزء المخصص. |

