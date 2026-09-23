---
title: "PdfEncryptionDetails"
linktitle: "PdfEncryptionDetails"
second_title: "Aspose.Words für Java"
description: "Enthält Details zum Verschlüsseln und zu Zugriffsberechtigungen für ein PDF-Dokument in Java."
type: docs
weight: 534
url: /de/java/com.aspose.words/pdfencryptiondetails/
---

**Inheritance:**
java.lang.Object
```
public class PdfEncryptionDetails
```

Enthält Details zur Verschlüsselung und zu Zugriffsberechtigungen für ein PDF-Dokument.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Protect or Encrypt a Document ][Protect or Encrypt a Document].

 **Examples:** 

Zeigt, wie Berechtigungen für ein gespeichertes PDF-Dokument festgelegt werden.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```


[Protect or Encrypt a Document]: https://docs.aspose.com/words/java/protect-or-encrypt-a-document/
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [PdfEncryptionDetails(String userPassword, String ownerPassword)](#PdfEncryptionDetails-java.lang.String-java.lang.String) | Initialisiert eine Instanz dieser Klasse. |
| [PdfEncryptionDetails(String userPassword, String ownerPassword, int permissions)](#PdfEncryptionDetails-java.lang.String-java.lang.String-int) | Initialisiert eine neue Instanz dieser Klasse. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getOwnerPassword()](#getOwnerPassword) | Gibt das Besitzerpasswort für das verschlüsselte PDF-Dokument an. |
| [getPermissions()](#getPermissions) | Gibt die Vorgänge an, die einem Benutzer bei einem verschlüsselten PDF-Dokument erlaubt sind. |
| [getUserPassword()](#getUserPassword) | Gibt das Benutzerpasswort an, das zum Öffnen des verschlüsselten PDF-Dokuments erforderlich ist. |
| [setOwnerPassword(String value)](#setOwnerPassword-java.lang.String) | Gibt das Besitzerpasswort für das verschlüsselte PDF-Dokument an. |
| [setPermissions(int value)](#setPermissions-int) | Gibt die Vorgänge an, die einem Benutzer bei einem verschlüsselten PDF-Dokument erlaubt sind. |
| [setUserPassword(String value)](#setUserPassword-java.lang.String) | Gibt das Benutzerpasswort an, das zum Öffnen des verschlüsselten PDF-Dokuments erforderlich ist. |
### PdfEncryptionDetails(String userPassword, String ownerPassword) {#PdfEncryptionDetails-java.lang.String-java.lang.String}
```
public PdfEncryptionDetails(String userPassword, String ownerPassword)
```


Initialisiert eine Instanz dieser Klasse.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| userPassword | java.lang.String |  |
| ownerPassword | java.lang.String |  |

### PdfEncryptionDetails(String userPassword, String ownerPassword, int permissions) {#PdfEncryptionDetails-java.lang.String-java.lang.String-int}
```
public PdfEncryptionDetails(String userPassword, String ownerPassword, int permissions)
```


Initialisiert eine neue Instanz dieser Klasse.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| userPassword | java.lang.String |  |
| ownerPassword | java.lang.String |  |
| permissions | int |  |

### getOwnerPassword() {#getOwnerPassword}
```
public String getOwnerPassword()
```


Gibt das Besitzerpasswort für das verschlüsselte PDF-Dokument an.

 **Remarks:** 

Das Besitzerpasswort ermöglicht dem Benutzer, ein verschlüsseltes PDF-Dokument zu öffnen, ohne dass Zugriffsrestriktionen gelten, die in [getPermissions()](../../com.aspose.words/pdfencryptiondetails/\#getPermissions) / [setPermissions(int)](../../com.aspose.words/pdfencryptiondetails/\#setPermissions-int) angegeben sind.

Das Besitzerpasswort darf nicht dasselbe wie das Benutzerpasswort sein.

 **Examples:** 

Zeigt, wie Berechtigungen für ein gespeichertes PDF-Dokument festgelegt werden.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```

**Returns:**
java.lang.String - Der entsprechende java.lang.String-Wert.
### getPermissions() {#getPermissions}
```
public int getPermissions()
```


