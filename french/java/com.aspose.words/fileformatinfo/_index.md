---
title: "FileFormatInfo"
linktitle: "FileFormatInfo"
second_title: "Aspose.Words pour Java"
description: "Contient les données renvoyées par les méthodes de détection du format de document de FileFormatUtil en Java."
type: docs
weight: 309
url: /fr/java/com.aspose.words/fileformatinfo/
---

**Inheritance:**
java.lang.Object
```
public class FileFormatInfo
```

Contient les données renvoyées par les méthodes de détection du format de document de [FileFormatUtil](../../com.aspose.words/fileformatutil/).

Pour en savoir plus, consultez l'article de documentation [ Detect File Format and Check Format Compatibility ][Detect File Format and Check Format Compatibility].

 **Remarks:** 

Vous ne créez pas d'instances de cette classe directement. Les objets de cette classe sont renvoyés par les méthodes **M:Aspose.Words.FileFormatUtil.DetectFileFormat(System.IO.Stream)**.

 **Examples:** 

Montre comment utiliser la classe FileFormatUtil pour détecter le format du document et le chiffrement.

```

 Document doc = new Document();

 // Configure a SaveOptions object to encrypt the document
 // with a password when we save it, and then save the document.
 OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.ODT);
 saveOptions.setPassword("MyPassword");

 doc.save(getArtifactsDir() + "File.DetectDocumentEncryption.odt", saveOptions);

 // Verify the file type of our document, and its encryption status.
 FileFormatInfo info = FileFormatUtil.detectFileFormat(getArtifactsDir() + "File.DetectDocumentEncryption.odt");

 Assert.assertEquals(".odt", FileFormatUtil.loadFormatToExtension(info.getLoadFormat()));
 Assert.assertTrue(info.isEncrypted());
 
```

Montre comment utiliser la classe FileFormatUtil pour détecter le format du document et la présence de signatures numériques.

```

 // Use a FileFormatInfo instance to verify that a document is not digitally signed.
 FileFormatInfo info = FileFormatUtil.detectFileFormat(getMyDir() + "Document.docx");

 Assert.assertEquals(".docx", FileFormatUtil.loadFormatToExtension(info.getLoadFormat()));
 Assert.assertFalse(info.hasDigitalSignature());

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw", null);
 DigitalSignatureUtil.sign(getMyDir() + "Document.docx", getArtifactsDir() + "File.DetectDigitalSignatures.docx",
         certificateHolder);

 // Use a new FileFormatInstance to confirm that it is signed.
 info = FileFormatUtil.detectFileFormat(getArtifactsDir() + "File.DetectDigitalSignatures.docx");

 Assert.assertTrue(info.hasDigitalSignature());

 // We can load and access the signatures of a signed document in a collection like this.
 Assert.assertEquals(1, DigitalSignatureUtil.loadSignatures(getArtifactsDir() + "File.DetectDigitalSignatures.docx").getCount());
 
```


[Detect File Format and Check Format Compatibility]: https://docs.aspose.com/words/java/detect-file-format-and-check-format-compatibility/
## Méthodes

