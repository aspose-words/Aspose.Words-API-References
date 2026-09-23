---
title: "FontInfoCollection"
linktitle: "FontInfoCollection"
second_title: "Aspose.Words für Java"
description: "Stellt eine Sammlung von Schriften dar, die in einem Java‑Dokument verwendet werden."
type: docs
weight: 327
url: /de/java/com.aspose.words/fontinfocollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class FontInfoCollection implements Iterable
```

Stellt eine Sammlung von im Dokument verwendeten Schriften dar.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Working with Fonts ][Working with Fonts].

 **Remarks:** 

Elemente sind [FontInfo](../../com.aspose.words/fontinfo/)‑Objekte.

Sie erstellen keine Instanzen dieser Klasse direkt. Verwenden Sie die Eigenschaft [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/\#getFontInfos), um auf die im Dokument definierte Schriften‑Sammlung zuzugreifen.

 **Examples:** 

Zeigt, wie man die Details der im Dokument vorhandenen Schriften ausgibt.

```

 Document doc = new Document(getMyDir() + "Embedded font.docx");

 FontInfoCollection allFonts = doc.getFontInfos();
 // Print all the used and unused fonts in the document.
 for (int i = 0; i < allFonts.getCount(); i++) {
     System.out.println("Font index #{i}");
     System.out.println("\tName: {allFonts[i].Name}");
 }
 
```

Zeigt, wie ein Dokument mit eingebetteten TrueType‑Schriften gespeichert wird.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [contains(String name)](#contains-java.lang.String) | Bestimmt, ob die Sammlung eine Schrift mit dem angegebenen Namen enthält. |
| [get(int index)](#get-int) | Liefert eine Schrift am angegebenen Index. |
| [get(String name)](#get-java.lang.String) | Stellt Zugriff auf die Elemente der Sammlung bereit. |
| [getCount()](#getCount) | Ermittelt die Anzahl der im Sammelobjekt enthaltenen Elemente. |
| [getEmbedSystemFonts()](#getEmbedSystemFonts) | Gibt an, ob Systemschriften in das Dokument eingebettet werden sollen oder nicht. |
| [getEmbedTrueTypeFonts()](#getEmbedTrueTypeFonts) | Gibt an, ob TrueType‑Schriften beim Speichern eines Dokuments eingebettet werden sollen oder nicht. |
| [getSaveSubsetFonts()](#getSaveSubsetFonts) | Gibt an, ob ein Teil der eingebetteten TrueType‑Schriften mit dem Dokument gespeichert werden soll oder nicht. |
| [iterator()](#iterator) | Gibt ein Iterator-Objekt zurück, das verwendet werden kann, um über alle Elemente in der Sammlung zu iterieren. |
| [setEmbedSystemFonts(boolean value)](#setEmbedSystemFonts-boolean) | Gibt an, ob Systemschriften in das Dokument eingebettet werden sollen oder nicht. |
| [setEmbedTrueTypeFonts(boolean value)](#setEmbedTrueTypeFonts-boolean) | Gibt an, ob TrueType‑Schriften beim Speichern eines Dokuments eingebettet werden sollen oder nicht. |
| [setSaveSubsetFonts(boolean value)](#setSaveSubsetFonts-boolean) | Gibt an, ob ein Teil der eingebetteten TrueType‑Schriften mit dem Dokument gespeichert werden soll oder nicht. |
### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


Bestimmt, ob die Sammlung eine Schrift mit dem angegebenen Namen enthält.

 **Examples:** 

Zeigt Informationen über die Schriften, die im leeren Dokument vorhanden sind.

```

 Document doc = new Document();

 // A blank document contains 3 default fonts. Each font in the document
 // will have a corresponding FontInfo object which contains details about that font.
 Assert.assertEquals(3, doc.getFontInfos().getCount());

 Assert.assertTrue(doc.getFontInfos().contains("Times New Roman"));
 Assert.assertEquals(204, doc.getFontInfos().get("Times New Roman").getCharset());

 Assert.assertTrue(doc.getFontInfos().contains("Symbol"));
 Assert.assertTrue(doc.getFontInfos().contains("Arial"));
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Groß-/Kleinschreibung‑unabhängiger Name der zu findenden Schrift. |

