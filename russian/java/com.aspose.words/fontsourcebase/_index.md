---
title: "FontSourceBase"
linktitle: "FontSourceBase"
second_title: "Aspose.Words для Java"
description: "Это абстрактный базовый класс для классов, позволяющих пользователю указывать различные источники шрифтов в Java."
type: docs
weight: 333
url: /ru/java/com.aspose.words/fontsourcebase/
---

**Inheritance:**
java.lang.Object
```
public abstract class FontSourceBase
```

Это абстрактный базовый класс для классов, позволяющих пользователю указывать различные источники шрифтов.

Чтобы узнать больше, посетите статью документации [ Working with Fonts ][Working with Fonts].

 **Examples:** 

Показывает, как использовать файл шрифта в локальной файловой системе в качестве источника шрифтов.

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
## Методы

| Метод | Описание |
| --- | --- |
| [getAvailableFonts()](#getAvailableFonts) | Возвращает список шрифтов, доступных через этот источник. |
| [getFontDataInternal()](#getFontDataInternal) |  |
| [getPriority()](#getPriority) | Возвращает приоритет источника шрифтов. |
| [getPriorityInternal()](#getPriorityInternal) |  |
| [getType()](#getType) | Возвращает тип источника шрифтов. |
| [getWarningCallback()](#getWarningCallback) | Вызывается при обработке источника шрифтов, когда обнаруживается проблема, которая может привести к потере точности форматирования. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Вызывается при обработке источника шрифтов, когда обнаруживается проблема, которая может привести к потере точности форматирования. |
### getAvailableFonts() {#getAvailableFonts}
```
public ArrayList getAvailableFonts()
```


Возвращает список шрифтов, доступных через этот источник.

 **Examples:** 

Показывает, как вывести список доступных шрифтов.

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


Возвращает приоритет источника шрифтов.

 **Remarks:** 

Это значение используется, когда в разных источниках шрифтов есть шрифты с одинаковым названием семейства и стилем. В этом случае Aspose.Words выбирает шрифт из источника с более высоким значением приоритета.

Значение по умолчанию — 0.

 **Examples:** 

Показывает, как использовать файл шрифта в локальной файловой системе в качестве источника шрифтов.

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
int - Приоритет источника шрифтов.
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


Возвращает тип источника шрифтов.

 **Examples:** 

Показывает, как использовать файл шрифта в локальной файловой системе в качестве источника шрифтов.

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
int - Тип источника шрифтов. Возвращаемое значение является одной из констант [FontSourceType](../../com.aspose.words/fontsourcetype/).
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


Вызывается при обработке источника шрифтов, когда обнаруживается проблема, которая может привести к потере точности форматирования.

 **Examples:** 

Показывает, как вызвать обратный вызов предупреждения при работе с источниками шрифтов.

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


Вызывается при обработке источника шрифтов, когда обнаруживается проблема, которая может привести к потере точности форматирования.

 **Examples:** 

Показывает, как вызвать обратный вызов предупреждения при работе с источниками шрифтов.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | Соответствующее значение [IWarningCallback](../../com.aspose.words/iwarningcallback/). |

