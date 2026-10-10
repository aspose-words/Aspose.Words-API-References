---
title: "CustomPart"
linktitle: "CustomPart"
second_title: "Aspose.Words per Java"
description: "Rappresenta una parte di contenuto arbitrario personalizzata che non è definita dallo standard ISO/IEC 29500 in Java."
type: docs
weight: 141
url: /it/java/com.aspose.words/custompart/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class CustomPart implements Cloneable
```

Rappresenta una parte personalizzata (contenuto arbitrario) che non è definita dallo standard ISO/IEC 29500.

Per saperne di più, visita l'articolo di documentazione [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control].

 **Remarks:** 

Questa classe rappresenta una parte OOXML che è il target di una "relazione sconosciuta". Tutte le relazioni non definite all'interno di ISO/IEC 29500 sono considerate "relazioni sconosciute". Le relazioni sconosciute sono consentite all'interno di un documento Office Open XML a condizione che rispettino le linee guida per il markup delle relazioni.

Microsoft Word conserva le parti personalizzate durante i cicli di apertura/salvataggio. Ulteriori informazioni sono disponibili qui http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx

Aspose.Words esegue anche il round‑trip delle parti personalizzate e, inoltre, consente di accedere programmaticamente a tali parti tramite gli oggetti [CustomPart](../../com.aspose.words/custompart/) e [CustomPartCollection](../../com.aspose.words/custompartcollection/).

Non confondere le parti personalizzate con i Dati XML Personalizzati. Usa [CustomXmlPart](../../com.aspose.words/customxmlpart/) se devi accedere ai Dati XML Personalizzati.

 **Examples:** 

Mostra come accedere alla raccolta di parti personalizzate arbitrarie di un documento.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [deepClone()](#deepClone) | Crea una copia "sufficientemente profonda" dell'oggetto. |
| [getContentType()](#getContentType) | Specifica il tipo di contenuto di questa parte personalizzata. |
| [getData()](#getData) | Contiene i dati di questa parte personalizzata. |
| [getName()](#getName) | Ottiene il nome assoluto di questa parte all'interno del pacchetto OOXML o l'URL di destinazione. |
| [getRelationshipType()](#getRelationshipType) | Ottiene il tipo di relazione dal componente padre a questa parte personalizzata. |
| [isExternal()](#isExternal) | Falso se questa parte personalizzata è memorizzata all'interno del pacchetto OOXML. |
| [isExternal(boolean value)](#isExternal-boolean) | Falso se questa parte personalizzata è memorizzata all'interno del pacchetto OOXML. |
| [setContentType(String value)](#setContentType-java.lang.String) | Specifica il tipo di contenuto di questa parte personalizzata. |
| [setData(byte[] value)](#setData-byte) | Contiene i dati di questa parte personalizzata. |
| [setName(String value)](#setName-java.lang.String) | Imposta il nome assoluto di questa parte all'interno del pacchetto OOXML o l'URL di destinazione. |
| [setRelationshipType(String value)](#setRelationshipType-java.lang.String) | Imposta il tipo di relazione dal componente padre a questa parte personalizzata. |
### deepClone() {#deepClone}
```
public CustomPart deepClone()
```


Crea una copia "sufficientemente profonda" dell'oggetto. Non duplica i byte del valore [getData()](../../com.aspose.words/custompart/\#getData) / [setData(byte[])](../../com.aspose.words/custompart/\#setData-byte).

 **Examples:** 

Mostra come accedere alla raccolta di parti personalizzate arbitrarie di un documento.

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


Specifica il tipo di contenuto di questa parte personalizzata.

 **Remarks:** 

Questa proprietà è applicabile solo quando [isExternal()](../../com.aspose.words/custompart/\#isExternal) / [isExternal(boolean)](../../com.aspose.words/custompart/\#isExternal-boolean) è false.

Il valore predefinito è una stringa vuota. Un valore valido deve essere una stringa non vuota.

 **Examples:** 

Mostra come accedere alla raccolta di parti personalizzate arbitrarie di un documento.

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
java.lang.String - Il valore java.lang.String corrispondente.
### getData() {#getData}
```
public byte[] getData()
```


Contiene i dati di questa parte personalizzata.

 **Remarks:** 

Questa proprietà è applicabile solo quando [isExternal()](../../com.aspose.words/custompart/\#isExternal) / [isExternal(boolean)](../../com.aspose.words/custompart/\#isExternal-boolean) è false.

Il valore predefinito è un array di byte vuoto. Il valore non può essere  null .

 **Examples:** 

Mostra come accedere alla raccolta di parti personalizzate arbitrarie di un documento.

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
byte[] - Il valore byte[] corrispondente.
### getName() {#getName}
```
public String getName()
```


Ottiene il nome assoluto di questa parte all'interno del pacchetto OOXML o l'URL di destinazione.

 **Remarks:** 

Se il target della relazione è interno, questa proprietà è il nome assoluto della parte all'interno del pacchetto. Se il target della relazione è esterno, questa proprietà è l'URL di destinazione.

Il valore predefinito è una stringa vuota. Un valore valido deve essere una stringa non vuota.

 **Examples:** 

Mostra come accedere alla raccolta di parti personalizzate arbitrarie di un documento.

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
java.lang.String - Il nome assoluto di questa parte all'interno del pacchetto OOXML o l'URL di destinazione.
### getRelationshipType() {#getRelationshipType}
```
public String getRelationshipType()
```


Ottiene il tipo di relazione dal componente padre a questa parte personalizzata.

 **Remarks:** 

Il tipo di relazione per una parte personalizzata deve essere "unknown", ad es. un tipo di relazione personalizzato, non uno dei tipi di relazione definiti all'interno di ISO/IEC 29500.

Il valore predefinito è una stringa vuota. Un valore valido deve essere una stringa non vuota.

 **Examples:** 

Mostra come accedere alla raccolta di parti personalizzate arbitrarie di un documento.

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
java.lang.String - Il tipo di relazione dal componente padre a questa parte personalizzata.
### isExternal() {#isExternal}
```
public boolean isExternal()
```


Falso se questa parte personalizzata è memorizzata all'interno del pacchetto OOXML. Vero se questa parte personalizzata è un target esterno.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come accedere alla raccolta di parti personalizzate arbitrarie di un documento.

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
boolean - Il valore booleano corrispondente.
### isExternal(boolean value) {#isExternal-boolean}
```
public void isExternal(boolean value)
```


Falso se questa parte personalizzata è memorizzata all'interno del pacchetto OOXML. Vero se questa parte personalizzata è un target esterno.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come accedere alla raccolta di parti personalizzate arbitrarie di un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setContentType(String value) {#setContentType-java.lang.String}
```
public void setContentType(String value)
```


Specifica il tipo di contenuto di questa parte personalizzata.

 **Remarks:** 

Questa proprietà è applicabile solo quando [isExternal()](../../com.aspose.words/custompart/\#isExternal) / [isExternal(boolean)](../../com.aspose.words/custompart/\#isExternal-boolean) è false.

Il valore predefinito è una stringa vuota. Un valore valido deve essere una stringa non vuota.

 **Examples:** 

Mostra come accedere alla raccolta di parti personalizzate arbitrarie di un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il valore java.lang.String corrispondente. |

### setData(byte[] value) {#setData-byte}
```
public void setData(byte[] value)
```


Contiene i dati di questa parte personalizzata.

 **Remarks:** 

Questa proprietà è applicabile solo quando [isExternal()](../../com.aspose.words/custompart/\#isExternal) / [isExternal(boolean)](../../com.aspose.words/custompart/\#isExternal-boolean) è false.

Il valore predefinito è un array di byte vuoto. Il valore non può essere  null .

 **Examples:** 

Mostra come accedere alla raccolta di parti personalizzate arbitrarie di un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | byte[] | Il valore byte[] corrispondente. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Imposta il nome assoluto di questa parte all'interno del pacchetto OOXML o l'URL di destinazione.

 **Remarks:** 

Se il target della relazione è interno, questa proprietà è il nome assoluto della parte all'interno del pacchetto. Se il target della relazione è esterno, questa proprietà è l'URL di destinazione.

Il valore predefinito è una stringa vuota. Un valore valido deve essere una stringa non vuota.

 **Examples:** 

Mostra come accedere alla raccolta di parti personalizzate arbitrarie di un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il nome assoluto di questa parte all'interno del pacchetto OOXML o l'URL di destinazione. |

### setRelationshipType(String value) {#setRelationshipType-java.lang.String}
```
public void setRelationshipType(String value)
```


Imposta il tipo di relazione dal componente padre a questa parte personalizzata.

 **Remarks:** 

Il tipo di relazione per una parte personalizzata deve essere "unknown", ad es. un tipo di relazione personalizzato, non uno dei tipi di relazione definiti all'interno di ISO/IEC 29500.

Il valore predefinito è una stringa vuota. Un valore valido deve essere una stringa non vuota.

 **Examples:** 

Mostra come accedere alla raccolta di parti personalizzate arbitrarie di un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il tipo di relazione dal componente padre a questa parte personalizzata. |