**Returns:**
boolean -  true  wenn das Element in der Sammlung gefunden wird; andernfalls,  false .
### get(int index) {#get-int}
```
public FontInfo get(int index)
```


Liefert eine Schrift am angegebenen Index.

 **Examples:** 

Zeigt, wie eine eingebettete Schrift aus einem Dokument extrahiert und im lokalen Dateisystem gespeichert wird.

```

 Document doc = new Document(getMyDir() + "Embedded font.docx");

 FontInfo embeddedFont = doc.getFontInfos().get("Alte DIN 1451 Mittelschrift");
 byte[] embeddedFontBytes = embeddedFont.getEmbeddedFont(EmbeddedFontFormat.OPEN_TYPE, EmbeddedFontStyle.REGULAR);
 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Alte DIN 1451 Mittelschrift.ttf"), embeddedFontBytes);

 // Embedded font formats may be different in other formats such as .doc.
 // We need to know the correct format before we can extract the font.
 doc = new Document(getMyDir() + "Embedded font.doc");

 Assert.assertNull(doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFont(EmbeddedFontFormat.OPEN_TYPE, EmbeddedFontStyle.REGULAR));
 Assert.assertNotNull(doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFont(EmbeddedFontFormat.EMBEDDED_OPEN_TYPE, EmbeddedFontStyle.REGULAR));

 // Also, we can convert embedded OpenType format, which comes from .doc documents, to OpenType.
 embeddedFontBytes = doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFontAsOpenType(EmbeddedFontStyle.REGULAR);

 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Alte DIN 1451 Mittelschrift.otf"), embeddedFontBytes);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Nullbasierter Index der Schrift. |

**Returns:**
[FontInfo](../../com.aspose.words/fontinfo/) - A font at the specified index.
### get(String name) {#get-java.lang.String}
```
public FontInfo get(String name)
```


Stellt Zugriff auf die Sammlungs‑Elemente bereit. Liefert eine Schrift mit dem angegebenen Namen.

 **Examples:** 

Zeigt, wie eine eingebettete Schrift aus einem Dokument extrahiert und im lokalen Dateisystem gespeichert wird.

```

 Document doc = new Document(getMyDir() + "Embedded font.docx");

 FontInfo embeddedFont = doc.getFontInfos().get("Alte DIN 1451 Mittelschrift");
 byte[] embeddedFontBytes = embeddedFont.getEmbeddedFont(EmbeddedFontFormat.OPEN_TYPE, EmbeddedFontStyle.REGULAR);
 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Alte DIN 1451 Mittelschrift.ttf"), embeddedFontBytes);

 // Embedded font formats may be different in other formats such as .doc.
 // We need to know the correct format before we can extract the font.
 doc = new Document(getMyDir() + "Embedded font.doc");

 Assert.assertNull(doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFont(EmbeddedFontFormat.OPEN_TYPE, EmbeddedFontStyle.REGULAR));
 Assert.assertNotNull(doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFont(EmbeddedFontFormat.EMBEDDED_OPEN_TYPE, EmbeddedFontStyle.REGULAR));

 // Also, we can convert embedded OpenType format, which comes from .doc documents, to OpenType.
 embeddedFontBytes = doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFontAsOpenType(EmbeddedFontStyle.REGULAR);

 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Alte DIN 1451 Mittelschrift.otf"), embeddedFontBytes);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Groß-/Kleinschreibung‑unabhängiger Name der zu findenden Schrift. |

**Returns:**
[FontInfo](../../com.aspose.words/fontinfo/) - The corresponding [FontInfo](../../com.aspose.words/fontinfo/) value.
### getCount() {#getCount}
```
public int getCount()
```


Ermittelt die Anzahl der im Sammelobjekt enthaltenen Elemente.

 **Examples:** 

