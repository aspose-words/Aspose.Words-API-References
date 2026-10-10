---
title: "NativeLibSettings"
linktitle: "NativeLibSettings"
second_title: "Aspose.Words Java için"
description: "Bu sınıf, Aspose.Words yerel kütüphaneleri için geçici klasör gibi çeşitli seçenekleri ayarlamaya ve yerel kütüphanelerin Java'da yüklenip kullanılmasını sağlamaya yardımcı olur."
type: docs
weight: 475
url: /tr/java/com.aspose.words/nativelibsettings/
---

**Inheritance:**
java.lang.Object
```
public class NativeLibSettings
```

Bu sınıf, Aspose.Words yerel kütüphaneleri için geçici klasör gibi çeşitli seçenekleri ayarlamaya ve yerel kütüphanelerin yüklenip kullanılmasını sağlamaya yardımcı olur.
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [clearAsposeNativeTmpDirectory()](#clearAsposeNativeTmpDirectory) | Aspose geçici kütüphanelerinin depolandığı dizini temizler. |
| [getInterruptThreadIfImageExceptionThrown()](#getInterruptThreadIfImageExceptionThrown) | Görüntü istisnalarında iş parçacığı kesilmesini kontrol eden özelliğin mevcut değerini döndürür. |
| [getTmpDirectoryPath()](#getTmpDirectoryPath) | Yerel kütüphanelerin geçici dizinine giden yolu döndürür. |
| [getUseJAIImageRendering()](#getUseJAIImageRendering) | Belge görüntülerinin oluşturulması sırasında JAI (Java Advanced Imaging) kullanılıp kullanılmayacağını belirleyen bir değer alır. |
| [isHarfBuzzNativeLibLoaded()](#isHarfBuzzNativeLibLoaded) | `true` döndürür eğer HarfBuzz kütüphaneleri yüklüyse. |
| [isWinNativeLibLoaded()](#isWinNativeLibLoaded) | `true` döndürür eğer WindowsNativeCall kütüphaneleri yüklüyse. |
| [loadHarfBuzzNativeLib()](#loadHarfBuzzNativeLib) | harfbuzz-shaping-engine-dll.dll kütüphanelerinin yüklenmesini ve kullanılmasını ayarlar. |
| [loadWinNativeLib()](#loadWinNativeLib) | Sets to load and use WindowsNativeCall\_x86 | \_x64.dll kütüphaneleri. |
| [setInterruptThreadIfImageExceptionThrown(boolean abortSavingIfImageExceptionThrown)](#setInterruptThreadIfImageExceptionThrown-boolean) | Görüntü istisnalarını işlerken davranışı tanımlayan özelliği ayarlar. |
| [setTmpDirectoryPath(String path)](#setTmpDirectoryPath-java.lang.String) | Yerel kütüphanelerin geçici dizinine giden yolu belirtir. |
| [setUseJAIImageRendering(boolean useJAIImageRendering)](#setUseJAIImageRendering-boolean) | Belge görüntülerinin oluşturulması sırasında JAI (Java Advanced Imaging) kullanılıp kullanılmayacağını belirleyen bir değeri ayarlar. |
| [skipHarfBuzzNativeLib()](#skipHarfBuzzNativeLib) | Yüklemeyi atla ve harfbuzz-shaping-engine-dll.dll kütüphanelerini kullan. |
| [skipWinNativeLib()](#skipWinNativeLib) | Skip loading and use WindowsNativeCall\_x86 | \_x64.dll kütüphaneleri. |
### clearAsposeNativeTmpDirectory() {#clearAsposeNativeTmpDirectory}
```
public static void clearAsposeNativeTmpDirectory()
```


Aspose geçici kütüphanelerinin depolandığı dizini temizler.

### getInterruptThreadIfImageExceptionThrown() {#getInterruptThreadIfImageExceptionThrown}
```
public static boolean getInterruptThreadIfImageExceptionThrown()
```


Görüntü istisnalarında iş parçacığı kesilmesini kontrol eden özelliğin mevcut değerini döndürür.

**Remarks:**

Varsayılan değer `false`'tır.

**Returns:**
boolean - iş parçacığının görüntü istisnalarında kesilip kesilmemesi.
### getTmpDirectoryPath() {#getTmpDirectoryPath}
```
public static String getTmpDirectoryPath()
```


Yerel kütüphanelerin geçici dizinine giden yolu döndürür.

**Returns:**
java.lang.String
### getUseJAIImageRendering() {#getUseJAIImageRendering}
```
public static boolean getUseJAIImageRendering()
```


Belge görüntülerinin oluşturulması sırasında JAI (Java Advanced Imaging) kullanılıp kullanılmayacağını belirleyen bir değer alır. Bazı durumlarda bu performansı artırabilir.

**Remarks:**

Varsayılan değer `true`'tır.

JAI, [burada][] açıklandığı gibi bir bağımlılık olarak eklenmişse kullanılacaktır. JAI devre dışı bırakılırsa bazı görüntüler doğru şekilde oluşturulmayabilir.


[here]: https://docs.aspose.com/words/java/system-requirements/#optional-dependencies

**Returns:**
boolean - JAI kullanılıyor mu.
### isHarfBuzzNativeLibLoaded() {#isHarfBuzzNativeLibLoaded}
```
public static boolean isHarfBuzzNativeLibLoaded()
```


`true` döndürür eğer HarfBuzz kütüphaneleri yüklüyse. Varsayılan olarak, yerel kütüphaneler yüklenir.

**Returns:**
boolean
### isWinNativeLibLoaded() {#isWinNativeLibLoaded}
```
public static boolean isWinNativeLibLoaded()
```


`true` döndürür eğer WindowsNativeCall kütüphaneleri yüklüyse. Varsayılan olarak, yerel kütüphaneler yüklenir.

**Returns:**
boolean
### loadHarfBuzzNativeLib() {#loadHarfBuzzNativeLib}
```
public static void loadHarfBuzzNativeLib()
```


harfbuzz-shaping-engine-dll.dll kütüphanelerinin yüklenmesini ve kullanılmasını ayarlar. Varsayılan olarak, yerel kütüphaneler yüklenir.

### loadWinNativeLib() {#loadWinNativeLib}
```
public static void loadWinNativeLib()
```


WindowsNativeCall\_x86|\_x64.dll kütüphanelerini yüklemeyi ve kullanmayı ayarlar. Varsayılan olarak, yerel kütüphaneler yüklenir.

### setInterruptThreadIfImageExceptionThrown(boolean abortSavingIfImageExceptionThrown) {#setInterruptThreadIfImageExceptionThrown-boolean}
```
public static void setInterruptThreadIfImageExceptionThrown(boolean abortSavingIfImageExceptionThrown)
```


Görüntü istisnalarını işlerken davranışı tanımlayan özelliği ayarlar. Özellik true olarak ayarlanırsa, görüntü işleme sırasında bir istisna oluştuğunda yürütme iş parçacığı kesilir.

**Remarks:**

Varsayılan değer `false`'tır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| abortSavingIfImageExceptionThrown | boolean | true - görüntü istisnalarında iş parçacığını kes, false - kesme |

### setTmpDirectoryPath(String path) {#setTmpDirectoryPath-java.lang.String}
```
public static void setTmpDirectoryPath(String path)
```


Yerel kütüphanelerin geçici dizinine giden yolu belirtir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| yol | java.lang.String | yerel kütüphanelerin geçici dizinine giden yol. |

### setUseJAIImageRendering(boolean useJAIImageRendering) {#setUseJAIImageRendering-boolean}
```
public static void setUseJAIImageRendering(boolean useJAIImageRendering)
```


Belge görüntülerinin render edilmesi sırasında JAI (Java Advanced Imaging) kullanılıp kullanılmayacağını belirleyen bir değeri ayarlar. Bazı durumlarda bu performansı artırabilir.

**Remarks:**

Varsayılan değer `true`'tır.

JAI, [burada][] açıklandığı gibi bir bağımlılık olarak eklenmişse kullanılacaktır. JAI devre dışı bırakılırsa bazı görüntüler doğru şekilde oluşturulmayabilir.


[here]: https://docs.aspose.com/words/java/system-requirements/#optional-dependencies

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| useJAIImageRendering | boolean | JAI kullanmak gerekli mi. |

### skipHarfBuzzNativeLib() {#skipHarfBuzzNativeLib}
```
public static void skipHarfBuzzNativeLib()
```


harfbuzz-shaping-engine-dll.dll kütüphanelerinin yüklenmesini atlayın ve kullanın. Varsayılan olarak, yerel kütüphaneler yüklenir.

### skipWinNativeLib() {#skipWinNativeLib}
```
public static void skipWinNativeLib()
```


WindowsNativeCall\_x86|\_x64.dll kütüphanelerinin yüklenmesini atlayın ve kullanın. Varsayılan olarak, yerel kütüphaneler yüklenir.

