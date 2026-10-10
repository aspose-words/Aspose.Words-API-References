---
title: "FontInfoCollection"
linktitle: "FontInfoCollection"
second_title: "Aspose.Words per Java"
description: "Rappresenta una raccolta di caratteri utilizzati in un documento in Java."
type: docs
weight: 327
url: /it/java/com.aspose.words/fontinfocollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class FontInfoCollection implements Iterable
```

Rappresenta una raccolta di font utilizzati in un documento.

Per saperne di più, visita l'articolo di documentazione [ Working with Fonts ][Working with Fonts].

 **Remarks:** 

Gli elementi sono oggetti [FontInfo](../../com.aspose.words/fontinfo/).

Non si creano istanze di questa classe direttamente. Utilizzare la proprietà [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/\#getFontInfos) per accedere alla raccolta di caratteri definita nel documento.

 **Examples:** 

Mostra come stampare i dettagli dei font presenti in un documento.

```

 Document doc = new Document(getMyDir() + "Embedded font.docx");

 FontInfoCollection allFonts = doc.getFontInfos();
 // Print all the used and unused fonts in the document.
 for (int i = 0; i < allFonts.getCount(); i++) {
     System.out.println("Font index #{i}");
     System.out.println("\tName: {allFonts[i].Name}");
 }
 
