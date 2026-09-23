---
title: "FileFormatUtil"
linktitle: "FileFormatUtil"
second_title: "Aspose.Words für Java"
description: "Stellt Hilfsmethoden für die Arbeit mit Dateiformaten bereit, z. B. zum Erkennen von Dateiformaten oder zum Konvertieren von Dateierweiterungen in/von Dateiformat‑Enums in Java."
type: docs
weight: 310
url: /de/java/com.aspose.words/fileformatutil/
---

**Inheritance:**
java.lang.Object
```
public class FileFormatUtil
```

Stellt Dienstprogrammmethoden für die Arbeit mit Dateiformaten bereit, z. B. zum Erkennen von Dateiformaten oder zum Konvertieren von Dateierweiterungen in/von Dateiformat-Enums.

Um mehr zu erfahren, besuchen Sie den [ Detect File Format and Check Format Compatibility ][Detect File Format and Check Format Compatibility] Dokumentationsartikel.

 **Examples:** 

Zeigt, wie man die Kodierung in einer HTML‑Datei erkennt.

```

 FileFormatInfo info = FileFormatUtil.detectFileFormat(getMyDir() + "Document.html");

 Assert.assertEquals(LoadFormat.HTML, info.getLoadFormat());

 // The Encoding property is used only when we create a FileFormatInfo object for an html document.
 Assert.assertEquals("windows-1252", info.getEncoding().name());
 
```


[Detect File Format and Check Format Compatibility]: https://docs.aspose.com/words/java/detect-file-format-and-check-format-compatibility/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [contentTypeToLoadFormat(String contentType)](#contentTypeToLoadFormat-java.lang.String) | Konvertiert den IANA‑Inhaltstyp in einen Aufladeformat‑Aufzählungswert. |
| [contentTypeToSaveFormat(String contentType)](#contentTypeToSaveFormat-java.lang.String) | Konvertiert den IANA‑Inhaltstyp in einen Speicherformat‑Aufzählungswert. |
| [detectFileFormat(InputStream stream)](#detectFileFormat-java.io.InputStream) |  |
| [detectFileFormat(String fileName)](#detectFileFormat-java.lang.String) | Ermittelt und gibt die Informationen über das Format eines Dokuments zurück. |
| [extensionToSaveFormat(String extension)](#extensionToSaveFormat-java.lang.String) | Konvertiert eine Dateinamenerweiterung in einen [SaveFormat](../../com.aspose.words/saveformat/)‑Wert. |
| [imageTypeToExtension(int imageType)](#imageTypeToExtension-int) |  |
| [loadFormatToExtension(int loadFormat)](#loadFormatToExtension-int) |  |
| [loadFormatToSaveFormat(int loadFormat)](#loadFormatToSaveFormat-int) |  |
| [saveFormatToExtension(int saveFormat)](#saveFormatToExtension-int) |  |
| [saveFormatToLoadFormat(int saveFormat)](#saveFormatToLoadFormat-int) |  |
### contentTypeToLoadFormat(String contentType) {#contentTypeToLoadFormat-java.lang.String}
```
public static int contentTypeToLoadFormat(String contentType)
```


Konvertiert den IANA‑Inhaltstyp in einen Aufladeformat‑Aufzählungswert.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| contentType | java.lang.String |  |

**Returns:**
int
### contentTypeToSaveFormat(String contentType) {#contentTypeToSaveFormat-java.lang.String}
```
public static int contentTypeToSaveFormat(String contentType)
```


Konvertiert den IANA‑Inhaltstyp in einen Speicherformat‑Aufzählungswert.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| contentType | java.lang.String |  |

**Returns:**
int
### detectFileFormat(InputStream stream) {#detectFileFormat-java.io.InputStream}
```
public static FileFormatInfo detectFileFormat(InputStream stream)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | java.io.InputStream |  |

**Returns:**
[FileFormatInfo](../../com.aspose.words/fileformatinfo/)
### detectFileFormat(String fileName) {#detectFileFormat-java.lang.String}
```
public static FileFormatInfo detectFileFormat(String fileName)
```


Ermittelt und gibt die Informationen über das Format eines Dokuments zurück. Ermittelt und gibt die Informationen über das Format eines in einer Festplattendatei gespeicherten Dokuments zurück.

 **Remarks:** 

Selbst wenn diese Methode das Dokumentformat erkennt, garantiert sie nicht, dass das angegebene Dokument gültig ist. Diese Methode erkennt das Dokumentformat nur, indem sie Daten liest, die für die Erkennung ausreichen. Um vollständig zu überprüfen, ob ein Dokument gültig ist, müssen Sie das Dokument in ein [Document](../../com.aspose.words/document/)‑Objekt laden.

Diese Methode wirft [FileCorruptedException](../../com.aspose.words/filecorruptedexception/), wenn das Format erkannt wird, die Erkennung jedoch aufgrund von Beschädigungen nicht abgeschlossen werden kann.

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

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | java.lang.String | Der Dateiname. |

**Returns:**
[FileFormatInfo](../../com.aspose.words/fileformatinfo/) - A [FileFormatInfo](../../com.aspose.words/fileformatinfo/) object that contains the detected information.
### extensionToSaveFormat(String extension) {#extensionToSaveFormat-java.lang.String}
```
public static int extensionToSaveFormat(String extension)
```


Konvertiert eine Dateinamenerweiterung in einen [SaveFormat](../../com.aspose.words/saveformat/)‑Wert.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| extension | java.lang.String | Die Dateierweiterung. Kann mit oder ohne führenden Punkt angegeben werden. Groß-/Kleinschreibung wird ignoriert. |

**Returns:**
int
### imageTypeToExtension(int imageType) {#imageTypeToExtension-int}
```
public static String imageTypeToExtension(int imageType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| imageType | int |  |

**Returns:**
java.lang.String
### loadFormatToExtension(int loadFormat) {#loadFormatToExtension-int}
```
public static String loadFormatToExtension(int loadFormat)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| loadFormat | int |  |

**Returns:**
java.lang.String
### loadFormatToSaveFormat(int loadFormat) {#loadFormatToSaveFormat-int}
```
public static int loadFormatToSaveFormat(int loadFormat)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| loadFormat | int |  |

**Returns:**
int
### saveFormatToExtension(int saveFormat) {#saveFormatToExtension-int}
```
public static String saveFormatToExtension(int saveFormat)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
### saveFormatToLoadFormat(int saveFormat) {#saveFormatToLoadFormat-int}
```
public static int saveFormatToLoadFormat(int saveFormat)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
int
