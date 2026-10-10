---
title: "DigitalSignature"
linktitle: "DigitalSignature"
second_title: "Aspose.Words für Java"
description: "Stellt eine digitale Signatur in einem Dokument und das Ergebnis ihrer Verifizierung in Java dar."
type: docs
weight: 150
url: /de/java/com.aspose.words/digitalsignature/
---

**Inheritance:**
java.lang.Object
```
public class DigitalSignature
```

Stellt eine digitale Signatur in einem Dokument und das Ergebnis ihrer Verifizierung dar.

Weitere Informationen finden Sie im Dokumentationsartikel [ Work with Digital Signatures ][Work with Digital Signatures].

 **Examples:** 

Zeigt, wie man die Gültigkeit prüft und Informationen zu jeder Signatur in einem Dokument anzeigt.

```

 Document doc = new Document(getMyDir() + "Digitally signed.docx");

 for (DigitalSignature signature : doc.getDigitalSignatures()) {
     System.out.println("*** Signature Found ***");
     System.out.println("Is valid: " + signature.isValid());
     // This property is available in MS Word documents only
     System.out.println("Reason for signing: " + signature.getComments());
     System.out.println("Signature type: " + signature.getSignatureType());
     System.out.println("Time of signing: " + signature.getSignTime());
     System.out.println("Subject name: " + signature.getSubjectName());
     System.out.println("Issuer name: " + signature.getIssuerName());
     System.out.println();
 }
 
```


