---
title: "FileFormatInfo"
linktitle: "FileFormatInfo"
second_title: "Aspose.Words per Java"
description: "Contiene i dati restituiti dai metodi di rilevamento del formato del documento di FileFormatUtil in Java."
type: docs
weight: 309
url: /it/java/com.aspose.words/fileformatinfo/
---

**Inheritance:**
java.lang.Object
```
public class FileFormatInfo
```

Contiene i dati restituiti dai metodi di rilevamento del formato del documento di [FileFormatUtil](../../com.aspose.words/fileformatutil/).

Per saperne di più, visita l'articolo della documentazione [ Detect File Format and Check Format Compatibility ][Detect File Format and Check Format Compatibility].

 **Remarks:** 

Non si creano istanze di questa classe direttamente. Gli oggetti di questa classe sono restituiti dai metodi **M:Aspose.Words.FileFormatUtil.DetectFileFormat(System.IO.Stream)**.

 **Examples:** 

Mostra come utilizzare la classe FileFormatUtil per rilevare il formato del documento e la crittografia.

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

Mostra come utilizzare la classe FileFormatUtil per rilevare il formato del documento e la presenza di firme digitali.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getEncoding()](#getEncoding) | Restituisce la codifica rilevata, se applicabile al formato del documento corrente. |
| [getLoadFormat()](#getLoadFormat) | Restituisce il formato del documento rilevato. |
| [hasDigitalSignature()](#hasDigitalSignature) | Restituisce  true  se questo documento contiene una firma digitale. |
| [hasMacros()](#hasMacros) | Restituisce  true  se questo documento contiene macro VBA. |
| [isEncrypted()](#isEncrypted) | Restituisce  true  se il documento è crittografato e richiede una password per l'apertura. |
### getEncoding() {#getEncoding}
```
public Charset getEncoding()
```


Restituisce la codifica rilevata, se applicabile al formato del documento corrente. Al momento rileva la codifica solo per i documenti HTML.

 **Examples:** 

Mostra come rilevare la codifica in un file HTML.

```

 FileFormatInfo info = FileFormatUtil.detectFileFormat(getMyDir() + "Document.html");

 Assert.assertEquals(LoadFormat.HTML, info.getLoadFormat());

 // The Encoding property is used only when we create a FileFormatInfo object for an html document.
 Assert.assertEquals("windows-1252", info.getEncoding().name());
 
```

**Returns:**
java.nio.charset.Charset - La codifica rilevata, se applicabile al formato del documento corrente.
### getLoadFormat() {#getLoadFormat}
```
public int getLoadFormat()
```


Restituisce il formato del documento rilevato.

 **Remarks:** 

Quando un documento OOXML è crittografato, non è possibile determinare se si tratta di un documento Excel, Word o PowerPoint senza prima decrittarlo, quindi per un documento OOXML crittografato questa proprietà restituirà sempre [LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX).

 **Examples:** 

Mostra come utilizzare la classe FileFormatUtil per rilevare il formato del documento e la crittografia.

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

Mostra come utilizzare la classe FileFormatUtil per rilevare il formato del documento e la presenza di firme digitali.

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

Mostra come utilizzare i metodi di FileFormatUtil per rilevare il formato di un documento.

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
int - Il formato del documento rilevato. Il valore restituito è una delle costanti di [LoadFormat](../../com.aspose.words/loadformat/).
### hasDigitalSignature() {#hasDigitalSignature}
```
public boolean hasDigitalSignature()
```


Restituisce  true  se questo documento contiene una firma digitale. Questa proprietà indica semplicemente che una firma digitale è presente su un documento, ma non specifica se la firma è valida o meno.

 **Remarks:** 

Questa proprietà esiste per aiutarti a distinguere i documenti firmati digitalmente da quelli non firmati. Se utilizzi Aspose.Words per modificare e salvare un documento firmato digitalmente, la firma digitale verrà persa. Questo è previsto, poiché una firma digitale serve a garantire l'autenticità di un documento. Utilizzando questa proprietà puoi rilevare i documenti firmati digitalmente prima di elaborarli allo stesso modo dei documenti normali e adottare qualche azione per evitare la perdita della firma digitale, ad esempio notificare l'utente.

 **Examples:** 

Mostra come utilizzare la classe FileFormatUtil per rilevare il formato del documento e la presenza di firme digitali.

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
boolean -  true  se questo documento contiene una firma digitale.
### hasMacros() {#hasMacros}
```
public boolean hasMacros()
```


Restituisce  true  se questo documento contiene macro VBA.

 **Examples:** 

Mostra come verificare la presenza di macro VBA senza caricare il documento.

```

 FileFormatInfo fileFormatInfo = FileFormatUtil.detectFileFormat(getMyDir() + "Macro.docm");
 Assert.assertTrue(fileFormatInfo.hasMacros());
 
```

**Returns:**
boolean -  true  se questo documento contiene macro VBA.
### isEncrypted() {#isEncrypted}
```
public boolean isEncrypted()
```


Restituisce  true  se il documento è crittografato e richiede una password per l'apertura.

 **Remarks:** 

Questa proprietà esiste per aiutarti a distinguere i documenti crittografati da quelli non crittografati. Se tenti di caricare un documento crittografato con Aspose.Words senza fornire una password, verrà generata un'eccezione. Puoi utilizzare questa proprietà per rilevare se un documento richiede una password e adottare qualche azione prima di caricare il documento, ad esempio chiedere all'utente di inserire una password.

 **Examples:** 

Mostra come utilizzare la classe FileFormatUtil per rilevare il formato del documento e la crittografia.

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
boolean -  true  se il documento è crittografato e richiede una password per l'apertura.
