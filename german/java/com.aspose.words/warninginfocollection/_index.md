---
title: "WarningInfoCollection"
linktitle: "WarningInfoCollection"
second_title: "Aspose.Words für Java"
description: "Stellt eine typisierte Sammlung von WarningInfo-Objekten in Java dar."
type: docs
weight: 718
url: /de/java/com.aspose.words/warninginfocollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
[com.aspose.words.IWarningCallback](../../com.aspose.words/iwarningcallback/), java.lang.Iterable
```
public class WarningInfoCollection implements IWarningCallback, Iterable
```

Stellt eine typisierte Sammlung von [WarningInfo](../../com.aspose.words/warninginfo/) Objekten dar.

Weitere Informationen finden Sie im Dokumentationsartikel [ Programming with Documents ][Programming with Documents].

 **Remarks:** 

Sie können dieses Sammlungsobjekt als einfachste Form einer [IWarningCallback](../../com.aspose.words/iwarningcallback/) Implementierung verwenden, um alle Warnungen zu sammeln, die Aspose.Words während eines Ladevorgangs oder Speichervorgangs erzeugt. Erzeugen Sie eine Instanz dieser Klasse und weisen Sie sie der [LoadOptions.getWarningCallback()](../../com.aspose.words/loadoptions/\#getWarningCallback) / [LoadOptions.setWarningCallback(com.aspose.words.IWarningCallback)](../../com.aspose.words/loadoptions/\#setWarningCallback-com.aspose.words.IWarningCallback) oder [DocumentBase.getWarningCallback()](../../com.aspose.words/documentbase/\#getWarningCallback) / [DocumentBase.setWarningCallback(com.aspose.words.IWarningCallback)](../../com.aspose.words/documentbase/\#setWarningCallback-com.aspose.words.IWarningCallback) Eigenschaft zu.

 **Examples:** 

Zeigt, wie die Eigenschaft zum Finden der besten Übereinstimmung für eine fehlende Schriftart aus den verfügbaren Schriftquellen festgelegt wird.

```

 // Open a document that contains text formatted with a font that does not exist in any of our font sources.
 Document doc = new Document(getMyDir() + "Missing font.docx");

 // Assign a callback for handling font substitution warnings.
 WarningInfoCollection warningCollector = new WarningInfoCollection();
 doc.setWarningCallback(warningCollector);

 // Set a default font name and enable font substitution.
 FontSettings fontSettings = new FontSettings();
 fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Arial");
 fontSettings.getSubstitutionSettings().getFontInfoSubstitution().setEnabled(true);

 // Original font metrics should be used after font substitution.
 doc.getLayoutOptions().setKeepOriginalFontMetrics(true);

 // We will get a font substitution warning if we save a document with a missing font.
 doc.setFontSettings(fontSettings);
 doc.save(getArtifactsDir() + "FontSettings.EnableFontSubstitution.pdf");

 for (WarningInfo info : warningCollector)
 {
     if (info.getWarningType() == WarningType.FONT_SUBSTITUTION)
         System.out.println(info.getDescription());
 }
 
```


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [clear()](#clear) | Entfernt alle Elemente aus der Sammlung. |
| [get(int index)](#get-int) | Ruft ein Element am angegebenen Index ab. |
| [getCount()](#getCount) | Ermittelt die Anzahl der im Sammelobjekt enthaltenen Elemente. |
| [iterator()](#iterator) | Gibt ein Iterator-Objekt zurück, das verwendet werden kann, um über alle Elemente in der Sammlung zu iterieren. |
| [warning(WarningInfo info)](#warning-com.aspose.words.WarningInfo) | Implementiert das [IWarningCallback](../../com.aspose.words/iwarningcallback/) Interface. |
### clear() {#clear}
```
public void clear()
```


Entfernt alle Elemente aus der Sammlung.

 **Examples:** 

Zeigt, wie die Eigenschaft zum Finden der besten Übereinstimmung für eine fehlende Schriftart aus den verfügbaren Schriftquellen festgelegt wird.

```

 // Open a document that contains text formatted with a font that does not exist in any of our font sources.
 Document doc = new Document(getMyDir() + "Missing font.docx");

 // Assign a callback for handling font substitution warnings.
 WarningInfoCollection warningCollector = new WarningInfoCollection();
 doc.setWarningCallback(warningCollector);

 // Set a default font name and enable font substitution.
 FontSettings fontSettings = new FontSettings();
 fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Arial");
 fontSettings.getSubstitutionSettings().getFontInfoSubstitution().setEnabled(true);

 // Original font metrics should be used after font substitution.
 doc.getLayoutOptions().setKeepOriginalFontMetrics(true);

 // We will get a font substitution warning if we save a document with a missing font.
 doc.setFontSettings(fontSettings);
 doc.save(getArtifactsDir() + "FontSettings.EnableFontSubstitution.pdf");

 for (WarningInfo info : warningCollector)
 {
     if (info.getWarningType() == WarningType.FONT_SUBSTITUTION)
         System.out.println(info.getDescription());
 }
 
```

### get(int index) {#get-int}
```
public WarningInfo get(int index)
```


Ruft ein Element am angegebenen Index ab.

 **Examples:** 

Zeigt, wie man Warnungen zu nicht unterstützten Formaten erhält.

```

 WarningInfoCollection warings = new WarningInfoCollection();
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setWarningCallback(warings);
 Document doc = new Document(getMyDir() + "FB2 document.fb2", loadOptions);

 Assert.assertEquals("The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warings.get(0).getDescription());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Nullbasierter Index des Elements. |

**Returns:**
[WarningInfo](../../com.aspose.words/warninginfo/) - An item at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Ermittelt die Anzahl der im Sammelobjekt enthaltenen Elemente.

 **Examples:** 

Zeigt, wie man Warnungen zu nicht unterstützten Formaten erhält.

```

 WarningInfoCollection warings = new WarningInfoCollection();
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setWarningCallback(warings);
 Document doc = new Document(getMyDir() + "FB2 document.fb2", loadOptions);

 Assert.assertEquals("The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warings.get(0).getDescription());
 
```

**Returns:**
int – Die Anzahl der im Sammelobjekt enthaltenen Elemente.
### iterator() {#iterator}
```
public Iterator iterator()
```


Gibt ein Iterator-Objekt zurück, das verwendet werden kann, um über alle Elemente in der Sammlung zu iterieren.

**Returns:**
java.util.Iterator
### warning(WarningInfo info) {#warning-com.aspose.words.WarningInfo}
```
public void warning(WarningInfo info)
```


Implementiert das [IWarningCallback](../../com.aspose.words/iwarningcallback/) Interface. Fügt dieser Sammlung eine Warnung hinzu.

 **Examples:** 

Zeigt, wie die Eigenschaft zum Finden der besten Übereinstimmung für eine fehlende Schriftart aus den verfügbaren Schriftquellen festgelegt wird.

```

 // Open a document that contains text formatted with a font that does not exist in any of our font sources.
 Document doc = new Document(getMyDir() + "Missing font.docx");

 // Assign a callback for handling font substitution warnings.
 WarningInfoCollection warningCollector = new WarningInfoCollection();
 doc.setWarningCallback(warningCollector);

 // Set a default font name and enable font substitution.
 FontSettings fontSettings = new FontSettings();
 fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Arial");
 fontSettings.getSubstitutionSettings().getFontInfoSubstitution().setEnabled(true);

 // Original font metrics should be used after font substitution.
 doc.getLayoutOptions().setKeepOriginalFontMetrics(true);

 // We will get a font substitution warning if we save a document with a missing font.
 doc.setFontSettings(fontSettings);
 doc.save(getArtifactsDir() + "FontSettings.EnableFontSubstitution.pdf");

 for (WarningInfo info : warningCollector)
 {
     if (info.getWarningType() == WarningType.FONT_SUBSTITUTION)
         System.out.println(info.getDescription());
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| info | [WarningInfo](../../com.aspose.words/warninginfo/) |  |