```

Mostra come salvare un documento con caratteri TrueType incorporati.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [contains(String name)](#contains-java.lang.String) | Determina se la raccolta contiene un carattere con il nome specificato. |
| [get(int index)](#get-int) | Ottiene un carattere all'indice specificato. |
| [get(String name)](#get-java.lang.String) | Fornisce l'accesso agli elementi della raccolta. |
| [getCount()](#getCount) | Ottiene il numero di elementi contenuti nella collezione. |
| [getEmbedSystemFonts()](#getEmbedSystemFonts) | Specifica se incorporare o meno i caratteri di Sistema nel documento. |
| [getEmbedTrueTypeFonts()](#getEmbedTrueTypeFonts) | Specifica se incorporare o meno i caratteri TrueType in un documento al momento del salvataggio. |
| [getSaveSubsetFonts()](#getSaveSubsetFonts) | Specifica se salvare o meno un sottoinsieme dei caratteri TrueType incorporati con il documento. |
| [iterator()](#iterator) | Restituisce un oggetto iteratore che può essere usato per iterare su tutti gli elementi nella collezione. |
| [setEmbedSystemFonts(boolean value)](#setEmbedSystemFonts-boolean) | Specifica se incorporare o meno i caratteri di Sistema nel documento. |
| [setEmbedTrueTypeFonts(boolean value)](#setEmbedTrueTypeFonts-boolean) | Specifica se incorporare o meno i caratteri TrueType in un documento al momento del salvataggio. |
| [setSaveSubsetFonts(boolean value)](#setSaveSubsetFonts-boolean) | Specifica se salvare o meno un sottoinsieme dei caratteri TrueType incorporati con il documento. |
### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


Determina se la raccolta contiene un carattere con il nome specificato.

 **Examples:** 

Mostra informazioni sui caratteri presenti nel documento vuoto.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String | Nome del carattere da individuare, senza distinzione tra maiuscole e minuscole. |

**Returns:**
boolean -  true  se l'elemento è trovato nella raccolta; altrimenti,  false .
### get(int index) {#get-int}
```
public FontInfo get(int index)
```


Ottiene un carattere all'indice specificato.

 **Examples:** 

Mostra come estrarre un carattere incorporato da un documento e salvarlo nel file system locale.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | Indice basato su zero del carattere. |

**Returns:**
[FontInfo](../../com.aspose.words/fontinfo/) - A font at the specified index.
### get(String name) {#get-java.lang.String}
```
public FontInfo get(String name)
```


Fornisce l'accesso agli elementi della raccolta.  Ottiene un carattere con il nome specificato.

 **Examples:** 

Mostra come estrarre un carattere incorporato da un documento e salvarlo nel file system locale.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String | Nome del carattere da individuare, senza distinzione tra maiuscole e minuscole. |

**Returns:**
[FontInfo](../../com.aspose.words/fontinfo/) - The corresponding [FontInfo](../../com.aspose.words/fontinfo/) value.
### getCount() {#getCount}
```
public int getCount()
```


Ottiene il numero di elementi contenuti nella collezione.

 **Examples:** 

Mostra informazioni sui caratteri presenti nel documento vuoto.

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
int - Il numero di elementi contenuti nella collezione.
### getEmbedSystemFonts() {#getEmbedSystemFonts}
```
public boolean getEmbedSystemFonts()
```


Specifica se incorporare o meno i caratteri di Sistema nel documento. Il valore predefinito per questa proprietà è  false .

Questa opzione funziona solo quando l'opzione [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) è impostata su  true .

 **Remarks:** 

Impostare questa proprietà su  true  è utile se l'utente utilizza un sistema dell'Asia orientale e desidera creare un documento leggibile da altri che non hanno i caratteri per quella lingua sul proprio sistema. Ad esempio, un utente su un sistema giapponese potrebbe scegliere di incorporare i caratteri in un documento affinché il documento giapponese sia leggibile su tutti i sistemi.

Questa opzione funziona solo per i formati DOC, DOCX e RTF.

 **Examples:** 

Mostra come salvare un documento con caratteri TrueType incorporati.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getEmbedTrueTypeFonts() {#getEmbedTrueTypeFonts}
```
public boolean getEmbedTrueTypeFonts()
```


Specifica se incorporare o meno i caratteri TrueType in un documento al momento del salvataggio. Il valore predefinito per questa proprietà è  false .

 **Remarks:** 

L'incorporamento dei caratteri TrueType consente ad altri di visualizzare il documento con gli stessi caratteri usati per crearlo, ma può aumentare notevolmente le dimensioni del documento.

Questa opzione funziona solo per i formati DOC, DOCX e RTF.

 **Examples:** 

Mostra come salvare un documento con caratteri TrueType incorporati.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getSaveSubsetFonts() {#getSaveSubsetFonts}
```
public boolean getSaveSubsetFonts()
```


Specifica se salvare o meno un sottoinsieme dei caratteri TrueType incorporati con il documento. Il valore predefinito per questa proprietà è  false .

Questa opzione funziona solo quando la proprietà [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) è impostata su  true .

 **Remarks:** 

Questa opzione funziona solo per i formati DOC, DOCX e RTF.

 **Examples:** 

Mostra come salvare un documento con caratteri TrueType incorporati.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### iterator() {#iterator}
```
public Iterator iterator()
```


Restituisce un oggetto iteratore che può essere usato per iterare su tutti gli elementi nella collezione.

 **Examples:** 

Mostra come accedere e stampare i dettagli di ogni carattere in un documento.

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


Specifica se incorporare o meno i caratteri di Sistema nel documento. Il valore predefinito per questa proprietà è  false .

Questa opzione funziona solo quando l'opzione [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) è impostata su  true .

 **Remarks:** 

Impostare questa proprietà su  true  è utile se l'utente utilizza un sistema dell'Asia orientale e desidera creare un documento leggibile da altri che non hanno i caratteri per quella lingua sul proprio sistema. Ad esempio, un utente su un sistema giapponese potrebbe scegliere di incorporare i caratteri in un documento affinché il documento giapponese sia leggibile su tutti i sistemi.

Questa opzione funziona solo per i formati DOC, DOCX e RTF.

 **Examples:** 

Mostra come salvare un documento con caratteri TrueType incorporati.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setEmbedTrueTypeFonts(boolean value) {#setEmbedTrueTypeFonts-boolean}
```
public void setEmbedTrueTypeFonts(boolean value)
```


Specifica se incorporare o meno i caratteri TrueType in un documento al momento del salvataggio. Il valore predefinito per questa proprietà è  false .

 **Remarks:** 

L'incorporamento dei caratteri TrueType consente ad altri di visualizzare il documento con gli stessi caratteri usati per crearlo, ma può aumentare notevolmente le dimensioni del documento.

Questa opzione funziona solo per i formati DOC, DOCX e RTF.

 **Examples:** 

Mostra come salvare un documento con caratteri TrueType incorporati.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setSaveSubsetFonts(boolean value) {#setSaveSubsetFonts-boolean}
```
public void setSaveSubsetFonts(boolean value)
```


Specifica se salvare o meno un sottoinsieme dei caratteri TrueType incorporati con il documento. Il valore predefinito per questa proprietà è  false .

Questa opzione funziona solo quando la proprietà [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) è impostata su  true .

 **Remarks:** 

Questa opzione funziona solo per i formati DOC, DOCX e RTF.

 **Examples:** 

Mostra come salvare un documento con caratteri TrueType incorporati.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