[Work with Digital Signatures]: https://docs.aspose.com/words/java/working-with-digital-signatures/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getApplicationVersion()](#getApplicationVersion) | Gibt die Anwendungsversion für die digitale Signatur zurück. |
| [getCertificateHolder()](#getCertificateHolder) | Gibt das Zertifikatsinhaber-Objekt zurück, das das Zertifikat enthält, das zum Signieren des Dokuments verwendet wurde. |
| [getColorDepth()](#getColorDepth) | Ermittelt die Farbtiefe für die digitale Signatur. |
| [getComments()](#getComments) | Liest den Kommentar zum Signaturzweck. |
| [getHorizontalResolution()](#getHorizontalResolution) | Ermittelt die horizontale Auflösung für die digitale Signatur. |
| [getIssuerName()](#getIssuerName) | Gibt den Distinguished Name des Zertifikatsausstellers zurück. |
| [getOfficeVersion()](#getOfficeVersion) | Ermittelt die Office-Version für die digitale Signatur. |
| [getSignTime()](#getSignTime) | Liest die Zeit, zu der das Dokument signiert wurde. |
| [getSignatureType()](#getSignatureType) | Liest den Typ der digitalen Signatur. |
| [getSignatureValue()](#getSignatureValue) | Liest ein Byte-Array, das einen Signaturwert darstellt. |
| [getSubjectName()](#getSubjectName) | Gibt den Distinguished Name des Zertifikats zurück, das zum Signieren des Dokuments verwendet wurde. |
| [getVerticalResolution()](#getVerticalResolution) | Ermittelt die vertikale Auflösung für die digitale Signatur. |
| [getWindowsVersion()](#getWindowsVersion) | Ermittelt die Windows-Version für die digitale Signatur. |
| [isValid()](#isValid) | Gibt  true  zurück, wenn diese digitale Signatur gültig ist und das Dokument nicht manipuliert wurde. |
| [toString()](#toString) | Gibt eine benutzerfreundliche Zeichenkette zurück, die den Wert dieses Objekts anzeigt. |
### getApplicationVersion() {#getApplicationVersion}
```
public String getApplicationVersion()
```


Gibt die Anwendungsversion für die digitale Signatur zurück.

**Returns:**
java.lang.String - Die Anwendungs-Version für die digitale Signatur.
### getCertificateHolder() {#getCertificateHolder}
```
public CertificateHolder getCertificateHolder()
```


Gibt das Zertifikatsinhaber-Objekt zurück, das das Zertifikat enthält, das zum Signieren des Dokuments verwendet wurde.

 **Examples:** 

Zeigt, wie man Dokumente mit X.509‑Zertifikaten signiert.

```

 // Verify that a document is not signed.
 Assert.assertFalse(FileFormatUtil.detectFileFormat(getMyDir() + "Document.docx").hasDigitalSignature());

 // Create a CertificateHolder object from a PKCS12 file, which we will use to sign the document.
 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw", null);

 SignOptions signOptions = new SignOptions();
 signOptions.setSignTime(new Date());

 // There are two ways of saving a signed copy of a document to the local file system:
 // 1 - Designate a document by a local system filename and save a signed copy at a location specified by another filename.
 DigitalSignatureUtil.sign(getMyDir() + "Document.docx", getArtifactsDir() + "Document.DigitalSignature.docx",
         certificateHolder, signOptions);

 Assert.assertTrue(FileFormatUtil.detectFileFormat(getArtifactsDir() + "Document.DigitalSignature.docx").hasDigitalSignature());

 // 2 - Take a document from a stream, and save a signed copy to another stream.
 InputStream inDoc = new FileInputStream(getMyDir() + "Document.docx");
 try {
     OutputStream outDoc = new FileOutputStream(getArtifactsDir() + "Document.DigitalSignature.docx");
     try {
         DigitalSignatureUtil.sign(inDoc, outDoc, certificateHolder);
     } finally {
         if (outDoc != null) outDoc.close();
     }
 } finally {
     if (inDoc != null) inDoc.close();
 }

 Assert.assertTrue(FileFormatUtil.detectFileFormat(getArtifactsDir() + "Document.DigitalSignature.docx").hasDigitalSignature());

 // Please verify that all of the document's digital signatures are valid and check their details.
 Document signedDoc = new Document(getArtifactsDir() + "Document.DigitalSignature.docx");
 DigitalSignatureCollection digitalSignatureCollection = signedDoc.getDigitalSignatures();

 Assert.assertTrue(digitalSignatureCollection.isValid());
 Assert.assertEquals(1, digitalSignatureCollection.getCount());
 Assert.assertEquals(DigitalSignatureType.XML_DSIG, digitalSignatureCollection.get(0).getSignatureType());
 Assert.assertEquals("CN=Morzal.Me", signedDoc.getDigitalSignatures().get(0).getIssuerName());
 Assert.assertEquals("CN=Morzal.Me", signedDoc.getDigitalSignatures().get(0).getSubjectName());
 
```

**Returns:**
[CertificateHolder](../../com.aspose.words/certificateholder/) - The certificate holder object that contains the certificate was used to sign the document.
### getColorDepth() {#getColorDepth}
```
public int getColorDepth()
```


Ermittelt die Farbtiefe für die digitale Signatur.

**Returns:**
int - Die Farbtiefe für die digitale Signatur.
### getComments() {#getComments}
```
public String getComments()
```


Liest den Kommentar zum Signaturzweck.

 **Examples:** 

Zeigt, wie man die Gültigkeit prüft und Informationen zu jeder Signatur in einem Dokument anzeigt.

```

 Document doc = new Document(getMyDir() + "Digitally signed.docx");

 for (DigitalSignature signature : doc.getDigitalSignatures()) {
     System.out.println("*** Signature Found ***");
     System.out.println("Is valid: " + signature.isValid());
     // This property is available in MS Word documents only
     System.out.println("Reason for signing: " + signature.getComments());
     System.out.println("Signature type: " + signature.getSignatureType());
     System.out.println("Time of signing: " + signature.getSignTime());
     System.out.println("Subject name: " + signature.getSubjectName());
     System.out.println("Issuer name: " + signature.getIssuerName());
     System.out.println();
 }
 
```

**Returns:**
java.lang.String - Der Kommentar zum Signaturzweck.
### getHorizontalResolution() {#getHorizontalResolution}
```
public int getHorizontalResolution()
```


Ermittelt die horizontale Auflösung für die digitale Signatur.

**Returns:**
int - Die horizontale Auflösung für die digitale Signatur.
### getIssuerName() {#getIssuerName}
```
public String getIssuerName()
```


Gibt den Distinguished Name des Zertifikatsausstellers zurück.

 **Examples:** 

Zeigt, wie man Dokumente mit X.509‑Zertifikaten signiert.

```

 // Verify that a document is not signed.
 Assert.assertFalse(FileFormatUtil.detectFileFormat(getMyDir() + "Document.docx").hasDigitalSignature());

 // Create a CertificateHolder object from a PKCS12 file, which we will use to sign the document.
 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw", null);

 SignOptions signOptions = new SignOptions();
 signOptions.setSignTime(new Date());

 // There are two ways of saving a signed copy of a document to the local file system:
 // 1 - Designate a document by a local system filename and save a signed copy at a location specified by another filename.
 DigitalSignatureUtil.sign(getMyDir() + "Document.docx", getArtifactsDir() + "Document.DigitalSignature.docx",
         certificateHolder, signOptions);

 Assert.assertTrue(FileFormatUtil.detectFileFormat(getArtifactsDir() + "Document.DigitalSignature.docx").hasDigitalSignature());

 // 2 - Take a document from a stream, and save a signed copy to another stream.
 InputStream inDoc = new FileInputStream(getMyDir() + "Document.docx");
 try {
     OutputStream outDoc = new FileOutputStream(getArtifactsDir() + "Document.DigitalSignature.docx");
     try {
         DigitalSignatureUtil.sign(inDoc, outDoc, certificateHolder);
     } finally {
         if (outDoc != null) outDoc.close();
     }
 } finally {
     if (inDoc != null) inDoc.close();
 }

 Assert.assertTrue(FileFormatUtil.detectFileFormat(getArtifactsDir() + "Document.DigitalSignature.docx").hasDigitalSignature());

 // Please verify that all of the document's digital signatures are valid and check their details.
 Document signedDoc = new Document(getArtifactsDir() + "Document.DigitalSignature.docx");
 DigitalSignatureCollection digitalSignatureCollection = signedDoc.getDigitalSignatures();

 Assert.assertTrue(digitalSignatureCollection.isValid());
 Assert.assertEquals(1, digitalSignatureCollection.getCount());
 Assert.assertEquals(DigitalSignatureType.XML_DSIG, digitalSignatureCollection.get(0).getSignatureType());
 Assert.assertEquals("CN=Morzal.Me", signedDoc.getDigitalSignatures().get(0).getIssuerName());
 Assert.assertEquals("CN=Morzal.Me", signedDoc.getDigitalSignatures().get(0).getSubjectName());
 
```

**Returns:**
java.lang.String - Der Distinguished Name des Zertifikatsausstellers.
### getOfficeVersion() {#getOfficeVersion}
```
public String getOfficeVersion()
```


Ermittelt die Office-Version für die digitale Signatur.

**Returns:**
java.lang.String - Die Office-Version für die digitale Signatur.
### getSignTime() {#getSignTime}
```
public Date getSignTime()
```


Liest die Zeit, zu der das Dokument signiert wurde.

 **Examples:** 

Zeigt, wie man die Gültigkeit prüft und Informationen zu jeder Signatur in einem Dokument anzeigt.

```

 Document doc = new Document(getMyDir() + "Digitally signed.docx");

 for (DigitalSignature signature : doc.getDigitalSignatures()) {
     System.out.println("*** Signature Found ***");
     System.out.println("Is valid: " + signature.isValid());
     // This property is available in MS Word documents only
     System.out.println("Reason for signing: " + signature.getComments());
     System.out.println("Signature type: " + signature.getSignatureType());
     System.out.println("Time of signing: " + signature.getSignTime());
     System.out.println("Subject name: " + signature.getSubjectName());
     System.out.println("Issuer name: " + signature.getIssuerName());
     System.out.println();
 }
 
```

**Returns:**
java.util.Date - Die Zeit, zu der das Dokument signiert wurde.
### getSignatureType() {#getSignatureType}
```
public int getSignatureType()
```


Liest den Typ der digitalen Signatur.

 **Examples:** 

Zeigt, wie man die Gültigkeit prüft und Informationen zu jeder Signatur in einem Dokument anzeigt.

```

 Document doc = new Document(getMyDir() + "Digitally signed.docx");

 for (DigitalSignature signature : doc.getDigitalSignatures()) {
     System.out.println("*** Signature Found ***");
     System.out.println("Is valid: " + signature.isValid());
     // This property is available in MS Word documents only
     System.out.println("Reason for signing: " + signature.getComments());
     System.out.println("Signature type: " + signature.getSignatureType());
     System.out.println("Time of signing: " + signature.getSignTime());
     System.out.println("Subject name: " + signature.getSubjectName());
     System.out.println("Issuer name: " + signature.getIssuerName());
     System.out.println();
 }
 
```

**Returns:**
int - Der Typ der digitalen Signatur. Der zurückgegebene Wert ist einer der Konstanten von [DigitalSignatureType](../../com.aspose.words/digitalsignaturetype/) Konstanten.
### getSignatureValue() {#getSignatureValue}
```
public byte[] getSignatureValue()
```


Liest ein Byte-Array, das einen Signaturwert darstellt.

 **Examples:** 

Zeigt, wie man einen Signaturwert aus einem digital signierten Dokument erhält.

```

 Document doc = new Document(getMyDir() + "Digitally signed.docx");

 for (DigitalSignature digitalSignature : doc.getDigitalSignatures())
 {
     String signatureValue = Base64.getEncoder().encodeToString(digitalSignature.getSignatureValue());
     Assert.assertEquals("K1cVLLg2kbJRAzT5WK+m++G8eEO+l7S+5ENdjMxxTXkFzGUfvwxREuJdSFj9AbD" +
             "MhnGvDURv9KEhC25DDF1al8NRVR71TF3CjHVZXpYu7edQS5/yLw/k5CiFZzCp1+MmhOdYPcVO+Fm" +
             "+9fKr2iNLeyYB+fgEeZHfTqTFM2WwAqo=", signatureValue);
 }
 
```

**Returns:**
byte[] - Ein Array von Bytes, das einen Signaturwert darstellt.
### getSubjectName() {#getSubjectName}
```
public String getSubjectName()
```


Gibt den Distinguished Name des Zertifikats zurück, das zum Signieren des Dokuments verwendet wurde.

 **Examples:** 

Zeigt, wie man Dokumente mit X.509‑Zertifikaten signiert.

```

 // Verify that a document is not signed.
 Assert.assertFalse(FileFormatUtil.detectFileFormat(getMyDir() + "Document.docx").hasDigitalSignature());

 // Create a CertificateHolder object from a PKCS12 file, which we will use to sign the document.
 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw", null);

 SignOptions signOptions = new SignOptions();
 signOptions.setSignTime(new Date());

 // There are two ways of saving a signed copy of a document to the local file system:
 // 1 - Designate a document by a local system filename and save a signed copy at a location specified by another filename.
 DigitalSignatureUtil.sign(getMyDir() + "Document.docx", getArtifactsDir() + "Document.DigitalSignature.docx",
         certificateHolder, signOptions);

 Assert.assertTrue(FileFormatUtil.detectFileFormat(getArtifactsDir() + "Document.DigitalSignature.docx").hasDigitalSignature());

 // 2 - Take a document from a stream, and save a signed copy to another stream.
 InputStream inDoc = new FileInputStream(getMyDir() + "Document.docx");
 try {
     OutputStream outDoc = new FileOutputStream(getArtifactsDir() + "Document.DigitalSignature.docx");
     try {
         DigitalSignatureUtil.sign(inDoc, outDoc, certificateHolder);
     } finally {
         if (outDoc != null) outDoc.close();
     }
 } finally {
     if (inDoc != null) inDoc.close();
 }

 Assert.assertTrue(FileFormatUtil.detectFileFormat(getArtifactsDir() + "Document.DigitalSignature.docx").hasDigitalSignature());

 // Please verify that all of the document's digital signatures are valid and check their details.
 Document signedDoc = new Document(getArtifactsDir() + "Document.DigitalSignature.docx");
 DigitalSignatureCollection digitalSignatureCollection = signedDoc.getDigitalSignatures();

 Assert.assertTrue(digitalSignatureCollection.isValid());
 Assert.assertEquals(1, digitalSignatureCollection.getCount());
 Assert.assertEquals(DigitalSignatureType.XML_DSIG, digitalSignatureCollection.get(0).getSignatureType());
 Assert.assertEquals("CN=Morzal.Me", signedDoc.getDigitalSignatures().get(0).getIssuerName());
 Assert.assertEquals("CN=Morzal.Me", signedDoc.getDigitalSignatures().get(0).getSubjectName());
 
```

**Returns:**
java.lang.String - Der Distinguished Name des Zertifikats, das zum Signieren des Dokuments verwendet wurde.
### getVerticalResolution() {#getVerticalResolution}
```
public int getVerticalResolution()
```


Ermittelt die vertikale Auflösung für die digitale Signatur.

**Returns:**
int - Die vertikale Auflösung für die digitale Signatur.
### getWindowsVersion() {#getWindowsVersion}
```
public String getWindowsVersion()
```


Ermittelt die Windows-Version für die digitale Signatur.

**Returns:**
java.lang.String - Die Windows-Version für die digitale Signatur.
### isValid() {#isValid}
```
public boolean isValid()
```


Gibt  true  zurück, wenn diese digitale Signatur gültig ist und das Dokument nicht manipuliert wurde.

 **Examples:** 

Zeigt, wie man die Gültigkeit prüft und Informationen zu jeder Signatur in einem Dokument anzeigt.

```

 Document doc = new Document(getMyDir() + "Digitally signed.docx");

 for (DigitalSignature signature : doc.getDigitalSignatures()) {
     System.out.println("*** Signature Found ***");
     System.out.println("Is valid: " + signature.isValid());
     // This property is available in MS Word documents only
     System.out.println("Reason for signing: " + signature.getComments());
     System.out.println("Signature type: " + signature.getSignatureType());
     System.out.println("Time of signing: " + signature.getSignTime());
     System.out.println("Subject name: " + signature.getSubjectName());
     System.out.println("Issuer name: " + signature.getIssuerName());
     System.out.println();
 }
 
```

**Returns:**
boolean -  true  wenn diese digitale Signatur gültig ist und das Dokument nicht manipuliert wurde.
### toString() {#toString}
```
public String toString()
```


Gibt eine benutzerfreundliche Zeichenkette zurück, die den Wert dieses Objekts anzeigt.

**Returns:**
java.lang.String