Zeigt Informationen über die Schriften, die im leeren Dokument vorhanden sind.

```

 Document doc = new Document();

 // A blank document contains 3 default fonts. Each font in the document
 // will have a corresponding FontInfo object which contains details about that font.
 Assert.assertEquals(3, doc.getFontInfos().getCount());

 Assert.assertTrue(doc.getFontInfos().contains("Times New Roman"));
 Assert.assertEquals(204, doc.getFontInfos().get("Times New Roman").getCharset());

 Assert.assertTrue(doc.getFontInfos().contains("Symbol"));
 Assert.assertTrue(doc.getFontInfos().contains("Arial"));
 
```

**Returns:**
int – Die Anzahl der im Sammelobjekt enthaltenen Elemente.
### getEmbedSystemFonts() {#getEmbedSystemFonts}
```
public boolean getEmbedSystemFonts()
```


Gibt an, ob Systemschriften in das Dokument eingebettet werden sollen oder nicht. Der Standardwert für diese Eigenschaft ist false.

Diese Option funktioniert nur, wenn die Option [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) auf true gesetzt ist.

 **Remarks:** 

Das Setzen dieser Eigenschaft auf true ist nützlich, wenn der Benutzer ein ostasiatisches System verwendet und ein Dokument erstellen möchte, das von anderen gelesen werden kann, die keine Schriften für diese Sprache auf ihrem System haben. Zum Beispiel könnte ein Benutzer eines japanischen Systems wählen, die Schriften in ein Dokument einzubetten, sodass das japanische Dokument auf allen Systemen lesbar ist.

Diese Option funktioniert nur für die Formate DOC, DOCX und RTF.

 **Examples:** 

