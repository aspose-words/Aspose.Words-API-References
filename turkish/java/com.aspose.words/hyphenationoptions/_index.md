---
title: "HyphenationOptions"
linktitle: "HyphenationOptions"
second_title: "Aspose.Words Java için"
description: "Java'da belge heceleme seçeneklerini yapılandırmaya izin verir."
type: docs
weight: 388
url: /tr/java/com.aspose.words/hyphenationoptions/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class HyphenationOptions implements Cloneable
```

Belge heceleme seçeneklerini yapılandırmaya izin verir.

Daha fazla bilgi için, [ Working with Hyphenation ][Working with Hyphenation] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Otomatik hecelemeyi nasıl yapılandıracağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```


[Working with Hyphenation]: https://docs.aspose.com/words/java/working-with-hyphenation/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getAutoHyphenation()](#getAutoHyphenation) | Belge için otomatik hecelemenin açık olup olmadığını belirleyen değeri alır. |
| [getConsecutiveHyphenLimit()](#getConsecutiveHyphenLimit) | Tire ile biten ardışık satırların azami sayısını alır. |
| [getHyphenateCaps()](#getHyphenateCaps) | Tamamen büyük harflerle yazılmış kelimelerin tirelenip tirelenmeyeceğini belirleyen değeri alır. |
| [getHyphenationZone()](#getHyphenationZone) | Sağ kenardan, kelimeleri tirelemek istemediğiniz 1/20 puan birimindeki mesafeyi alır. |
| [setAutoHyphenation(boolean value)](#setAutoHyphenation-boolean) | Belge için otomatik tirelemenin açık olup olmadığını belirleyen değeri ayarlar. |
| [setConsecutiveHyphenLimit(int value)](#setConsecutiveHyphenLimit-int) | Tire ile biten ardışık satırların azami sayısını ayarlar. |
| [setHyphenateCaps(boolean value)](#setHyphenateCaps-boolean) | Tamamen büyük harflerle yazılmış kelimelerin tirelenip tirelenmeyeceğini belirleyen değeri ayarlar. |
| [setHyphenationZone(int value)](#setHyphenationZone-int) | Sağ kenardan, kelimeleri tirelemek istemediğiniz 1/20 puan birimindeki mesafeyi ayarlar. |
### getAutoHyphenation() {#getAutoHyphenation}
```
public boolean getAutoHyphenation()
```


Belge için otomatik tirelemenin açık olup olmadığını belirleyen değeri alır. Bu özelliğin varsayılan değeri false.

 **Examples:** 

Otomatik hecelemeyi nasıl yapılandıracağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Returns:**
boolean - Belge için otomatik tirelemenin açık olup olmadığını belirleyen değer.
### getConsecutiveHyphenLimit() {#getConsecutiveHyphenLimit}
```
public int getConsecutiveHyphenLimit()
```


Tire ile biten ardışık satırların azami sayısını alır. Bu özelliğin varsayılan değeri 0.

 **Remarks:** 

Bu özelliğin değeri 0 olarak ayarlanırsa, tire ile biten herhangi sayıda ardışık satır olabilir.

Bu özellik, PDF gibi sabit sayfa formatlarına kaydedilirken etkili değildir.

 **Examples:** 

Otomatik hecelemeyi nasıl yapılandıracağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Returns:**
int - Tire ile biten ardışık satırların azami sayısı.
### getHyphenateCaps() {#getHyphenateCaps}
```
public boolean getHyphenateCaps()
```


Tamamen büyük harflerle yazılmış kelimelerin tirelenip tirelenmeyeceğini belirleyen değeri alır. Bu özelliğin varsayılan değeri true.

 **Examples:** 

Otomatik hecelemeyi nasıl yapılandıracağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Returns:**
boolean - Tamamen büyük harflerle yazılmış kelimelerin tirelenip tirelenmeyeceğini belirleyen değer.
### getHyphenationZone() {#getHyphenationZone}
```
public int getHyphenationZone()
```


Sağ kenardan, kelimeleri tirelemek istemediğiniz 1/20 puan birimindeki mesafeyi alır. Bu özelliğin varsayılan değeri 360 (0.25 inç).

 **Examples:** 

Otomatik hecelemeyi nasıl yapılandıracağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Returns:**
int - Sağ kenardan, kelimeleri tirelemek istemediğiniz 1/20 puan birimindeki mesafe.
### setAutoHyphenation(boolean value) {#setAutoHyphenation-boolean}
```
public void setAutoHyphenation(boolean value)
```


Belge için otomatik tirelemenin açık olup olmadığını belirleyen değeri ayarlar. Bu özelliğin varsayılan değeri false.

 **Examples:** 

Otomatik hecelemeyi nasıl yapılandıracağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Belge için otomatik tirelemenin açık olup olmadığını belirleyen değer. |

### setConsecutiveHyphenLimit(int value) {#setConsecutiveHyphenLimit-int}
```
public void setConsecutiveHyphenLimit(int value)
```


Tire ile biten ardışık satırların azami sayısını ayarlar. Bu özelliğin varsayılan değeri 0.

 **Remarks:** 

Bu özelliğin değeri 0 olarak ayarlanırsa, tire ile biten herhangi sayıda ardışık satır olabilir.

Bu özellik, PDF gibi sabit sayfa formatlarına kaydedilirken etkili değildir.

 **Examples:** 

Otomatik hecelemeyi nasıl yapılandıracağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Tire ile biten ardışık satırların azami sayısı. |

### setHyphenateCaps(boolean value) {#setHyphenateCaps-boolean}
```
public void setHyphenateCaps(boolean value)
```


Tamamen büyük harflerle yazılmış kelimelerin tirelenip tirelenmeyeceğini belirleyen değeri ayarlar. Bu özelliğin varsayılan değeri true.

 **Examples:** 

Otomatik hecelemeyi nasıl yapılandıracağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Tamamen büyük harflerle yazılmış kelimelerin tirelenip tirelenmeyeceğini belirleyen değer. |

### setHyphenationZone(int value) {#setHyphenationZone-int}
```
public void setHyphenationZone(int value)
```


Sağ kenardan, kelimeleri tirelemek istemediğiniz 1/20 puan birimindeki mesafeyi ayarlar. Bu özelliğin varsayılan değeri 360 (0.25 inç).

 **Examples:** 

Otomatik hecelemeyi nasıl yapılandıracağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Sağ kenardan, kelimeleri tirelemek istemediğiniz 1/20 puan birimindeki mesafe. |

