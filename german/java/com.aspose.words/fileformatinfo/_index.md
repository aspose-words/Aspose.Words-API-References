---
title: "FileFormatInfo"
linktitle: "FileFormatInfo"
second_title: "Aspose.Words für Java"
description: "Enthält Daten, die von den Dokumentformat-Erkennungsmethoden von FileFormatUtil in Java zurückgegeben werden."
type: docs
weight: 309
url: /de/java/com.aspose.words/fileformatinfo/
---

**Inheritance:**
java.lang.Object
```
public class FileFormatInfo
```

Enthält Daten, die von den Dokumentformat-Erkennungsmethoden von [FileFormatUtil](../../com.aspose.words/fileformatutil/) zurückgegeben werden.

Um mehr zu erfahren, besuchen Sie den [ Detect File Format and Check Format Compatibility ][Detect File Format and Check Format Compatibility] Dokumentationsartikel.

 **Remarks:** 

Sie erstellen keine Instanzen dieser Klasse direkt. Objekte dieser Klasse werden von den **M:Aspose.Words.FileFormatUtil.DetectFileFormat(System.IO.Stream)**-Methoden zurückgegeben.

 **Examples:** 

Zeigt, wie man die Klasse FileFormatUtil verwendet, um das Dokumentformat und die Verschlüsselung zu erkennen.

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

Zeigt, wie man die Klasse FileFormatUtil verwendet, um das Dokumentformat und das Vorhandensein digitaler Signaturen zu erkennen.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getEncoding()](#getEncoding) | Ermittelt die erkannte Kodierung, falls sie für das aktuelle Dokumentformat zutrifft. |
| [getLoadFormat()](#getLoadFormat) | Ermittelt das erkannte Dokumentformat. |
| [hasDigitalSignature()](#hasDigitalSignature) | Gibt  true  zurück, wenn dieses Dokument eine digitale Signatur enthält. |
| [hasMacros()](#hasMacros) | Gibt  true  zurück, wenn dieses Dokument VBA‑Makros enthält. |
| [isEncrypted()](#isEncrypted) | Gibt  true  zurück, wenn das Dokument verschlüsselt ist und ein Passwort zum Öffnen benötigt. |
### getEncoding() {#getEncoding}
```
public Charset getEncoding()
```


Ermittelt die erkannte Kodierung, falls sie für das aktuelle Dokumentformat zutrifft. Derzeit wird die Kodierung nur für HTML‑Dokumente erkannt.

 **Examples:** 

Zeigt, wie man die Kodierung in einer HTML‑Datei erkennt.

```

 FileFormatInfo info = FileFormatUtil.detectFileFormat(getMyDir() + "Document.html");

 Assert.assertEquals(LoadFormat.HTML, info.getLoadFormat());

 // The Encoding property is used only when we create a FileFormatInfo object for an html document.
 Assert.assertEquals("windows-1252", info.getEncoding().name());
 
```

**Returns:**
java.nio.charset.Charset – Die erkannte Kodierung, falls sie für das aktuelle Dokumentformat zutrifft.
### getLoadFormat() {#getLoadFormat}
```
public int getLoadFormat()
```


Ermittelt das erkannte Dokumentformat.

 **Remarks:** 

Wenn ein OOXML‑Dokument verschlüsselt ist, kann nicht festgestellt werden, ob es sich um ein Excel-, Word‑ oder PowerPoint‑Dokument handelt, ohne es zuerst zu entschlüsseln. Daher gibt diese Eigenschaft bei einem verschlüsselten OOXML‑Dokument stets [LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX) zurück.

 **Examples:** 

Zeigt, wie man die Klasse FileFormatUtil verwendet, um das Dokumentformat und die Verschlüsselung zu erkennen.

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

Zeigt, wie man die Klasse FileFormatUtil verwendet, um das Dokumentformat und das Vorhandensein digitaler Signaturen zu erkennen.

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

Zeigt, wie man die FileFormatUtil-Methoden verwendet, um das Format eines Dokuments zu erkennen.

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
int – Das erkannte Dokumentformat. Der zurückgegebene Wert ist einer der Konstanten von [LoadFormat](../../com.aspose.words/loadformat/).
### hasDigitalSignature() {#hasDigitalSignature}
```
public boolean hasDigitalSignature()
```


Gibt  true  zurück, wenn dieses Dokument eine digitale Signatur enthält. Diese Eigenschaft weist lediglich darauf hin, dass eine digitale Signatur im Dokument vorhanden ist, gibt jedoch nicht an, ob die Signatur gültig ist oder nicht.

 **Remarks:** 

Diese Eigenschaft dient dazu, digital signierte Dokumente von unsignierten zu unterscheiden. Wenn Sie Aspose.Words verwenden, um ein digital signiertes Dokument zu ändern und zu speichern, geht die digitale Signatur verloren. Das ist beabsichtigt, da eine digitale Signatur die Authentizität eines Dokuments schützt. Mit dieser Eigenschaft können Sie digital signierte Dokumente erkennen, bevor Sie sie wie normale Dokumente verarbeiten, und entsprechende Maßnahmen ergreifen, um den Verlust der digitalen Signatur zu vermeiden, z. B. den Benutzer benachrichtigen.

 **Examples:** 

Zeigt, wie man die Klasse FileFormatUtil verwendet, um das Dokumentformat und das Vorhandensein digitaler Signaturen zu erkennen.

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
boolean –  true  wenn dieses Dokument eine digitale Signatur enthält.
### hasMacros() {#hasMacros}
```
public boolean hasMacros()
```


Gibt  true  zurück, wenn dieses Dokument VBA‑Makros enthält.

 **Examples:** 

Zeigt, wie die Anwesenheit von VBA‑Makros geprüft werden kann, ohne das Dokument zu laden.

```

 FileFormatInfo fileFormatInfo = FileFormatUtil.detectFileFormat(getMyDir() + "Macro.docm");
 Assert.assertTrue(fileFormatInfo.hasMacros());
 
```

**Returns:**
boolean –  true  wenn dieses Dokument VBA‑Makros enthält.
### isEncrypted() {#isEncrypted}
```
public boolean isEncrypted()
```


Gibt  true  zurück, wenn das Dokument verschlüsselt ist und ein Passwort zum Öffnen benötigt.

 **Remarks:** 

Diese Eigenschaft dient dazu, verschlüsselte Dokumente von unverschlüsselten zu unterscheiden. Wenn Sie versuchen, ein verschlüsseltes Dokument mit Aspose.Words zu laden, ohne ein Passwort anzugeben, wird eine Ausnahme ausgelöst. Sie können diese Eigenschaft verwenden, um zu erkennen, ob ein Dokument ein Passwort benötigt, und vor dem Laden des Dokuments entsprechende Maßnahmen ergreifen, z. B. den Benutzer nach einem Passwort fragen.

 **Examples:** 

Zeigt, wie man die Klasse FileFormatUtil verwendet, um das Dokumentformat und die Verschlüsselung zu erkennen.

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
boolean –  true  wenn das Dokument verschlüsselt ist und ein Passwort zum Öffnen benötigt.