Zeigt, wie ein Dokument mit eingebetteten TrueType‑Schriften gespeichert wird.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getEmbedTrueTypeFonts() {#getEmbedTrueTypeFonts}
```
public boolean getEmbedTrueTypeFonts()
```


Gibt an, ob TrueType-Schriften beim Speichern eines Dokuments eingebettet werden sollen oder nicht. Der Standardwert für diese Eigenschaft ist false.

 **Remarks:** 

Das Einbetten von TrueType-Schriften ermöglicht es anderen, das Dokument mit denselben Schriften zu sehen, die bei der Erstellung verwendet wurden, kann jedoch die Dokumentgröße erheblich vergrößern.

Diese Option funktioniert nur für die Formate DOC, DOCX und RTF.

 **Examples:** 

Zeigt, wie ein Dokument mit eingebetteten TrueType‑Schriften gespeichert wird.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getSaveSubsetFonts() {#getSaveSubsetFonts}
```
public boolean getSaveSubsetFonts()
```


Gibt an, ob ein Teil der eingebetteten TrueType-Schriften mit dem Dokument gespeichert werden soll oder nicht. Der Standardwert für diese Eigenschaft ist false.

Diese Option funktioniert nur, wenn die Eigenschaft [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) auf true gesetzt ist.

 **Remarks:** 

Diese Option funktioniert nur für die Formate DOC, DOCX und RTF.

 **Examples:** 

Zeigt, wie ein Dokument mit eingebetteten TrueType‑Schriften gespeichert wird.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### iterator() {#iterator}
```
public Iterator iterator()
```


Gibt ein Iterator-Objekt zurück, das verwendet werden kann, um über alle Elemente in der Sammlung zu iterieren.

 **Examples:** 

Zeigt, wie man auf jede Schrift in einem Dokument zugreift und deren Details ausgibt.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 Iterator fontCollectionEnumerator = doc.getFontInfos().iterator();
 while (fontCollectionEnumerator.hasNext()) {
     FontInfo fontInfo = fontCollectionEnumerator.next();
     if (fontInfo != null) {
         System.out.println("Font name: " + fontInfo.getName());

         // Alt names are usually blank.
         System.out.println("Alt name: " + fontInfo.getAltName());
         System.out.println("\t- Family: " + fontInfo.getFamily());
         System.out.println("\t- " + (fontInfo.isTrueType() ? "Is TrueType" : "Is not TrueType"));
         System.out.println("\t- Pitch: " + fontInfo.getPitch());
         System.out.println("\t- Charset: " + fontInfo.getCharset());
         System.out.println("\t- Panose:");
         System.out.println("\t\tFamily Kind: " + (fontInfo.getPanose()[0] & 0xFF));
         System.out.println("\t\tSerif Style: " + (fontInfo.getPanose()[1] & 0xFF));
         System.out.println("\t\tWeight: " + (fontInfo.getPanose()[2] & 0xFF));
         System.out.println("\t\tProportion: " + (fontInfo.getPanose()[3] & 0xFF));
         System.out.println("\t\tContrast: " + (fontInfo.getPanose()[4] & 0xFF));
         System.out.println("\t\tStroke Variation: " + (fontInfo.getPanose()[5] & 0xFF));
         System.out.println("\t\tArm Style: " + (fontInfo.getPanose()[6] & 0xFF));
         System.out.println("\t\tLetterform: " + (fontInfo.getPanose()[7] & 0xFF));
         System.out.println("\t\tMidline: " + (fontInfo.getPanose()[8] & 0xFF));
         System.out.println("\t\tX-Height: " + (fontInfo.getPanose()[9] & 0xFF));
     }
 }
 
```

**Returns:**
java.util.Iterator
### setEmbedSystemFonts(boolean value) {#setEmbedSystemFonts-boolean}
```
public void setEmbedSystemFonts(boolean value)
```


Gibt an, ob Systemschriften in das Dokument eingebettet werden sollen oder nicht. Der Standardwert für diese Eigenschaft ist false.

Diese Option funktioniert nur, wenn die Option [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) auf true gesetzt ist.

 **Remarks:** 

Das Setzen dieser Eigenschaft auf true ist nützlich, wenn der Benutzer ein ostasiatisches System verwendet und ein Dokument erstellen möchte, das von anderen gelesen werden kann, die keine Schriften für diese Sprache auf ihrem System haben. Zum Beispiel könnte ein Benutzer eines japanischen Systems wählen, die Schriften in ein Dokument einzubetten, sodass das japanische Dokument auf allen Systemen lesbar ist.

Diese Option funktioniert nur für die Formate DOC, DOCX und RTF.

 **Examples:** 

Zeigt, wie ein Dokument mit eingebetteten TrueType‑Schriften gespeichert wird.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setEmbedTrueTypeFonts(boolean value) {#setEmbedTrueTypeFonts-boolean}
```
public void setEmbedTrueTypeFonts(boolean value)
```


Gibt an, ob TrueType-Schriften beim Speichern eines Dokuments eingebettet werden sollen oder nicht. Der Standardwert für diese Eigenschaft ist false.

 **Remarks:** 

Das Einbetten von TrueType-Schriften ermöglicht es anderen, das Dokument mit denselben Schriften zu sehen, die bei der Erstellung verwendet wurden, kann jedoch die Dokumentgröße erheblich vergrößern.

Diese Option funktioniert nur für die Formate DOC, DOCX und RTF.

 **Examples:** 

Zeigt, wie ein Dokument mit eingebetteten TrueType‑Schriften gespeichert wird.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setSaveSubsetFonts(boolean value) {#setSaveSubsetFonts-boolean}
```
public void setSaveSubsetFonts(boolean value)
```


Gibt an, ob ein Teil der eingebetteten TrueType-Schriften mit dem Dokument gespeichert werden soll oder nicht. Der Standardwert für diese Eigenschaft ist false.

Diese Option funktioniert nur, wenn die Eigenschaft [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) auf true gesetzt ist.

 **Remarks:** 

Diese Option funktioniert nur für die Formate DOC, DOCX und RTF.

 **Examples:** 

Zeigt, wie ein Dokument mit eingebetteten TrueType‑Schriften gespeichert wird.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

