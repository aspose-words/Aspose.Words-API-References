---
title: "WriteProtection"
linktitle: "WriteProtection"
second_title: "Aspose.Words für Java"
description: "Gibt die Schreibschutz-Einstellungen für ein Dokument in Java an."
type: docs
weight: 738
url: /de/java/com.aspose.words/writeprotection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class WriteProtection implements Cloneable
```

Gibt die Schreibschutz-Einstellungen für ein Dokument an.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Protect or Encrypt a Document ][Protect or Encrypt a Document].

 **Remarks:** 

Der Schreibschutz gibt an, ob der Autor empfohlen hat, das Dokument nur lesend zu öffnen und/oder ein Passwort zum Ändern des Dokuments erforderlich ist.

Schreibschutz unterscheidet sich vom Dokumentenschutz. Schreibschutz wird in Microsoft Word in den Optionen des Dialogfelds „Speichern unter“ angegeben.

Sie erstellen keine Instanzen dieser Klasse direkt. Sie greifen über die Eigenschaft [Document.getWriteProtection()](../../com.aspose.words/document/\#getWriteProtection) auf die Dokumentenschutz-Einstellungen zu.

 **Examples:** 

Zeigt, wie man ein Dokument mit einem Passwort schützt.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getReadOnlyRecommended()](#getReadOnlyRecommended) | Gibt an, ob der Dokumentautor empfohlen hat, das Dokument nur lesend zu öffnen. |
| [isWriteProtected()](#isWriteProtected) | Gibt  true  zurück, wenn ein Schreibschutz-Passwort festgelegt ist. |
| [setPassword(String password)](#setPassword-java.lang.String) | Setzt das Schreibschutz-Passwort für das Dokument. |
| [setReadOnlyRecommended(boolean value)](#setReadOnlyRecommended-boolean) | Gibt an, ob der Dokumentautor empfohlen hat, das Dokument nur lesend zu öffnen. |
| [validatePassword(String password)](#validatePassword-java.lang.String) | Gibt  true  zurück, wenn das angegebene Passwort dem Schreibschutz-Passwort entspricht, mit dem das Dokument geschützt wurde. |
### getReadOnlyRecommended() {#getReadOnlyRecommended}
```
public boolean getReadOnlyRecommended()
```


Gibt an, ob der Dokumentautor empfohlen hat, das Dokument nur lesend zu öffnen.

 **Examples:** 

Zeigt, wie man ein Dokument mit einem Passwort schützt.

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
boolean - Der entsprechende  boolean  Wert.
### isWriteProtected() {#isWriteProtected}
```
public boolean isWriteProtected()
```


Gibt  true  zurück, wenn ein Schreibschutz-Passwort festgelegt ist.

 **Examples:** 

Zeigt, wie man ein Dokument mit einem Passwort schützt.

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
boolean -  true  wenn ein Schreibschutz-Passwort festgelegt ist.
### setPassword(String password) {#setPassword-java.lang.String}
```
public void setPassword(String password)
```


Setzt das Schreibschutz-Passwort für das Dokument.

 **Remarks:** 

Wenn ein Passwort festgelegt ist, fordert Microsoft Word den Benutzer auf, es einzugeben oder das Dokument schreibgeschützt zu öffnen.

 **Examples:** 

Zeigt, wie man ein Dokument mit einem Passwort schützt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Passwort | java.lang.String | Das zu setzende Passwort. Darf nicht  null  sein, kann aber eine leere Zeichenfolge sein. |

### setReadOnlyRecommended(boolean value) {#setReadOnlyRecommended-boolean}
```
public void setReadOnlyRecommended(boolean value)
```


Gibt an, ob der Dokumentautor empfohlen hat, das Dokument nur lesend zu öffnen.

 **Examples:** 

Zeigt, wie man ein Dokument mit einem Passwort schützt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### validatePassword(String password) {#validatePassword-java.lang.String}
```
public boolean validatePassword(String password)
```


Gibt  true  zurück, wenn das angegebene Passwort dem Schreibschutz-Passwort entspricht, mit dem das Dokument geschützt wurde. Wenn das Dokument nicht passwortgeschützt ist, wird  false  zurückgegeben.

 **Examples:** 

Zeigt, wie man ein Dokument mit einem Passwort schützt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Passwort | java.lang.String |  |

**Returns:**
boolean
