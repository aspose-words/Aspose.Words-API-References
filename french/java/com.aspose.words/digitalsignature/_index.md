---
title: "DigitalSignature"
linktitle: "DigitalSignature"
second_title: "Aspose.Words pour Java"
description: "Représente une signature numérique sur un document et le résultat de sa vérification en Java."
type: docs
weight: 150
url: /fr/java/com.aspose.words/digitalsignature/
---

**Inheritance:**
java.lang.Object
```
public class DigitalSignature
```

Représente une signature numérique sur un document et le résultat de sa vérification.

Pour en savoir plus, consultez l'article de documentation [ Work with Digital Signatures ][Work with Digital Signatures].

 **Examples:** 

Montre comment valider et afficher les informations sur chaque signature dans un document.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [getApplicationVersion()](#getApplicationVersion) | Obtient la version de l'application pour la signature numérique. |
| [getCertificateHolder()](#getCertificateHolder) | Renvoie l'objet détenteur du certificat qui contient le certificat utilisé pour signer le document. |
| [getColorDepth()](#getColorDepth) | Obtient la profondeur de couleur pour la signature numérique. |
| [getComments()](#getComments) | Obtient le commentaire du but de la signature. |
| [getHorizontalResolution()](#getHorizontalResolution) | Obtient la résolution horizontale de la signature numérique. |
| [getIssuerName()](#getIssuerName) | Renvoie le nom distinctif du sujet du certificat de l'émetteur. |
| [getOfficeVersion()](#getOfficeVersion) | Obtient la version Office de la signature numérique. |
| [getSignTime()](#getSignTime) | Obtient l'heure à laquelle le document a été signé. |
| [getSignatureType()](#getSignatureType) | Obtient le type de la signature numérique. |
| [getSignatureValue()](#getSignatureValue) | Obtient un tableau d'octets représentant une valeur de signature. |
| [getSubjectName()](#getSubjectName) | Renvoie le nom distinctif du sujet du certificat qui a été utilisé pour signer le document. |
| [getVerticalResolution()](#getVerticalResolution) | Obtient la résolution verticale de la signature numérique. |
| [getWindowsVersion()](#getWindowsVersion) | Obtient la version Windows de la signature numérique. |
| [isValid()](#isValid) | Renvoie  true  si cette signature numérique est valide et que le document n'a pas été altéré. |
| [toString()](#toString) | Renvoie une chaîne conviviale qui affiche la valeur de cet objet. |
### getApplicationVersion() {#getApplicationVersion}
```
public String getApplicationVersion()
```


Obtient la version de l'application pour la signature numérique.

**Returns:**
java.lang.String - La version de l'application pour la signature numérique.
### getCertificateHolder() {#getCertificateHolder}
```
public CertificateHolder getCertificateHolder()
```


Renvoie l'objet détenteur du certificat qui contient le certificat utilisé pour signer le document.

 **Examples:** 

Montre comment signer des documents avec des certificats X.509.

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


Obtient la profondeur de couleur pour la signature numérique.

**Returns:**
int - La profondeur de couleur de la signature numérique.
### getComments() {#getComments}
```
public String getComments()
```


Obtient le commentaire du but de la signature.

 **Examples:** 

Montre comment valider et afficher les informations sur chaque signature dans un document.

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
java.lang.String - Le commentaire de l'objectif de signature.
### getHorizontalResolution() {#getHorizontalResolution}
```
public int getHorizontalResolution()
```


Obtient la résolution horizontale de la signature numérique.

**Returns:**
int - La résolution horizontale de la signature numérique.
### getIssuerName() {#getIssuerName}
```
public String getIssuerName()
```


Renvoie le nom distinctif du sujet du certificat de l'émetteur.

 **Examples:** 

Montre comment signer des documents avec des certificats X.509.

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
java.lang.String - Le nom distinctif du sujet du certificat émetteur.
### getOfficeVersion() {#getOfficeVersion}
```
public String getOfficeVersion()
```


Obtient la version Office de la signature numérique.

**Returns:**
java.lang.String - La version Office pour la signature numérique.
### getSignTime() {#getSignTime}
```
public Date getSignTime()
```


Obtient l'heure à laquelle le document a été signé.

 **Examples:** 

Montre comment valider et afficher les informations sur chaque signature dans un document.

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
java.util.Date - L'heure à laquelle le document a été signé.
### getSignatureType() {#getSignatureType}
```
public int getSignatureType()
```


Obtient le type de la signature numérique.

 **Examples:** 

Montre comment valider et afficher les informations sur chaque signature dans un document.

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
int - Le type de la signature numérique. La valeur retournée est l'une des constantes [DigitalSignatureType](../../com.aspose.words/digitalsignaturetype/).
### getSignatureValue() {#getSignatureValue}
```
public byte[] getSignatureValue()
```


Obtient un tableau d'octets représentant une valeur de signature.

 **Examples:** 

Montre comment obtenir une valeur de signature numérique à partir d'un document signé numériquement.

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
byte[] - Un tableau d'octets représentant une valeur de signature.
### getSubjectName() {#getSubjectName}
```
public String getSubjectName()
```


Renvoie le nom distinctif du sujet du certificat qui a été utilisé pour signer le document.

 **Examples:** 

Montre comment signer des documents avec des certificats X.509.

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
java.lang.String - Le nom distinctif du sujet du certificat qui a été utilisé pour signer le document.
### getVerticalResolution() {#getVerticalResolution}
```
public int getVerticalResolution()
```


Obtient la résolution verticale de la signature numérique.

**Returns:**
int - La résolution verticale pour la signature numérique.
### getWindowsVersion() {#getWindowsVersion}
```
public String getWindowsVersion()
```


Obtient la version Windows de la signature numérique.

**Returns:**
java.lang.String - La version Windows pour la signature numérique.
### isValid() {#isValid}
```
public boolean isValid()
```


Renvoie  true  si cette signature numérique est valide et que le document n'a pas été altéré.

 **Examples:** 

Montre comment valider et afficher les informations sur chaque signature dans un document.

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
boolean -  true  si cette signature numérique est valide et que le document n'a pas été altéré.
### toString() {#toString}
```
public String toString()
```


Renvoie une chaîne conviviale qui affiche la valeur de cet objet.

**Returns:**
java.lang.String
