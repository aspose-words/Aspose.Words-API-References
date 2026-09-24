---
title: "StreamFontSource"
linktitle: "StreamFontSource"
second_title: "Aspose.Words Java için"
description: "Java'da kullanıcı tanımlı akış yazı tipi kaynağı için temel sınıf."
type: docs
weight: 635
url: /tr/java/com.aspose.words/streamfontsource/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FontSourceBase](../../com.aspose.words/fontsourcebase/)
```
public abstract class StreamFontSource extends FontSourceBase
```

Kullanıcı tanımlı akış yazı tipi kaynağı için temel sınıf.

Daha fazla bilgi için, [ Working with Fonts ][Working with Fonts] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Akış yazı tipi kaynağını kullanmak için, [StreamFontSource](../../com.aspose.words/streamfontsource/) üzerinden türetilmiş bir sınıf oluşturmalı ve [openFontDataStream()](../../com.aspose.words/streamfontsource/\#openFontDataStream) yöntemini uygulamalısınız.

[openFontDataStream()](../../com.aspose.words/streamfontsource/\#openFontDataStream) method could be called several times. For the first time it will be called when Aspose.Words scans the provided font sources to get the list of available fonts. Later it may be called if the font is used in the document to parse the font data and to embed the font data to some output formats.

[StreamFontSource](../../com.aspose.words/streamfontsource/) may be useful because it allows to load the font data only when it is required and not to store it in the memory for the [FontSettings](../../com.aspose.words/fontsettings/) lifetime.

 **Examples:** 

Yazı tiplerini akıştan nasıl yükleyeceğinizi gösterir.

```

 public void streamFontSourceFileRendering() throws Exception {
     FontSettings fontSettings = new FontSettings();
     fontSettings.setFontsSources(new FontSourceBase[]{new StreamFontSourceFile()});

     DocumentBuilder builder = new DocumentBuilder();
     builder.getDocument().setFontSettings(fontSettings);
     builder.getFont().setName("Kreon-Regular");
     builder.writeln("Test aspose text when saving to PDF.");

     builder.getDocument().save(getArtifactsDir() + "FontSettings.StreamFontSourceFileRendering.pdf");
 }

 /// 
 /// Load the font data only when required instead of storing it in the memory for the entire lifetime of the "FontSettings" object.
 /// 
 private static class StreamFontSourceFile extends StreamFontSource  {
     public FileInputStream openFontDataStream() throws Exception {
         return new FileInputStream(getFontsDir() + "Kreon-Regular.ttf");
     }
 }
 
```


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getAvailableFonts()](#getAvailableFonts) | Bu kaynak üzerinden kullanılabilir yazı tiplerinin listesini döndürür. |
| [getCacheKey()](#getCacheKey) | Bu kaynağın önbellekteki anahtarı. |
| [getCacheKeyInternal()](#getCacheKeyInternal) |  |
| [getFilePath()](#getFilePath) |  |
| [getFontBytes()](#getFontBytes) |  |
| [getFontDataInternal()](#getFontDataInternal) |  |
| [getPriority()](#getPriority) | Yazı tipi kaynağı önceliğini döndürür. |
| [getPriorityInternal()](#getPriorityInternal) |  |
| [getSize()](#getSize) |  |
| [getType()](#getType) | Yazı tipi kaynağının türünü döndürür. |
| [getWarningCallback()](#getWarningCallback) | Biçimlendirme doğruluğunun kaybolmasına neden olabilecek bir sorun tespit edildiğinde, yazı tipi kaynağının işlenmesi sırasında çağrılır. |
| [isEmbedded()](#isEmbedded) |  |
| [openFontDataStream()](#openFontDataStream) | Bu yöntem, talep üzerine yazı tipi verileri içeren akışı açmalıdır. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Biçimlendirme doğruluğunun kaybolmasına neden olabilecek bir sorun tespit edildiğinde, yazı tipi kaynağının işlenmesi sırasında çağrılır. |
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
### getCacheKeyInternal() {#getCacheKeyInternal}
```
public String getCacheKeyInternal()
```




**Returns:**
java.lang.String
### getFilePath() {#getFilePath}
```
public String getFilePath()
```




**Returns:**
java.lang.String
### getFontBytes() {#getFontBytes}
```
public byte[] getFontBytes()
```




**Returns:**
byte[]
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
### getSize() {#getSize}
```
public int getSize()
```




**Returns:**
int
### getType() {#getType}
```
public int getType()
```


Yazı tipi kaynağının türünü döndürür.

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
### isEmbedded() {#isEmbedded}
```
public boolean isEmbedded()
```




**Returns:**
boolean
### openFontDataStream() {#openFontDataStream}
```
public abstract InputStream openFontDataStream()
```


Bu yöntem, talep üzerine yazı tipi verileri içeren akışı açmalıdır.

 **Remarks:** 

Akış okunduktan sonra kapatılacaktır. Bunu açıkça kapatmanıza gerek yoktur.

 **Examples:** 

Yazı tiplerini akıştan nasıl yükleyeceğinizi gösterir.

```

 public void streamFontSourceFileRendering() throws Exception {
     FontSettings fontSettings = new FontSettings();
     fontSettings.setFontsSources(new FontSourceBase[]{new StreamFontSourceFile()});

     DocumentBuilder builder = new DocumentBuilder();
     builder.getDocument().setFontSettings(fontSettings);
     builder.getFont().setName("Kreon-Regular");
     builder.writeln("Test aspose text when saving to PDF.");

     builder.getDocument().save(getArtifactsDir() + "FontSettings.StreamFontSourceFileRendering.pdf");
 }

 /// 
 /// Load the font data only when required instead of storing it in the memory for the entire lifetime of the "FontSettings" object.
 /// 
 private static class StreamFontSourceFile extends StreamFontSource  {
     public FileInputStream openFontDataStream() throws Exception {
         return new FileInputStream(getFontsDir() + "Kreon-Regular.ttf");
     }
 }
 
```

**Returns:**
java.io.InputStream - Yazı tipi veri akışı.
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

