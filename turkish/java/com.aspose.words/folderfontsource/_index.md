---
title: "FolderFontSource"
linktitle: "FolderFontSource"
second_title: "Aspose.Words Java için"
description: "Java'da TrueType yazı tipi dosyalarını içeren klasörü temsil eder."
type: docs
weight: 318
url: /tr/java/com.aspose.words/folderfontsource/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FontSourceBase](../../com.aspose.words/fontsourcebase/)
```
public class FolderFontSource extends FontSourceBase
```

TrueType yazı tipi dosyalarını içeren klasörü temsil eder.

Daha fazla bilgi için, [ Working with Fonts ][Working with Fonts] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Yazı tiplerini bir yazı tipi kaynağı olarak içeren yerel sistem klasörünün nasıl kullanılacağını gösterir.

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
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [FolderFontSource(String folderPath, boolean scanSubfolders)](#FolderFontSource-java.lang.String-boolean) | Yapıcı. |
| [FolderFontSource(String folderPath, boolean scanSubfolders, int priority)](#FolderFontSource-java.lang.String-boolean-int) | Yapıcı. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getAvailableFonts()](#getAvailableFonts) | Bu kaynak üzerinden kullanılabilir yazı tiplerinin listesini döndürür. |
| [getFolderPath()](#getFolderPath) | Klasörün yolu. |
| [getFontDataInternal()](#getFontDataInternal) |  |
| [getPriority()](#getPriority) | Yazı tipi kaynağı önceliğini döndürür. |
| [getPriorityInternal()](#getPriorityInternal) |  |
| [getScanSubfolders()](#getScanSubfolders) | Alt klasörlerin taranıp taranmayacağını belirler. |
| [getType()](#getType) | Yazı tipi kaynağının türünü döndürür. |
| [getWarningCallback()](#getWarningCallback) | Biçimlendirme doğruluğunun kaybolmasına neden olabilecek bir sorun tespit edildiğinde, yazı tipi kaynağının işlenmesi sırasında çağrılır. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Biçimlendirme doğruluğunun kaybolmasına neden olabilecek bir sorun tespit edildiğinde, yazı tipi kaynağının işlenmesi sırasında çağrılır. |
### FolderFontSource(String folderPath, boolean scanSubfolders) {#FolderFontSource-java.lang.String-boolean}
```
public FolderFontSource(String folderPath, boolean scanSubfolders)
```


Yapıcı.

 **Examples:** 

Yazı tiplerini bir yazı tipi kaynağı olarak içeren yerel sistem klasörünün nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| folderPath | java.lang.String | Klasörün yolu. |
| scanSubfolders | boolean | Alt klasörlerin taranıp taranmayacağını belirler. |

### FolderFontSource(String folderPath, boolean scanSubfolders, int priority) {#FolderFontSource-java.lang.String-boolean-int}
```
public FolderFontSource(String folderPath, boolean scanSubfolders, int priority)
```


Yapıcı.

 **Examples:** 

Yazı tiplerini bir yazı tipi kaynağı olarak içeren yerel sistem klasörünün nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| folderPath | java.lang.String | Klasörün yolu. |
| scanSubfolders | boolean | Alt klasörlerin taranıp taranmayacağını belirler. |
| priority | int | Yazı tipi kaynağı önceliği. Daha fazla bilgi için [FontSourceBase.getPriority()](../../com.aspose.words/fontsourcebase/\#getPriority) özelliği açıklamasına bakın. |

### getAvailableFonts() {#getAvailableFonts}
```
public ArrayList getAvailableFonts()
```


Bu kaynak üzerinden kullanılabilir yazı tiplerinin listesini döndürür.

 **Examples:** 

Kullanılabilir yazı tiplerini listelemenin nasıl yapılacağını gösterir.

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


Klasörün yolu.

 **Examples:** 

Yazı tiplerini bir yazı tipi kaynağı olarak içeren yerel sistem klasörünün nasıl kullanılacağını gösterir.

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
java.lang.String - İlgili java.lang.String değeri.
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


Yazı tipi kaynağı önceliğini döndürür.

 **Remarks:** 

Bu değer, farklı yazı tipi kaynaklarında aynı aile adı ve stile sahip yazı tipleri olduğunda kullanılır. Bu durumda Aspose.Words, daha yüksek öncelik değerine sahip kaynaktan yazı tipini seçer.

Varsayılan değer 0.

 **Examples:** 

Yerel dosya sistemindeki bir yazı tipi dosyasını yazı tipi kaynağı olarak kullanmanın nasıl yapılacağını gösterir.

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
int - Yazı tipi kaynağı önceliği.
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


Alt klasörlerin taranıp taranmayacağını belirler.

 **Examples:** 

Yazı tiplerini bir yazı tipi kaynağı olarak içeren yerel sistem klasörünün nasıl kullanılacağını gösterir.

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
boolean - İlgili  boolean  değeri.
### getType() {#getType}
```
public int getType()
```


Yazı tipi kaynağının türünü döndürür.

 **Examples:** 

Yazı tiplerini bir yazı tipi kaynağı olarak içeren yerel sistem klasörünün nasıl kullanılacağını gösterir.

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
int - Yazı tipi kaynağının türü. Döndürülen değer, [FontSourceType](../../com.aspose.words/fontsourcetype/) sabitlerinden biridir.
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


Biçimlendirme doğruluğunun kaybolmasına neden olabilecek bir sorun tespit edildiğinde, yazı tipi kaynağının işlenmesi sırasında çağrılır.

 **Examples:** 

Yazı tipi kaynaklarıyla çalışırken uyarı geri aramasını nasıl çağıracağınızı gösterir.

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


Biçimlendirme doğruluğunun kaybolmasına neden olabilecek bir sorun tespit edildiğinde, yazı tipi kaynağının işlenmesi sırasında çağrılır.

 **Examples:** 

Yazı tipi kaynaklarıyla çalışırken uyarı geri aramasını nasıl çağıracağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | İlgili [IWarningCallback](../../com.aspose.words/iwarningcallback/) değeri. |

