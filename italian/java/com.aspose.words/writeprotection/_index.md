---
title: "WriteProtection"
linktitle: "WriteProtection"
second_title: "Aspose.Words per Java"
description: "Specifica le impostazioni di protezione in scrittura per un documento in Java."
type: docs
weight: 738
url: /it/java/com.aspose.words/writeprotection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class WriteProtection implements Cloneable
```

Specifica le impostazioni di protezione in scrittura per un documento.

To learn more, visit the [ Proteggere o crittografare un documento ][Proteggere o crittografare un documento] documentation article.

 **Remarks:** 

La protezione in scrittura specifica se l'autore ha raccomandato che il documento sia aperto in sola lettura e/o richieda una password per modificare un documento.

La protezione in scrittura è diversa dalla protezione del documento. La protezione in scrittura è specificata in Microsoft Word nelle opzioni della finestra di dialogo Salva con nome.

Non si creano istanze di questa classe direttamente. Si accede alle impostazioni di protezione del documento tramite la proprietà [Document.getWriteProtection()](../../com.aspose.words/document/\#getWriteProtection).

 **Examples:** 

Mostra come proteggere un documento con una password.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This document is protected.");
 // Enter a password up to 15 characters in length, and then verify the document's protection status.
 doc.getWriteProtection().setPassword("MyPassword");
 doc.getWriteProtection().setReadOnlyRecommended(true);

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());
 Assert.assertTrue(doc.getWriteProtection().validatePassword("MyPassword"));

 // Protection does not prevent the document from being edited programmatically, nor does it encrypt the contents.
 doc.save(getArtifactsDir() + "Document.WriteProtection.docx");
 doc = new Document(getArtifactsDir() + "Document.WriteProtection.docx");

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());

 builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln("Writing text in a protected document.");

 Assert.assertEquals("Hello world! This document is protected." +
         "\rWriting text in a protected document.", doc.getText().trim());
 
```


