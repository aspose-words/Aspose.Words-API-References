---
title: "CustomPart"
linktitle: "CustomPart"
second_title: "Aspose.Words pour Java"
description: "Représente une partie de contenu arbitraire personnalisée qui n'est pas définie par la norme ISO/IEC 29500 en Java."
type: docs
weight: 141
url: /fr/java/com.aspose.words/custompart/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class CustomPart implements Cloneable
```

Représente une partie personnalisée (contenu arbitraire) qui n'est pas définie par la norme ISO/IEC 29500.

Pour en savoir plus, consultez l'article de documentation [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control].

 **Remarks:** 

Cette classe représente une partie OOXML qui est la cible d'une « relation inconnue ». Toutes les relations non définies dans la norme ISO/IEC 29500 sont considérées comme des « relations inconnues ». Les relations inconnues sont autorisées dans un document Office Open XML à condition qu'elles respectent les directives de balisage des relations.

Microsoft Word conserve les parties personnalisées pendant les cycles d'ouverture/enregistrement. Des informations supplémentaires sont disponibles ici http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx

Aspose.Words effectue également des aller‑retours des parties personnalisées et, de plus, permet d'accéder programmatiquement à ces parties via les objets [CustomPart](../../com.aspose.words/custompart/) et [CustomPartCollection](../../com.aspose.words/custompartcollection/).

Ne confondez pas les parties personnalisées avec les données XML personnalisées. Utilisez [CustomXmlPart](../../com.aspose.words/customxmlpart/) si vous devez accéder aux données XML personnalisées.

 **Examples:** 

Montre comment accéder à la collection de parties personnalisées arbitraires d'un document.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [deepClone()](#deepClone) | Effectue une copie « suffisamment profonde » de l'objet. |
| [getContentType()](#getContentType) | Spécifie le type de contenu de cette partie personnalisée. |
| [getData()](#getData) | Contient les données de cette partie personnalisée. |
| [getName()](#getName) | Obtient le nom absolu de cette partie dans le package OOXML ou l'URL cible. |
| [getRelationshipType()](#getRelationshipType) | Obtient le type de relation du morceau parent à cette partie personnalisée. |
| [isExternal()](#isExternal) | False si cette partie personnalisée est stockée à l'intérieur du package OOXML. |
| [isExternal(boolean value)](#isExternal-boolean) | False si cette partie personnalisée est stockée à l'intérieur du package OOXML. |
| [setContentType(String value)](#setContentType-java.lang.String) | Spécifie le type de contenu de cette partie personnalisée. |
| [setData(byte[] value)](#setData-byte) | Contient les données de cette partie personnalisée. |
| [setName(String value)](#setName-java.lang.String) | Définit le nom absolu de cette partie dans le package OOXML ou l'URL cible. |
| [setRelationshipType(String value)](#setRelationshipType-java.lang.String) | Définit le type de relation du morceau parent à cette partie personnalisée. |
### deepClone() {#deepClone}
```
public CustomPart deepClone()
```


Effectue une copie « suffisamment profonde » de l'objet. Ne duplique pas les octets de la valeur [getData()](../../com.aspose.words/custompart/\#getData) / [setData(byte[])](../../com.aspose.words/custompart/\#setData-byte).

 **Examples:** 

Montre comment accéder à la collection de parties personnalisées arbitraires d'un document.

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


Spécifie le type de contenu de cette partie personnalisée.

 **Remarks:** 

Cette propriété n'est applicable que lorsque [isExternal()](../../com.aspose.words/custompart/\#isExternal) / [isExternal(boolean)](../../com.aspose.words/custompart/\#isExternal-boolean) est false.

La valeur par défaut est une chaîne vide. Une valeur valide doit être une chaîne non vide.

 **Examples:** 

Montre comment accéder à la collection de parties personnalisées arbitraires d'un document.

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
java.lang.String - La valeur java.lang.String correspondante.
### getData() {#getData}
```
public byte[] getData()
```


Contient les données de cette partie personnalisée.

 **Remarks:** 

Cette propriété n'est applicable que lorsque [isExternal()](../../com.aspose.words/custompart/\#isExternal) / [isExternal(boolean)](../../com.aspose.words/custompart/\#isExternal-boolean) est false.

La valeur par défaut est un tableau d'octets vide. La valeur ne peut pas être nulle.

 **Examples:** 

Montre comment accéder à la collection de parties personnalisées arbitraires d'un document.

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
byte[] - La valeur byte[] correspondante.
### getName() {#getName}
```
public String getName()
```


Obtient le nom absolu de cette partie dans le package OOXML ou l'URL cible.

 **Remarks:** 

Si la cible de la relation est interne, cette propriété est le nom absolu de la partie dans le package. Si la cible de la relation est externe, cette propriété est l'URL cible.

La valeur par défaut est une chaîne vide. Une valeur valide doit être une chaîne non vide.

 **Examples:** 

Montre comment accéder à la collection de parties personnalisées arbitraires d'un document.

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
java.lang.String - Le nom absolu de cette partie dans le package OOXML ou l'URL cible.
### getRelationshipType() {#getRelationshipType}
```
public String getRelationshipType()
```


Obtient le type de relation du morceau parent à cette partie personnalisée.

 **Remarks:** 

Le type de relation pour une partie personnalisée doit être « unknown » par exemple un type de relation personnalisé, et non l'un des types de relation définis dans la norme ISO/IEC 29500.

La valeur par défaut est une chaîne vide. Une valeur valide doit être une chaîne non vide.

 **Examples:** 

Montre comment accéder à la collection de parties personnalisées arbitraires d'un document.

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
java.lang.String - Le type de relation du morceau parent à cette partie personnalisée.
### isExternal() {#isExternal}
```
public boolean isExternal()
```


False si cette partie personnalisée est stockée à l'intérieur du package OOXML. True si cette partie personnalisée est une cible externe.

 **Remarks:** 

La valeur par défaut est false.

 **Examples:** 

Montre comment accéder à la collection de parties personnalisées arbitraires d'un document.

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
boolean - La valeur  boolean  correspondante.
### isExternal(boolean value) {#isExternal-boolean}
```
public void isExternal(boolean value)
```


False si cette partie personnalisée est stockée à l'intérieur du package OOXML. True si cette partie personnalisée est une cible externe.

 **Remarks:** 

La valeur par défaut est false.

 **Examples:** 

Montre comment accéder à la collection de parties personnalisées arbitraires d'un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setContentType(String value) {#setContentType-java.lang.String}
```
public void setContentType(String value)
```


Spécifie le type de contenu de cette partie personnalisée.

 **Remarks:** 

Cette propriété n'est applicable que lorsque [isExternal()](../../com.aspose.words/custompart/\#isExternal) / [isExternal(boolean)](../../com.aspose.words/custompart/\#isExternal-boolean) est false.

La valeur par défaut est une chaîne vide. Une valeur valide doit être une chaîne non vide.

 **Examples:** 

Montre comment accéder à la collection de parties personnalisées arbitraires d'un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | La valeur java.lang.String correspondante. |

### setData(byte[] value) {#setData-byte}
```
public void setData(byte[] value)
```


Contient les données de cette partie personnalisée.

 **Remarks:** 

Cette propriété n'est applicable que lorsque [isExternal()](../../com.aspose.words/custompart/\#isExternal) / [isExternal(boolean)](../../com.aspose.words/custompart/\#isExternal-boolean) est false.

La valeur par défaut est un tableau d'octets vide. La valeur ne peut pas être nulle.

 **Examples:** 

Montre comment accéder à la collection de parties personnalisées arbitraires d'un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | byte[] | La valeur byte[] correspondante. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Définit le nom absolu de cette partie dans le package OOXML ou l'URL cible.

 **Remarks:** 

Si la cible de la relation est interne, cette propriété est le nom absolu de la partie dans le package. Si la cible de la relation est externe, cette propriété est l'URL cible.

La valeur par défaut est une chaîne vide. Une valeur valide doit être une chaîne non vide.

 **Examples:** 

Montre comment accéder à la collection de parties personnalisées arbitraires d'un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | Le nom absolu de cette partie dans le package OOXML ou l'URL cible. |

### setRelationshipType(String value) {#setRelationshipType-java.lang.String}
```
public void setRelationshipType(String value)
```


Définit le type de relation du morceau parent à cette partie personnalisée.

 **Remarks:** 

Le type de relation pour une partie personnalisée doit être « unknown » par exemple un type de relation personnalisé, et non l'un des types de relation définis dans la norme ISO/IEC 29500.

La valeur par défaut est une chaîne vide. Une valeur valide doit être une chaîne non vide.

 **Examples:** 

Montre comment accéder à la collection de parties personnalisées arbitraires d'un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | Le type de relation du morceau parent à cette partie personnalisée. |

