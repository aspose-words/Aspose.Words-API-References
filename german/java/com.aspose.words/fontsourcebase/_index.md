---
title: "FontSourceBase"
linktitle: "FontSourceBase"
second_title: "Aspose.Words für Java"
description: "Dies ist eine abstrakte Basisklasse für die Klassen, die es dem Benutzer ermöglichen, verschiedene Schriftquellen in Java anzugeben."
type: docs
weight: 333
url: /de/java/com.aspose.words/fontsourcebase/
---

**Inheritance:**
java.lang.Object
```
public abstract class FontSourceBase
```

Dies ist eine abstrakte Basisklasse für die Klassen, die dem Benutzer ermöglichen, verschiedene Schriftquellen anzugeben.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Working with Fonts ][Working with Fonts].

 **Examples:** 

Zeigt, wie eine Schriftdatei im lokalen Dateisystem als Schriftquelle verwendet wird.

```

 FileFontSource fileFontSource = new FileFontSource(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf", 0);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{fileFontSource});

 Assert.assertEquals(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.getFilePath());
 Assert.assertEquals(FontSourceType.FONT_FILE, fileFontSource.getType());
 Assert.assertEquals(0, fileFontSource.getPriority());
 
```


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getAvailableFonts()](#getAvailableFonts) | Gibt die Liste der über diese Quelle verfügbaren Schriftarten zurück. |
| [getFontDataInternal()](#getFontDataInternal) |  |
| [getPriority()](#getPriority) | Gibt die Priorität der Schriftquellen zurück. |
| [getPriorityInternal()](#getPriorityInternal) |  |
| [getType()](#getType) | Gibt den Typ der Schriftquelle zurück. |
| [getWarningCallback()](#getWarningCallback) | Wird während der Verarbeitung der Schriftquelle aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Formattreue führen könnte. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Wird während der Verarbeitung der Schriftquelle aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Formattreue führen könnte. |
### getAvailableFonts() {#getAvailableFonts}
```
public ArrayList getAvailableFonts()
```


Gibt die Liste der über diese Quelle verfügbaren Schriftarten zurück.

 **Examples:** 

Zeigt, wie verfügbare Schriftarten aufgelistet werden.

```

 // Configure Aspose.Words to source fonts from a custom folder, and then print every available font.
 FontSourceBase[] folderFontSource = {new FolderFontSource(getFontsDir(), true)};

 for (PhysicalFontInfo fontInfo : folderFontSource[0].getAvailableFonts()) {
     System.out.println(MessageFormat.format("FontFamilyName : {0}", fontInfo.getFontFamilyName()));
     System.out.println(MessageFormat.format("FullFontName  : {0}", fontInfo.getFullFontName()));
     System.out.println(MessageFormat.format("Version  : {0}", fontInfo.getVersion()));
     System.out.println(MessageFormat.format("FilePath : {0}\n", fontInfo.getFilePath()));
 }
 
```

**Returns:**
java.util.ArrayList
### getFontDataInternal() {#getFontDataInternal}
```
public Iterable getFontDataInternal()
```




**Returns:**
java.lang.Iterable
### getPriority() {#getPriority}
```
public int getPriority()
```


Gibt die Priorität der Schriftquellen zurück.

 **Remarks:** 

Dieser Wert wird verwendet, wenn Schriftarten mit demselben Familiennamen und Stil in verschiedenen Schriftquellen vorhanden sind. In diesem Fall wählt Aspose.Words die Schriftart aus der Quelle mit dem höheren Prioritätswert aus.

Der Standardwert ist 0.

 **Examples:** 

Zeigt, wie eine Schriftdatei im lokalen Dateisystem als Schriftquelle verwendet wird.

```

 FileFontSource fileFontSource = new FileFontSource(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf", 0);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{fileFontSource});

 Assert.assertEquals(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.getFilePath());
 Assert.assertEquals(FontSourceType.FONT_FILE, fileFontSource.getType());
 Assert.assertEquals(0, fileFontSource.getPriority());
 
```

**Returns:**
int – Die Priorität der Schriftquelle.
### getPriorityInternal() {#getPriorityInternal}
```
public int getPriorityInternal()
```




**Returns:**
int
### getType() {#getType}
```
public abstract int getType()
```


Gibt den Typ der Schriftquelle zurück.

 **Examples:** 

Zeigt, wie eine Schriftdatei im lokalen Dateisystem als Schriftquelle verwendet wird.

```

 FileFontSource fileFontSource = new FileFontSource(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf", 0);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{fileFontSource});

 Assert.assertEquals(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.getFilePath());
 Assert.assertEquals(FontSourceType.FONT_FILE, fileFontSource.getType());
 Assert.assertEquals(0, fileFontSource.getPriority());
 
```

**Returns:**
int – Der Typ der Schriftquelle. Der zurückgegebene Wert ist einer der Konstanten von [FontSourceType](../../com.aspose.words/fontsourcetype/).
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


Wird während der Verarbeitung der Schriftquelle aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Formattreue führen könnte.

 **Examples:** 

Zeigt, wie der Warn-Callback aufgerufen wird, wenn die Schriftquellen verwendet werden.

```

 public void fontSourceWarning()
 {
     FontSettings settings = new FontSettings();
     settings.setFontsFolder("bad folder?", false);

     FontSourceBase source = settings.getFontsSources()[0];
     FontSourceWarningCollector callback = new FontSourceWarningCollector();
     source.setWarningCallback(callback);

     // Get the list of fonts to call warning callback.
     ArrayList fontInfos = source.getAvailableFonts();

     Assert.assertEquals("Error loading font from the folder \"bad folder?\": ",
         callback.FontSubstitutionWarnings.get(0).getDescription());
 }

 private static class FontSourceWarningCollector implements IWarningCallback
 {
     /// 
     /// Called every time a warning occurs during processing of font source.
     /// 
     public void warning(WarningInfo info)
     {
         FontSubstitutionWarnings.warning(info);
     }

     public WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
 }
 
```

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


Wird während der Verarbeitung der Schriftquelle aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Formattreue führen könnte.

 **Examples:** 

Zeigt, wie der Warn-Callback aufgerufen wird, wenn die Schriftquellen verwendet werden.

```

 public void fontSourceWarning()
 {
     FontSettings settings = new FontSettings();
     settings.setFontsFolder("bad folder?", false);

     FontSourceBase source = settings.getFontsSources()[0];
     FontSourceWarningCollector callback = new FontSourceWarningCollector();
     source.setWarningCallback(callback);

     // Get the list of fonts to call warning callback.
     ArrayList fontInfos = source.getAvailableFonts();

     Assert.assertEquals("Error loading font from the folder \"bad folder?\": ",
         callback.FontSubstitutionWarnings.get(0).getDescription());
 }

 private static class FontSourceWarningCollector implements IWarningCallback
 {
     /// 
     /// Called every time a warning occurs during processing of font source.
     /// 
     public void warning(WarningInfo info)
     {
         FontSubstitutionWarnings.warning(info);
     }

     public WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | Der entsprechende [IWarningCallback](../../com.aspose.words/iwarningcallback/) Wert. |