[Protect or Encrypt a Document]: https://docs.aspose.com/words/java/protect-or-encrypt-a-document/
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getReadOnlyRecommended()](#getReadOnlyRecommended) | Specifica se l'autore del documento ha raccomandato che il documento sia aperto in sola lettura. |
| [isWriteProtected()](#isWriteProtected) | Restituisce  true  quando è impostata una password di protezione in scrittura. |
| [setPassword(String password)](#setPassword-java.lang.String) | Imposta la password di protezione in scrittura per il documento. |
| [setReadOnlyRecommended(boolean value)](#setReadOnlyRecommended-boolean) | Specifica se l'autore del documento ha raccomandato che il documento sia aperto in sola lettura. |
| [validatePassword(String password)](#validatePassword-java.lang.String) | Restituisce  true  se la password specificata è la stessa della password di protezione in scrittura con cui il documento è stato protetto. |
### getReadOnlyRecommended() {#getReadOnlyRecommended}
```
public boolean getReadOnlyRecommended()
```


Specifica se l'autore del documento ha raccomandato che il documento sia aperto in sola lettura.

 **Examples:** 

Mostra come proteggere un documento con una password.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This document is protected.");
 // Enter a password up to 15 characters in length, and then verify the document's protection status.
 doc.getWriteProtection().setPassword("MyPassword");
 doc.getWriteProtection().setReadOnlyRecommended(true);

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());
 Assert.assertTrue(doc.getWriteProtection().validatePassword("MyPassword"));

 // Protection does not prevent the document from being edited programmatically, nor does it encrypt the contents.
 doc.save(getArtifactsDir() + "Document.WriteProtection.docx");
 doc = new Document(getArtifactsDir() + "Document.WriteProtection.docx");

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());

 builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln("Writing text in a protected document.");

 Assert.assertEquals("Hello world! This document is protected." +
         "\rWriting text in a protected document.", doc.getText().trim());
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### isWriteProtected() {#isWriteProtected}
```
public boolean isWriteProtected()
```


Restituisce  true  quando è impostata una password di protezione in scrittura.

 **Examples:** 

Mostra come proteggere un documento con una password.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This document is protected.");
 // Enter a password up to 15 characters in length, and then verify the document's protection status.
 doc.getWriteProtection().setPassword("MyPassword");
 doc.getWriteProtection().setReadOnlyRecommended(true);

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());
 Assert.assertTrue(doc.getWriteProtection().validatePassword("MyPassword"));

 // Protection does not prevent the document from being edited programmatically, nor does it encrypt the contents.
 doc.save(getArtifactsDir() + "Document.WriteProtection.docx");
 doc = new Document(getArtifactsDir() + "Document.WriteProtection.docx");

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());

 builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln("Writing text in a protected document.");

 Assert.assertEquals("Hello world! This document is protected." +
         "\rWriting text in a protected document.", doc.getText().trim());
 
```

**Returns:**
boolean -  true  quando è impostata una password di protezione in scrittura.
### setPassword(String password) {#setPassword-java.lang.String}
```
public void setPassword(String password)
```


Imposta la password di protezione in scrittura per il documento.

 **Remarks:** 

Se è impostata una password, Microsoft Word richiederà all'utente di inserirla o di aprire il documento in sola lettura.

 **Examples:** 

Mostra come proteggere un documento con una password.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This document is protected.");
 // Enter a password up to 15 characters in length, and then verify the document's protection status.
 doc.getWriteProtection().setPassword("MyPassword");
 doc.getWriteProtection().setReadOnlyRecommended(true);

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());
 Assert.assertTrue(doc.getWriteProtection().validatePassword("MyPassword"));

 // Protection does not prevent the document from being edited programmatically, nor does it encrypt the contents.
 doc.save(getArtifactsDir() + "Document.WriteProtection.docx");
 doc = new Document(getArtifactsDir() + "Document.WriteProtection.docx");

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());

 builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln("Writing text in a protected document.");

 Assert.assertEquals("Hello world! This document is protected." +
         "\rWriting text in a protected document.", doc.getText().trim());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| password | java.lang.String | La password da impostare. Non può essere  null , ma può essere una stringa vuota. |

### setReadOnlyRecommended(boolean value) {#setReadOnlyRecommended-boolean}
```
public void setReadOnlyRecommended(boolean value)
```


Specifica se l'autore del documento ha raccomandato che il documento sia aperto in sola lettura.

 **Examples:** 

Mostra come proteggere un documento con una password.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This document is protected.");
 // Enter a password up to 15 characters in length, and then verify the document's protection status.
 doc.getWriteProtection().setPassword("MyPassword");
 doc.getWriteProtection().setReadOnlyRecommended(true);

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());
 Assert.assertTrue(doc.getWriteProtection().validatePassword("MyPassword"));

 // Protection does not prevent the document from being edited programmatically, nor does it encrypt the contents.
 doc.save(getArtifactsDir() + "Document.WriteProtection.docx");
 doc = new Document(getArtifactsDir() + "Document.WriteProtection.docx");

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());

 builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln("Writing text in a protected document.");

 Assert.assertEquals("Hello world! This document is protected." +
         "\rWriting text in a protected document.", doc.getText().trim());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### validatePassword(String password) {#validatePassword-java.lang.String}
```
public boolean validatePassword(String password)
```


Restituisce  true  se la password specificata è la stessa della password di protezione in scrittura con cui il documento è stato protetto. Se il documento non è protetto in scrittura con password, restituisce  false .

 **Examples:** 

Mostra come proteggere un documento con una password.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This document is protected.");
 // Enter a password up to 15 characters in length, and then verify the document's protection status.
 doc.getWriteProtection().setPassword("MyPassword");
 doc.getWriteProtection().setReadOnlyRecommended(true);

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());
 Assert.assertTrue(doc.getWriteProtection().validatePassword("MyPassword"));

 // Protection does not prevent the document from being edited programmatically, nor does it encrypt the contents.
 doc.save(getArtifactsDir() + "Document.WriteProtection.docx");
 doc = new Document(getArtifactsDir() + "Document.WriteProtection.docx");

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());

 builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln("Writing text in a protected document.");

 Assert.assertEquals("Hello world! This document is protected." +
         "\rWriting text in a protected document.", doc.getText().trim());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| password | java.lang.String |  |

**Returns:**
boolean
