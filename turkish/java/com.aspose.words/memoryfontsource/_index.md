---
title: "MemoryFontSource"
linktitle: "MemoryFontSource"
second_title: "Aspose.Words Java için"
description: "Java'da bellekte depolanan tek TrueType yazı tipi dosyasını temsil eder."
type: docs
weight: 461
url: /tr/java/com.aspose.words/memoryfontsource/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FontSourceBase](../../com.aspose.words/fontsourcebase/)
```
public class MemoryFontSource extends FontSourceBase
```

Bellekte depolanan tek TrueType yazı tipi dosyasını temsil eder.

Daha fazla bilgi için, [ Working with Fonts ][Working with Fonts] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Bir yazı tipi dosyasından gelen verilerle bir bayt dizisini yazı tipi kaynağı olarak nasıl kullanılacağını gösterir.

```

 byte[] fontBytes = DocumentHelper.getBytesFromStream(new FileInputStream(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf"));
 MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{memoryFontSource});

 Assert.assertEquals(FontSourceType.MEMORY_FONT, memoryFontSource.getType());
 Assert.assertEquals(0, memoryFontSource.getPriority());
 
```


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [MemoryFontSource(byte[] fontData)](#MemoryFontSource-byte) | Yapıcı. |
| [MemoryFontSource(byte[] fontData, int priority)](#MemoryFontSource-byte---int) | Yapıcı. |
| [MemoryFontSource(byte[] fontData, int priority, String cacheKey)](#MemoryFontSource-byte---int-java.lang.String) | Yapıcı. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getAvailableFonts()](#getAvailableFonts) | Bu kaynak üzerinden kullanılabilir yazı tiplerinin listesini döndürür. |
| [getCacheKey()](#getCacheKey) | Bu kaynağın önbellekteki anahtarı. |
| [getFontData()](#getFontData) | İkili yazı tipi verisi. |
| [getFontDataInternal()](#getFontDataInternal) |  |
| [getPriority()](#getPriority) | Yazı tipi kaynağı önceliğini döndürür. |
| [getPriorityInternal()](#getPriorityInternal) |  |
| [getType()](#getType) | Yazı tipi kaynağının türünü döndürür. |
| [getWarningCallback()](#getWarningCallback) | Biçimlendirme doğruluğunun kaybolmasına neden olabilecek bir sorun tespit edildiğinde, yazı tipi kaynağının işlenmesi sırasında çağrılır. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Biçimlendirme doğruluğunun kaybolmasına neden olabilecek bir sorun tespit edildiğinde, yazı tipi kaynağının işlenmesi sırasında çağrılır. |
### MemoryFontSource(byte[] fontData) {#MemoryFontSource-byte}
```
public MemoryFontSource(byte[] fontData)
```


Yapıcı.

 **Examples:** 

Bir yazı tipi dosyasından gelen verilerle bir bayt dizisini yazı tipi kaynağı olarak nasıl kullanılacağını gösterir.

```

 byte[] fontBytes = DocumentHelper.getBytesFromStream(new FileInputStream(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf"));
 MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{memoryFontSource});

 Assert.assertEquals(FontSourceType.MEMORY_FONT, memoryFontSource.getType());
 Assert.assertEquals(0, memoryFontSource.getPriority());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fontData | byte[] | İkili yazı tipi verisi. |

### MemoryFontSource(byte[] fontData, int priority) {#MemoryFontSource-byte---int}
```
public MemoryFontSource(byte[] fontData, int priority)
```


Yapıcı.

 **Examples:** 

Bir yazı tipi dosyasından gelen verilerle bir bayt dizisini yazı tipi kaynağı olarak nasıl kullanılacağını gösterir.

```

 byte[] fontBytes = DocumentHelper.getBytesFromStream(new FileInputStream(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf"));
 MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{memoryFontSource});

 Assert.assertEquals(FontSourceType.MEMORY_FONT, memoryFontSource.getType());
 Assert.assertEquals(0, memoryFontSource.getPriority());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fontData | byte[] | İkili yazı tipi verisi. |
| priority | int | Yazı tipi kaynağı önceliği. Daha fazla bilgi için [FontSourceBase.getPriority()](../../com.aspose.words/fontsourcebase/\#getPriority) özelliği açıklamasına bakın. |

### MemoryFontSource(byte[] fontData, int priority, String cacheKey) {#MemoryFontSource-byte---int-java.lang.String}
```
public MemoryFontSource(byte[] fontData, int priority, String cacheKey)
```


Yapıcı.

 **Examples:** 

Yazı tipi önbelleği başlatma sürecini nasıl hızlandıracağınızı gösterir.

```

 public void loadFontSearchCache() throws Exception
 {
     final String CACHE_KEY_1 = "Arvo";
     final String CACHE_KEY_2 = "Arvo-Bold";
     FontSettings parsedFonts = new FontSettings();
     FontSettings loadedCache = new FontSettings();

     parsedFonts.setFontsSources(new FontSourceBase[]
             {
                     new FileFontSource(getFontsDir() + "Arvo-Regular.ttf", 0, CACHE_KEY_1),
                     new FileFontSource(getFontsDir() + "Arvo-Bold.ttf", 0, CACHE_KEY_2)
             });

     try (ByteArrayOutputStream cacheStream = new ByteArrayOutputStream())
     {
         parsedFonts.saveSearchCache(cacheStream);
         ByteArrayInputStream inputStream = new ByteArrayInputStream(cacheStream.toByteArray());
         loadedCache.setFontsSources(new FontSourceBase[]
                 {
                         new SearchCacheStream(CACHE_KEY_1),
                         new MemoryFontSource(Files.readAllBytes(Paths.get(getFontsDir() + "Arvo-Bold.ttf")), 0, CACHE_KEY_2)
                 }, inputStream);
     }

     Assert.assertEquals(parsedFonts.getFontsSources().length, loadedCache.getFontsSources().length);
 }

 /// 
 /// Load the font data only when required instead of storing it in the memory
 /// for the entire lifetime of the "FontSettings" object.
 /// 
 private static class SearchCacheStream extends StreamFontSource
 {
     public SearchCacheStream(String cacheKey)
     {
         super(0, cacheKey);

     }

     public FileInputStream openFontDataStream() throws Exception
     {
         return new FileInputStream(getFontsDir() + "Arvo-Regular.ttf");
     }
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fontData | byte[] | İkili yazı tipi verisi. |
| priority | int | Yazı tipi kaynağı önceliği. Daha fazla bilgi için [FontSourceBase.getPriority()](../../com.aspose.words/fontsourcebase/\#getPriority) özelliği açıklamasına bakın. |
| cacheKey | java.lang.String | Bu kaynağın önbellekteki anahtarı. Daha fazla bilgi için [getCacheKey()](../../com.aspose.words/memoryfontsource/\#getCacheKey) özelliği açıklamasına bakın. |

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
### getCacheKey() {#getCacheKey}
```
public String getCacheKey()
```


Bu kaynağın önbellekteki anahtarı.

 **Remarks:** 

Bu anahtar, yazı tipi arama önbelleğini kaydederken/yüklerken kullanılan  ve  yöntemleriyle önbellek öğesini tanımlamak için kullanılır.

 **Examples:** 

Yazı tipi önbelleği başlatma sürecini nasıl hızlandıracağınızı gösterir.

```

 public void loadFontSearchCache() throws Exception
 {
     final String CACHE_KEY_1 = "Arvo";
     final String CACHE_KEY_2 = "Arvo-Bold";
     FontSettings parsedFonts = new FontSettings();
     FontSettings loadedCache = new FontSettings();

     parsedFonts.setFontsSources(new FontSourceBase[]
             {
                     new FileFontSource(getFontsDir() + "Arvo-Regular.ttf", 0, CACHE_KEY_1),
                     new FileFontSource(getFontsDir() + "Arvo-Bold.ttf", 0, CACHE_KEY_2)
             });

     try (ByteArrayOutputStream cacheStream = new ByteArrayOutputStream())
     {
         parsedFonts.saveSearchCache(cacheStream);
         ByteArrayInputStream inputStream = new ByteArrayInputStream(cacheStream.toByteArray());
         loadedCache.setFontsSources(new FontSourceBase[]
                 {
                         new SearchCacheStream(CACHE_KEY_1),
                         new MemoryFontSource(Files.readAllBytes(Paths.get(getFontsDir() + "Arvo-Bold.ttf")), 0, CACHE_KEY_2)
                 }, inputStream);
     }

     Assert.assertEquals(parsedFonts.getFontsSources().length, loadedCache.getFontsSources().length);
 }

 /// 
 /// Load the font data only when required instead of storing it in the memory
 /// for the entire lifetime of the "FontSettings" object.
 /// 
 private static class SearchCacheStream extends StreamFontSource
 {
     public SearchCacheStream(String cacheKey)
     {
         super(0, cacheKey);

     }

     public FileInputStream openFontDataStream() throws Exception
     {
         return new FileInputStream(getFontsDir() + "Arvo-Regular.ttf");
     }
 }
 
```

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getFontData() {#getFontData}
```
public byte[] getFontData()
```


İkili yazı tipi verisi.

 **Examples:** 

Bir yazı tipi dosyasından gelen verilerle bir bayt dizisini yazı tipi kaynağı olarak nasıl kullanılacağını gösterir.

```

 byte[] fontBytes = DocumentHelper.getBytesFromStream(new FileInputStream(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf"));
 MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{memoryFontSource});

 Assert.assertEquals(FontSourceType.MEMORY_FONT, memoryFontSource.getType());
 Assert.assertEquals(0, memoryFontSource.getPriority());
 
```

**Returns:**
byte[] - İlgili byte[] değeri.
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
### getType() {#getType}
```
public int getType()
```


Yazı tipi kaynağının türünü döndürür.

 **Examples:** 

Bir yazı tipi dosyasından gelen verilerle bir bayt dizisini yazı tipi kaynağı olarak nasıl kullanılacağını gösterir.

```

 byte[] fontBytes = DocumentHelper.getBytesFromStream(new FileInputStream(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf"));
 MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{memoryFontSource});

 Assert.assertEquals(FontSourceType.MEMORY_FONT, memoryFontSource.getType());
 Assert.assertEquals(0, memoryFontSource.getPriority());
 
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

