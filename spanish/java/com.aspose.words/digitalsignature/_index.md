---
title: "DigitalSignature"
linktitle: "DigitalSignature"
second_title: "Aspose.Words para Java"
description: "Representa una firma digital en un documento y el resultado de su verificación en Java."
type: docs
weight: 150
url: /es/java/com.aspose.words/digitalsignature/
---

**Inheritance:**
java.lang.Object
```
public class DigitalSignature
```

Representa una firma digital en un documento y el resultado de su verificación.

Para obtener más información, visite el artículo de documentación [ Work with Digital Signatures ][Work with Digital Signatures].

 **Examples:** 

Muestra cómo validar y mostrar información sobre cada firma en un documento.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [getApplicationVersion()](#getApplicationVersion) | Obtiene la versión de la aplicación para la firma digital. |
| [getCertificateHolder()](#getCertificateHolder) | Devuelve el objeto titular del certificado que contiene el certificado utilizado para firmar el documento. |
| [getColorDepth()](#getColorDepth) | Obtiene la profundidad de color para la firma digital. |
| [getComments()](#getComments) | Obtiene el comentario del propósito de la firma. |
| [getHorizontalResolution()](#getHorizontalResolution) | Obtiene la resolución horizontal para la firma digital. |
| [getIssuerName()](#getIssuerName) | Devuelve el nombre distinguido del sujeto del emisor del certificado. |
| [getOfficeVersion()](#getOfficeVersion) | Obtiene la versión de Office para la firma digital. |
| [getSignTime()](#getSignTime) | Obtiene la hora en que se firmó el documento. |
| [getSignatureType()](#getSignatureType) | Obtiene el tipo de la firma digital. |
| [getSignatureValue()](#getSignatureValue) | Obtiene una matriz de bytes que representa un valor de firma. |
| [getSubjectName()](#getSubjectName) | Devuelve el nombre distinguido del sujeto del certificado que se utilizó para firmar el documento. |
| [getVerticalResolution()](#getVerticalResolution) | Obtiene la resolución vertical para la firma digital. |
| [getWindowsVersion()](#getWindowsVersion) | Obtiene la versión de Windows para la firma digital. |
| [isValid()](#isValid) | Devuelve  true  si esta firma digital es válida y el documento no ha sido manipulado. |
| [toString()](#toString) | Devuelve una cadena amigable que muestra el valor de este objeto. |
### getApplicationVersion() {#getApplicationVersion}
```
public String getApplicationVersion()
```


Obtiene la versión de la aplicación para la firma digital.

**Returns:**
java.lang.String - La versión de la aplicación para la firma digital.
### getCertificateHolder() {#getCertificateHolder}
```
public CertificateHolder getCertificateHolder()
```


Devuelve el objeto titular del certificado que contiene el certificado utilizado para firmar el documento.

 **Examples:** 

Muestra cómo firmar documentos con certificados X.509.

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


Obtiene la profundidad de color para la firma digital.

**Returns:**
int - La profundidad de color para la firma digital.
### getComments() {#getComments}
```
public String getComments()
```


Obtiene el comentario del propósito de la firma.

 **Examples:** 

Muestra cómo validar y mostrar información sobre cada firma en un documento.

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
java.lang.String - El comentario del propósito de la firma.
### getHorizontalResolution() {#getHorizontalResolution}
```
public int getHorizontalResolution()
```


Obtiene la resolución horizontal para la firma digital.

**Returns:**
int - La resolución horizontal para la firma digital.
### getIssuerName() {#getIssuerName}
```
public String getIssuerName()
```


Devuelve el nombre distinguido del sujeto del emisor del certificado.

 **Examples:** 

Muestra cómo firmar documentos con certificados X.509.

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
java.lang.String - El nombre distinguido del sujeto del certificado emisor.
### getOfficeVersion() {#getOfficeVersion}
```
public String getOfficeVersion()
```


Obtiene la versión de Office para la firma digital.

**Returns:**
java.lang.String - La versión de Office para la firma digital.
### getSignTime() {#getSignTime}
```
public Date getSignTime()
```


Obtiene la hora en que se firmó el documento.

 **Examples:** 

Muestra cómo validar y mostrar información sobre cada firma en un documento.

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
java.util.Date - La hora en que se firmó el documento.
### getSignatureType() {#getSignatureType}
```
public int getSignatureType()
```


Obtiene el tipo de la firma digital.

 **Examples:** 

Muestra cómo validar y mostrar información sobre cada firma en un documento.

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
int - El tipo de la firma digital. El valor devuelto es una de las constantes [DigitalSignatureType](../../com.aspose.words/digitalsignaturetype/).
### getSignatureValue() {#getSignatureValue}
```
public byte[] getSignatureValue()
```


Obtiene una matriz de bytes que representa un valor de firma.

 **Examples:** 

Muestra cómo obtener un valor de firma digital de un documento firmado digitalmente.

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
byte[] - Una matriz de bytes que representa un valor de firma.
### getSubjectName() {#getSubjectName}
```
public String getSubjectName()
```


Devuelve el nombre distinguido del sujeto del certificado que se utilizó para firmar el documento.

 **Examples:** 

Muestra cómo firmar documentos con certificados X.509.

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
java.lang.String - El nombre distinguido del sujeto del certificado que se utilizó para firmar el documento.
### getVerticalResolution() {#getVerticalResolution}
```
public int getVerticalResolution()
```


Obtiene la resolución vertical para la firma digital.

**Returns:**
int - La resolución vertical para la firma digital.
### getWindowsVersion() {#getWindowsVersion}
```
public String getWindowsVersion()
```


Obtiene la versión de Windows para la firma digital.

**Returns:**
java.lang.String - La versión de Windows para la firma digital.
### isValid() {#isValid}
```
public boolean isValid()
```


Devuelve  true  si esta firma digital es válida y el documento no ha sido manipulado.

 **Examples:** 

Muestra cómo validar y mostrar información sobre cada firma en un documento.

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
boolean -  true  si esta firma digital es válida y el documento no ha sido manipulado.
### toString() {#toString}
```
public String toString()
```


Devuelve una cadena amigable que muestra el valor de este objeto.

**Returns:**
java.lang.String
