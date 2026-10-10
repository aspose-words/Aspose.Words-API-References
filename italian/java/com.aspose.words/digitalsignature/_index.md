---
title: "DigitalSignature"
linktitle: "DigitalSignature"
second_title: "Aspose.Words per Java"
description: "Rappresenta una firma digitale su un documento e il risultato della sua verifica in Java."
type: docs
weight: 150
url: /it/java/com.aspose.words/digitalsignature/
---

**Inheritance:**
java.lang.Object
```
public class DigitalSignature
```

Rappresenta una firma digitale su un documento e il risultato della sua verifica.

Per saperne di più, visita l'articolo di documentazione [ Work with Digital Signatures ][Work with Digital Signatures].

 **Examples:** 

Mostra come convalidare e visualizzare le informazioni su ogni firma in un documento.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getApplicationVersion()](#getApplicationVersion) | Ottiene la versione dell'applicazione per la firma digitale. |
| [getCertificateHolder()](#getCertificateHolder) | Restituisce l'oggetto titolare del certificato che contiene il certificato usato per firmare il documento. |
| [getColorDepth()](#getColorDepth) | Ottiene la profondità di colore per la firma digitale. |
| [getComments()](#getComments) | Ottiene il commento sullo scopo della firma. |
| [getHorizontalResolution()](#getHorizontalResolution) | Restituisce la risoluzione orizzontale per la firma digitale. |
| [getIssuerName()](#getIssuerName) | Restituisce il nome distinto del soggetto del certificato emittente. |
| [getOfficeVersion()](#getOfficeVersion) | Restituisce la versione di Office per la firma digitale. |
| [getSignTime()](#getSignTime) | Ottiene l'ora in cui il documento è stato firmato. |
| [getSignatureType()](#getSignatureType) | Restituisce il tipo della firma digitale. |
| [getSignatureValue()](#getSignatureValue) | Restituisce un array di byte che rappresenta il valore della firma. |
| [getSubjectName()](#getSubjectName) | Restituisce il nome distinto del soggetto del certificato utilizzato per firmare il documento. |
| [getVerticalResolution()](#getVerticalResolution) | Restituisce la risoluzione verticale per la firma digitale. |
| [getWindowsVersion()](#getWindowsVersion) | Restituisce la versione di Windows per la firma digitale. |
| [isValid()](#isValid) | Restituisce  true  se questa firma digitale è valida e il documento non è stato manomesso. |
| [toString()](#toString) | Restituisce una stringa leggibile che visualizza il valore di questo oggetto. |
### getApplicationVersion() {#getApplicationVersion}
```
public String getApplicationVersion()
```


Ottiene la versione dell'applicazione per la firma digitale.

**Returns:**
java.lang.String - La versione dell'applicazione per la firma digitale.
### getCertificateHolder() {#getCertificateHolder}
```
public CertificateHolder getCertificateHolder()
```


Restituisce l'oggetto titolare del certificato che contiene il certificato usato per firmare il documento.

 **Examples:** 

Mostra come firmare documenti con certificati X.509.

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


Ottiene la profondità di colore per la firma digitale.

**Returns:**
int - La profondità di colore per la firma digitale.
### getComments() {#getComments}
```
public String getComments()
```


Ottiene il commento sullo scopo della firma.

 **Examples:** 

Mostra come convalidare e visualizzare le informazioni su ogni firma in un documento.

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
java.lang.String - Il commento sullo scopo della firma.
### getHorizontalResolution() {#getHorizontalResolution}
```
public int getHorizontalResolution()
```


Restituisce la risoluzione orizzontale per la firma digitale.

**Returns:**
int - La risoluzione orizzontale per la firma digitale.
### getIssuerName() {#getIssuerName}
```
public String getIssuerName()
```


Restituisce il nome distinto del soggetto del certificato emittente.

 **Examples:** 

Mostra come firmare documenti con certificati X.509.

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
java.lang.String - Il nome distinto del soggetto del certificato emittente.
### getOfficeVersion() {#getOfficeVersion}
```
public String getOfficeVersion()
```


Restituisce la versione di Office per la firma digitale.

**Returns:**
java.lang.String - La versione di Office per la firma digitale.
### getSignTime() {#getSignTime}
```
public Date getSignTime()
```


Ottiene l'ora in cui il documento è stato firmato.

 **Examples:** 

Mostra come convalidare e visualizzare le informazioni su ogni firma in un documento.

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
java.util.Date - L'ora in cui il documento è stato firmato.
### getSignatureType() {#getSignatureType}
```
public int getSignatureType()
```


Restituisce il tipo della firma digitale.

 **Examples:** 

Mostra come convalidare e visualizzare le informazioni su ogni firma in un documento.

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
int - Il tipo della firma digitale. Il valore restituito è una delle costanti [DigitalSignatureType](../../com.aspose.words/digitalsignaturetype/).
### getSignatureValue() {#getSignatureValue}
```
public byte[] getSignatureValue()
```


Restituisce un array di byte che rappresenta il valore della firma.

 **Examples:** 

Mostra come ottenere il valore di una firma digitale da un documento firmato digitalmente.

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
byte[] - Un array di byte che rappresenta il valore di una firma.
### getSubjectName() {#getSubjectName}
```
public String getSubjectName()
```


Restituisce il nome distinto del soggetto del certificato utilizzato per firmare il documento.

 **Examples:** 

Mostra come firmare documenti con certificati X.509.

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
java.lang.String - Il nome distinto del soggetto del certificato utilizzato per firmare il documento.
### getVerticalResolution() {#getVerticalResolution}
```
public int getVerticalResolution()
```


Restituisce la risoluzione verticale per la firma digitale.

**Returns:**
int - La risoluzione verticale per la firma digitale.
### getWindowsVersion() {#getWindowsVersion}
```
public String getWindowsVersion()
```


Restituisce la versione di Windows per la firma digitale.

**Returns:**
java.lang.String - La versione di Windows per la firma digitale.
### isValid() {#isValid}
```
public boolean isValid()
```


Restituisce  true  se questa firma digitale è valida e il documento non è stato manomesso.

 **Examples:** 

Mostra come convalidare e visualizzare le informazioni su ogni firma in un documento.

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
boolean -  true  se questa firma digitale è valida e il documento non è stato manomesso.
### toString() {#toString}
```
public String toString()
```


Restituisce una stringa leggibile che visualizza il valore di questo oggetto.

**Returns:**
java.lang.String