Gibt die Vorgänge an, die einem Benutzer an einem verschlüsselten PDF-Dokument erlaubt sind. Der Standardwert ist [PdfPermissions.DISALLOW\_ALL](../../com.aspose.words/pdfpermissions/\#DISALLOW-ALL).

 **Examples:** 

Zeigt, wie Berechtigungen für ein gespeichertes PDF-Dokument festgelegt werden.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```

**Returns:**
int - Der entsprechende  int  Wert. Der zurückgegebene Wert ist eine bitweise Kombination von [PdfPermissions](../../com.aspose.words/pdfpermissions/) Konstanten.
### getUserPassword() {#getUserPassword}
```
public String getUserPassword()
```


Gibt das Benutzerpasswort an, das zum Öffnen des verschlüsselten PDF-Dokuments erforderlich ist.

 **Remarks:** 

Das Benutzerpasswort wird zum Öffnen eines verschlüsselten PDF-Dokuments zum Anzeigen benötigt. Die in [getPermissions()](../../com.aspose.words/pdfencryptiondetails/\#getPermissions) / [setPermissions(int)](../../com.aspose.words/pdfencryptiondetails/\#setPermissions-int) angegebenen Berechtigungen werden von der Lesesoftware durchgesetzt.

Das Benutzerpasswort kann  null  oder ein leerer String sein; in diesem Fall wird beim Öffnen des PDF-Dokuments kein Passwort vom Benutzer verlangt. Das Benutzerpasswort darf nicht dasselbe wie das Besitzerpasswort sein.

 **Examples:** 

Zeigt, wie Berechtigungen für ein gespeichertes PDF-Dokument festgelegt werden.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```

**Returns:**
java.lang.String - Der entsprechende java.lang.String-Wert.
### setOwnerPassword(String value) {#setOwnerPassword-java.lang.String}
```
public void setOwnerPassword(String value)
```


Gibt das Besitzerpasswort für das verschlüsselte PDF-Dokument an.

 **Remarks:** 

Das Besitzerpasswort ermöglicht dem Benutzer, ein verschlüsseltes PDF-Dokument zu öffnen, ohne dass Zugriffsrestriktionen gelten, die in [getPermissions()](../../com.aspose.words/pdfencryptiondetails/\#getPermissions) / [setPermissions(int)](../../com.aspose.words/pdfencryptiondetails/\#setPermissions-int) angegeben sind.

Das Besitzerpasswort darf nicht dasselbe wie das Benutzerpasswort sein.

 **Examples:** 

Zeigt, wie Berechtigungen für ein gespeichertes PDF-Dokument festgelegt werden.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

### setPermissions(int value) {#setPermissions-int}
```
public void setPermissions(int value)
```


Gibt die Vorgänge an, die einem Benutzer an einem verschlüsselten PDF-Dokument erlaubt sind. Der Standardwert ist [PdfPermissions.DISALLOW\_ALL](../../com.aspose.words/pdfpermissions/\#DISALLOW-ALL).

 **Examples:** 

Zeigt, wie Berechtigungen für ein gespeichertes PDF-Dokument festgelegt werden.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende  int  Wert. Der Wert muss eine bitweise Kombination von [PdfPermissions](../../com.aspose.words/pdfpermissions/) Konstanten sein. |

### setUserPassword(String value) {#setUserPassword-java.lang.String}
```
public void setUserPassword(String value)
```


Gibt das Benutzerpasswort an, das zum Öffnen des verschlüsselten PDF-Dokuments erforderlich ist.

 **Remarks:** 

Das Benutzerpasswort wird zum Öffnen eines verschlüsselten PDF-Dokuments zum Anzeigen benötigt. Die in [getPermissions()](../../com.aspose.words/pdfencryptiondetails/\#getPermissions) / [setPermissions(int)](../../com.aspose.words/pdfencryptiondetails/\#setPermissions-int) angegebenen Berechtigungen werden von der Lesesoftware durchgesetzt.

Das Benutzerpasswort kann  null  oder ein leerer String sein; in diesem Fall wird beim Öffnen des PDF-Dokuments kein Passwort vom Benutzer verlangt. Das Benutzerpasswort darf nicht dasselbe wie das Besitzerpasswort sein.

 **Examples:** 

Zeigt, wie Berechtigungen für ein gespeichertes PDF-Dokument festgelegt werden.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