| Méthode | Description |
| --- | --- |
| [getEncoding()](#getEncoding) | Obtient l'encodage détecté si applicable au format du document actuel. |
| [getLoadFormat()](#getLoadFormat) | Obtient le format de document détecté. |
| [hasDigitalSignature()](#hasDigitalSignature) | Renvoie  true  si ce document contient une signature numérique. |
| [hasMacros()](#hasMacros) | Renvoie  true  si ce document contient des macros VBA. |
| [isEncrypted()](#isEncrypted) | Renvoie  true  si le document est chiffré et nécessite un mot de passe pour être ouvert. |
### getEncoding() {#getEncoding}
```
public Charset getEncoding()
```


Obtient l'encodage détecté si applicable au format du document actuel. Pour le moment, il ne détecte l'encodage que pour les documents HTML.

 **Examples:** 

Montre comment détecter l'encodage dans un fichier HTML.

```

 FileFormatInfo info = FileFormatUtil.detectFileFormat(getMyDir() + "Document.html");

 Assert.assertEquals(LoadFormat.HTML, info.getLoadFormat());

 // The Encoding property is used only when we create a FileFormatInfo object for an html document.
 Assert.assertEquals("windows-1252", info.getEncoding().name());
 
```

**Returns:**
java.nio.charset.Charset - L'encodage détecté si applicable au format du document actuel.
### getLoadFormat() {#getLoadFormat}
```
public int getLoadFormat()
```


Obtient le format de document détecté.

 **Remarks:** 

Lorsqu'un document OOXML est chiffré, il n'est pas possible de déterminer s'il s'agit d'un document Excel, Word ou PowerPoint sans le déchiffrer au préalable ; ainsi, pour un document OOXML chiffré, cette propriété renverra toujours [LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX).

 **Examples:** 

Montre comment utiliser la classe FileFormatUtil pour détecter le format du document et le chiffrement.

```

 Document doc = new Document();

 // Configure a SaveOptions object to encrypt the document
 // with a password when we save it, and then save the document.
 OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.ODT);
 saveOptions.setPassword("MyPassword");

 doc.save(getArtifactsDir() + "File.DetectDocumentEncryption.odt", saveOptions);

 // Verify the file type of our document, and its encryption status.
 FileFormatInfo info = FileFormatUtil.detectFileFormat(getArtifactsDir() + "File.DetectDocumentEncryption.odt");

 Assert.assertEquals(".odt", FileFormatUtil.loadFormatToExtension(info.getLoadFormat()));
 Assert.assertTrue(info.isEncrypted());
 
```

Montre comment utiliser la classe FileFormatUtil pour détecter le format du document et la présence de signatures numériques.

```

 // Use a FileFormatInfo instance to verify that a document is not digitally signed.
 FileFormatInfo info = FileFormatUtil.detectFileFormat(getMyDir() + "Document.docx");

 Assert.assertEquals(".docx", FileFormatUtil.loadFormatToExtension(info.getLoadFormat()));
 Assert.assertFalse(info.hasDigitalSignature());

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw", null);
 DigitalSignatureUtil.sign(getMyDir() + "Document.docx", getArtifactsDir() + "File.DetectDigitalSignatures.docx",
         certificateHolder);

 // Use a new FileFormatInstance to confirm that it is signed.
 info = FileFormatUtil.detectFileFormat(getArtifactsDir() + "File.DetectDigitalSignatures.docx");

 Assert.assertTrue(info.hasDigitalSignature());

 // We can load and access the signatures of a signed document in a collection like this.
 Assert.assertEquals(1, DigitalSignatureUtil.loadSignatures(getArtifactsDir() + "File.DetectDigitalSignatures.docx").getCount());
 
```

Montre comment utiliser les méthodes de FileFormatUtil pour détecter le format d'un document.

```

 // Load a document from a file that is missing a file extension, and then detect its file format.
 FileInputStream docStream = new FileInputStream(getMyDir() + "Word document with missing file extension");

 FileFormatInfo info = FileFormatUtil.detectFileFormat(docStream);

 int loadFormat = info.getLoadFormat();

 Assert.assertEquals(LoadFormat.DOC, loadFormat);

 // Below are two methods of converting a LoadFormat to its corresponding SaveFormat.
 // 1 -  Get the file extension string for the LoadFormat, then get the corresponding SaveFormat from that string:
 String fileExtension = FileFormatUtil.loadFormatToExtension(loadFormat);

 int saveFormat = FileFormatUtil.extensionToSaveFormat(fileExtension);

 // 2 -  Convert the LoadFormat directly to its SaveFormat:
 saveFormat = FileFormatUtil.loadFormatToSaveFormat(loadFormat);

 // Load a document from the stream, and then save it to the automatically detected file extension.
 Document doc = new Document(docStream);

 Assert.assertEquals(".doc", FileFormatUtil.saveFormatToExtension(saveFormat));

 doc.save(getArtifactsDir() + "File.SaveToDetectedFileFormat" + FileFormatUtil.saveFormatToExtension(saveFormat));
 
```

**Returns:**
int - Le format de document détecté. La valeur renvoyée est l'une des constantes de [LoadFormat](../../com.aspose.words/loadformat/).
### hasDigitalSignature() {#hasDigitalSignature}
```
public boolean hasDigitalSignature()
```


Renvoie  true  si ce document contient une signature numérique. Cette propriété indique simplement qu'une signature numérique est présente sur un document, mais ne précise pas si la signature est valide ou non.

 **Remarks:** 

Cette propriété existe pour vous aider à distinguer les documents signés numériquement de ceux qui ne le sont pas. Si vous utilisez Aspose.Words pour modifier et enregistrer un document signé numériquement, la signature numérique sera perdue. C'est ainsi prévu, car une signature numérique sert à garantir l'authenticité d'un document. En utilisant cette propriété, vous pouvez détecter les documents signés numériquement avant de les traiter de la même manière que les documents normaux et prendre une mesure pour éviter la perte de la signature numérique, par exemple en avertissant l'utilisateur.

 **Examples:** 

Montre comment utiliser la classe FileFormatUtil pour détecter le format du document et la présence de signatures numériques.

```

 // Use a FileFormatInfo instance to verify that a document is not digitally signed.
 FileFormatInfo info = FileFormatUtil.detectFileFormat(getMyDir() + "Document.docx");

 Assert.assertEquals(".docx", FileFormatUtil.loadFormatToExtension(info.getLoadFormat()));
 Assert.assertFalse(info.hasDigitalSignature());

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw", null);
 DigitalSignatureUtil.sign(getMyDir() + "Document.docx", getArtifactsDir() + "File.DetectDigitalSignatures.docx",
         certificateHolder);

 // Use a new FileFormatInstance to confirm that it is signed.
 info = FileFormatUtil.detectFileFormat(getArtifactsDir() + "File.DetectDigitalSignatures.docx");

 Assert.assertTrue(info.hasDigitalSignature());

 // We can load and access the signatures of a signed document in a collection like this.
 Assert.assertEquals(1, DigitalSignatureUtil.loadSignatures(getArtifactsDir() + "File.DetectDigitalSignatures.docx").getCount());
 
```

**Returns:**
boolean -  true  si ce document contient une signature numérique.
### hasMacros() {#hasMacros}
```
public boolean hasMacros()
```


Renvoie  true  si ce document contient des macros VBA.

 **Examples:** 

Montre comment vérifier la présence de macros VBA sans charger le document.

```

 FileFormatInfo fileFormatInfo = FileFormatUtil.detectFileFormat(getMyDir() + "Macro.docm");
 Assert.assertTrue(fileFormatInfo.hasMacros());
 
```

**Returns:**
boolean -  true  si ce document contient des macros VBA.
### isEncrypted() {#isEncrypted}
```
public boolean isEncrypted()
```


Renvoie  true  si le document est chiffré et nécessite un mot de passe pour être ouvert.

 **Remarks:** 

Cette propriété existe pour vous aider à distinguer les documents chiffrés de ceux qui ne le sont pas. Si vous essayez de charger un document chiffré avec Aspose.Words sans fournir de mot de passe, une exception sera levée. Vous pouvez utiliser cette propriété pour détecter si un document nécessite un mot de passe et prendre une mesure avant de charger le document, par exemple en invitant l'utilisateur à saisir un mot de passe.

 **Examples:** 

Montre comment utiliser la classe FileFormatUtil pour détecter le format du document et le chiffrement.

```

 Document doc = new Document();

 // Configure a SaveOptions object to encrypt the document
 // with a password when we save it, and then save the document.
 OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.ODT);
 saveOptions.setPassword("MyPassword");

 doc.save(getArtifactsDir() + "File.DetectDocumentEncryption.odt", saveOptions);

 // Verify the file type of our document, and its encryption status.
 FileFormatInfo info = FileFormatUtil.detectFileFormat(getArtifactsDir() + "File.DetectDocumentEncryption.odt");

 Assert.assertEquals(".odt", FileFormatUtil.loadFormatToExtension(info.getLoadFormat()));
 Assert.assertTrue(info.isEncrypted());
 
```

**Returns:**
boolean -  true  si le document est chiffré et nécessite un mot de passe pour être ouvert.
