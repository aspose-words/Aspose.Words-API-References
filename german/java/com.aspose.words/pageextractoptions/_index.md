---
title: "PageExtractOptions"
linktitle: "PageExtractOptions"
second_title: "Aspose.Words für Java"
description: "Ermöglicht das Festlegen von Optionen für das Extrahieren von Dokumentseiten in Java."
type: docs
weight: 512
url: /de/java/com.aspose.words/pageextractoptions/
---

**Inheritance:**
java.lang.Object
```
public class PageExtractOptions
```

Ermöglicht die Angabe von Optionen für das Extrahieren von Dokumentseiten.

 **Examples:** 

Zeigt, wie die anfängliche Seitennummerierung zurückgesetzt und das NUMPAGE-Feld gespeichert wird.

```

 Document doc = new Document(getMyDir() + "Page fields.docx");

 // Default behavior:
 // The extracted page numbering is the same as in the original document, as if we had selected "Print 2 pages" in MS Word.
 // The start page will be set to 2 and the field indicating the number of pages will be removed
 // and replaced with a constant value equal to the number of pages.
 Document extractedDoc1 = doc.extractPages(1, 1);
 extractedDoc1.save(getArtifactsDir() + "Document.ExtractPagesWithOptions.Default.docx");

 // Altered behavior:
 // The extracted page numbering is reset and a new one begins,
 // as if we had copied the contents of the second page and pasted it into a new document.
 // The start page will be set to 1 and the field indicating the number of pages will be left unchanged
 // and will show the current number of pages.
 PageExtractOptions extractOptions = new PageExtractOptions();
 extractOptions.setUpdatePageStartingNumber(false);
 extractOptions.setUnlinkPagesNumberFields(false);
 Document extractedDoc2 = doc.extractPages(1, 1, extractOptions);
 extractedDoc2.save(getArtifactsDir() + "Document.ExtractPagesWithOptions.Options.docx");
 
```
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [PageExtractOptions()](#PageExtractOptions) | Initialisiert eine neue Instanz dieser Klasse. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getUnlinkPagesNumberFields()](#getUnlinkPagesNumberFields) | Gibt an, ob NUMPAGES-Felder im resultierenden Dokument durch ihre tatsächlichen Werte ersetzt werden. |
| [getUpdatePageStartingNumber()](#getUpdatePageStartingNumber) | Gibt an, ob die Startseitennummer im resultierenden Dokument aktualisiert werden soll. |
| [setUnlinkPagesNumberFields(boolean value)](#setUnlinkPagesNumberFields-boolean) | Gibt an, ob NUMPAGES-Felder im resultierenden Dokument durch ihre tatsächlichen Werte ersetzt werden. |
| [setUpdatePageStartingNumber(boolean value)](#setUpdatePageStartingNumber-boolean) | Gibt an, ob die Startseitennummer im resultierenden Dokument aktualisiert werden soll. |
### PageExtractOptions() {#PageExtractOptions}
```
public PageExtractOptions()
```


Initialisiert eine neue Instanz dieser Klasse.

### getUnlinkPagesNumberFields() {#getUnlinkPagesNumberFields}
```
public boolean getUnlinkPagesNumberFields()
```


Gibt an, ob NUMPAGES-Felder im resultierenden Dokument durch ihre tatsächlichen Werte ersetzt werden. Standardwert ist true.

 **Examples:** 

Zeigt, wie die anfängliche Seitennummerierung zurückgesetzt und das NUMPAGE-Feld gespeichert wird.

```

 Document doc = new Document(getMyDir() + "Page fields.docx");

 // Default behavior:
 // The extracted page numbering is the same as in the original document, as if we had selected "Print 2 pages" in MS Word.
 // The start page will be set to 2 and the field indicating the number of pages will be removed
 // and replaced with a constant value equal to the number of pages.
 Document extractedDoc1 = doc.extractPages(1, 1);
 extractedDoc1.save(getArtifactsDir() + "Document.ExtractPagesWithOptions.Default.docx");

 // Altered behavior:
 // The extracted page numbering is reset and a new one begins,
 // as if we had copied the contents of the second page and pasted it into a new document.
 // The start page will be set to 1 and the field indicating the number of pages will be left unchanged
 // and will show the current number of pages.
 PageExtractOptions extractOptions = new PageExtractOptions();
 extractOptions.setUpdatePageStartingNumber(false);
 extractOptions.setUnlinkPagesNumberFields(false);
 Document extractedDoc2 = doc.extractPages(1, 1, extractOptions);
 extractedDoc2.save(getArtifactsDir() + "Document.ExtractPagesWithOptions.Options.docx");
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getUpdatePageStartingNumber() {#getUpdatePageStartingNumber}
```
public boolean getUpdatePageStartingNumber()
```


Gibt an, ob die Startseitennummer im resultierenden Dokument aktualisiert werden soll. Standardwert ist true.

 **Examples:** 

Zeigt, wie die anfängliche Seitennummerierung zurückgesetzt und das NUMPAGE-Feld gespeichert wird.

```

 Document doc = new Document(getMyDir() + "Page fields.docx");

 // Default behavior:
 // The extracted page numbering is the same as in the original document, as if we had selected "Print 2 pages" in MS Word.
 // The start page will be set to 2 and the field indicating the number of pages will be removed
 // and replaced with a constant value equal to the number of pages.
 Document extractedDoc1 = doc.extractPages(1, 1);
 extractedDoc1.save(getArtifactsDir() + "Document.ExtractPagesWithOptions.Default.docx");

 // Altered behavior:
 // The extracted page numbering is reset and a new one begins,
 // as if we had copied the contents of the second page and pasted it into a new document.
 // The start page will be set to 1 and the field indicating the number of pages will be left unchanged
 // and will show the current number of pages.
 PageExtractOptions extractOptions = new PageExtractOptions();
 extractOptions.setUpdatePageStartingNumber(false);
 extractOptions.setUnlinkPagesNumberFields(false);
 Document extractedDoc2 = doc.extractPages(1, 1, extractOptions);
 extractedDoc2.save(getArtifactsDir() + "Document.ExtractPagesWithOptions.Options.docx");
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### setUnlinkPagesNumberFields(boolean value) {#setUnlinkPagesNumberFields-boolean}
```
public void setUnlinkPagesNumberFields(boolean value)
```


Gibt an, ob NUMPAGES-Felder im resultierenden Dokument durch ihre tatsächlichen Werte ersetzt werden. Standardwert ist true.

 **Examples:** 

Zeigt, wie die anfängliche Seitennummerierung zurückgesetzt und das NUMPAGE-Feld gespeichert wird.

```

 Document doc = new Document(getMyDir() + "Page fields.docx");

 // Default behavior:
 // The extracted page numbering is the same as in the original document, as if we had selected "Print 2 pages" in MS Word.
 // The start page will be set to 2 and the field indicating the number of pages will be removed
 // and replaced with a constant value equal to the number of pages.
 Document extractedDoc1 = doc.extractPages(1, 1);
 extractedDoc1.save(getArtifactsDir() + "Document.ExtractPagesWithOptions.Default.docx");

 // Altered behavior:
 // The extracted page numbering is reset and a new one begins,
 // as if we had copied the contents of the second page and pasted it into a new document.
 // The start page will be set to 1 and the field indicating the number of pages will be left unchanged
 // and will show the current number of pages.
 PageExtractOptions extractOptions = new PageExtractOptions();
 extractOptions.setUpdatePageStartingNumber(false);
 extractOptions.setUnlinkPagesNumberFields(false);
 Document extractedDoc2 = doc.extractPages(1, 1, extractOptions);
 extractedDoc2.save(getArtifactsDir() + "Document.ExtractPagesWithOptions.Options.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setUpdatePageStartingNumber(boolean value) {#setUpdatePageStartingNumber-boolean}
```
public void setUpdatePageStartingNumber(boolean value)
```


Gibt an, ob die Startseitennummer im resultierenden Dokument aktualisiert werden soll. Standardwert ist true.

 **Examples:** 

Zeigt, wie die anfängliche Seitennummerierung zurückgesetzt und das NUMPAGE-Feld gespeichert wird.

```

 Document doc = new Document(getMyDir() + "Page fields.docx");

 // Default behavior:
 // The extracted page numbering is the same as in the original document, as if we had selected "Print 2 pages" in MS Word.
 // The start page will be set to 2 and the field indicating the number of pages will be removed
 // and replaced with a constant value equal to the number of pages.
 Document extractedDoc1 = doc.extractPages(1, 1);
 extractedDoc1.save(getArtifactsDir() + "Document.ExtractPagesWithOptions.Default.docx");

 // Altered behavior:
 // The extracted page numbering is reset and a new one begins,
 // as if we had copied the contents of the second page and pasted it into a new document.
 // The start page will be set to 1 and the field indicating the number of pages will be left unchanged
 // and will show the current number of pages.
 PageExtractOptions extractOptions = new PageExtractOptions();
 extractOptions.setUpdatePageStartingNumber(false);
 extractOptions.setUnlinkPagesNumberFields(false);
 Document extractedDoc2 = doc.extractPages(1, 1, extractOptions);
 extractedDoc2.save(getArtifactsDir() + "Document.ExtractPagesWithOptions.Options.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

