---
title: "FolderFontSource"
linktitle: "FolderFontSource"
second_title: "Aspose.Words для Java"
description: "Представляет папку, содержащую файлы шрифтов TrueType в Java."
type: docs
weight: 318
url: /ru/java/com.aspose.words/folderfontsource/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FontSourceBase](../../com.aspose.words/fontsourcebase/)
```
public class FolderFontSource extends FontSourceBase
```

Представляет папку, содержащую файлы шрифтов TrueType.

Чтобы узнать больше, посетите статью документации [ Working with Fonts ][Working with Fonts].

 **Examples:** 

Показывает, как использовать локальную системную папку, содержащую шрифты, в качестве источника шрифтов.

```

 // Create a font source from a folder that contains font files.
 FolderFontSource folderFontSource = new FolderFontSource(getFontsDir(), false, 1);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{folderFontSource});

 Assert.assertEquals(getFontsDir(), folderFontSource.getFolderPath());
 Assert.assertEquals(false, folderFontSource.getScanSubfolders());
 Assert.assertEquals(FontSourceType.FONTS_FOLDER, folderFontSource.getType());
 Assert.assertEquals(1, folderFontSource.getPriority());
 
```


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [FolderFontSource(String folderPath, boolean scanSubfolders)](#FolderFontSource-java.lang.String-boolean) | Конструктор. |
| [FolderFontSource(String folderPath, boolean scanSubfolders, int priority)](#FolderFontSource-java.lang.String-boolean-int) | Конструктор. |
## Методы

| Метод | Описание |
| --- | --- |
| [getAvailableFonts()](#getAvailableFonts) | Возвращает список шрифтов, доступных через этот источник. |
| [getFolderPath()](#getFolderPath) | Путь к папке. |
| [getFontDataInternal()](#getFontDataInternal) |  |
| [getPriority()](#getPriority) | Возвращает приоритет источника шрифтов. |
| [getPriorityInternal()](#getPriorityInternal) |  |
| [getScanSubfolders()](#getScanSubfolders) | Определяет, следует ли сканировать подпапки. |
| [getType()](#getType) | Возвращает тип источника шрифтов. |
| [getWarningCallback()](#getWarningCallback) | Вызывается при обработке источника шрифтов, когда обнаруживается проблема, которая может привести к потере точности форматирования. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Вызывается при обработке источника шрифтов, когда обнаруживается проблема, которая может привести к потере точности форматирования. |
### FolderFontSource(String folderPath, boolean scanSubfolders) {#FolderFontSource-java.lang.String-boolean}
```
public FolderFontSource(String folderPath, boolean scanSubfolders)
```


Конструктор.

 **Examples:** 

Показывает, как использовать локальную системную папку, содержащую шрифты, в качестве источника шрифтов.

```

 // Create a font source from a folder that contains font files.
 FolderFontSource folderFontSource = new FolderFontSource(getFontsDir(), false, 1);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{folderFontSource});

 Assert.assertEquals(getFontsDir(), folderFontSource.getFolderPath());
 Assert.assertEquals(false, folderFontSource.getScanSubfolders());
 Assert.assertEquals(FontSourceType.FONTS_FOLDER, folderFontSource.getType());
 Assert.assertEquals(1, folderFontSource.getPriority());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| folderPath | java.lang.String | Путь к папке. |
| scanSubfolders | boolean | Определяет, следует ли сканировать подпапки. |

### FolderFontSource(String folderPath, boolean scanSubfolders, int priority) {#FolderFontSource-java.lang.String-boolean-int}
```
public FolderFontSource(String folderPath, boolean scanSubfolders, int priority)
```


Конструктор.

 **Examples:** 

Показывает, как использовать локальную системную папку, содержащую шрифты, в качестве источника шрифтов.

```

 // Create a font source from a folder that contains font files.
 FolderFontSource folderFontSource = new FolderFontSource(getFontsDir(), false, 1);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{folderFontSource});

 Assert.assertEquals(getFontsDir(), folderFontSource.getFolderPath());
 Assert.assertEquals(false, folderFontSource.getScanSubfolders());
 Assert.assertEquals(FontSourceType.FONTS_FOLDER, folderFontSource.getType());
 Assert.assertEquals(1, folderFontSource.getPriority());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| folderPath | java.lang.String | Путь к папке. |
| scanSubfolders | boolean | Определяет, следует ли сканировать подпапки. |
| priority | int | Приоритет источника шрифтов. Смотрите описание свойства [FontSourceBase.getPriority()](../../com.aspose.words/fontsourcebase/\#getPriority) для получения дополнительной информации. |

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
### getFolderPath() {#getFolderPath}
```
public String getFolderPath()
```


Путь к папке.

 **Examples:** 

Показывает, как использовать локальную системную папку, содержащую шрифты, в качестве источника шрифтов.

```

 // Create a font source from a folder that contains font files.
 FolderFontSource folderFontSource = new FolderFontSource(getFontsDir(), false, 1);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{folderFontSource});

 Assert.assertEquals(getFontsDir(), folderFontSource.getFolderPath());
 Assert.assertEquals(false, folderFontSource.getScanSubfolders());
 Assert.assertEquals(FontSourceType.FONTS_FOLDER, folderFontSource.getType());
 Assert.assertEquals(1, folderFontSource.getPriority());
 
```

**Returns:**
java.lang.String - Соответствующее значение java.lang.String.
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
### getScanSubfolders() {#getScanSubfolders}
```
public boolean getScanSubfolders()
```


Определяет, следует ли сканировать подпапки.

 **Examples:** 

Показывает, как использовать локальную системную папку, содержащую шрифты, в качестве источника шрифтов.

```

 // Create a font source from a folder that contains font files.
 FolderFontSource folderFontSource = new FolderFontSource(getFontsDir(), false, 1);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{folderFontSource});

 Assert.assertEquals(getFontsDir(), folderFontSource.getFolderPath());
 Assert.assertEquals(false, folderFontSource.getScanSubfolders());
 Assert.assertEquals(FontSourceType.FONTS_FOLDER, folderFontSource.getType());
 Assert.assertEquals(1, folderFontSource.getPriority());
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getType() {#getType}
```
public int getType()
```


Возвращает тип источника шрифтов.

 **Examples:** 

Показывает, как использовать локальную системную папку, содержащую шрифты, в качестве источника шрифтов.

```

 // Create a font source from a folder that contains font files.
 FolderFontSource folderFontSource = new FolderFontSource(getFontsDir(), false, 1);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{folderFontSource});

 Assert.assertEquals(getFontsDir(), folderFontSource.getFolderPath());
 Assert.assertEquals(false, folderFontSource.getScanSubfolders());
 Assert.assertEquals(FontSourceType.FONTS_FOLDER, folderFontSource.getType());
 Assert.assertEquals(1, folderFontSource.getPriority());
 
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

