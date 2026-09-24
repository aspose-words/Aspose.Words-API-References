---
title: "WarningInfoCollection"
linktitle: "WarningInfoCollection"
second_title: "Aspose.Words Java için"
description: "Java'da WarningInfo nesnelerinden oluşan tiplenmiş bir koleksiyonu temsil eder."
type: docs
weight: 718
url: /tr/java/com.aspose.words/warninginfocollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
[com.aspose.words.IWarningCallback](../../com.aspose.words/iwarningcallback/), java.lang.Iterable
```
public class WarningInfoCollection implements IWarningCallback, Iterable
```

[WarningInfo](../../com.aspose.words/warninginfo/) nesnelerinden oluşan tiplenmiş bir koleksiyonu temsil eder.

Daha fazla bilgi için, [ Programming with Documents ][Programming with Documents] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Bu koleksiyon nesnesini, Aspose.Words'ün bir yükleme veya kaydetme işlemi sırasında ürettiği tüm uyarıları toplamak için [IWarningCallback](../../com.aspose.words/iwarningcallback/) uygulamasının en basit biçimi olarak kullanabilirsiniz. Bu sınıfın bir örneğini oluşturun ve onu [LoadOptions.getWarningCallback()](../../com.aspose.words/loadoptions/\#getWarningCallback) / [LoadOptions.setWarningCallback(com.aspose.words.IWarningCallback)](../../com.aspose.words/loadoptions/\#setWarningCallback-com.aspose.words.IWarningCallback) veya [DocumentBase.getWarningCallback()](../../com.aspose.words/documentbase/\#getWarningCallback) / [DocumentBase.setWarningCallback(com.aspose.words.IWarningCallback)](../../com.aspose.words/documentbase/\#setWarningCallback-com.aspose.words.IWarningCallback) özelliğine atayın.

 **Examples:** 

Mevcut yazı tipi kaynaklarından eksik bir yazı tipi için en yakın eşleşmeyi bulmak üzere özelliğin nasıl ayarlanacağını gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [clear()](#clear) | Koleksiyondaki tüm öğeleri kaldırır. |
| [get(int index)](#get-int) | Belirtilen indeksteki öğeyi alır. |
| [getCount()](#getCount) | Koleksiyonda bulunan öğe sayısını alır. |
| [iterator()](#iterator) | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir yineleyici nesnesi döndürür. |
| [warning(WarningInfo info)](#warning-com.aspose.words.WarningInfo) | [IWarningCallback](../../com.aspose.words/iwarningcallback/) arayüzünü uygular. |
### clear() {#clear}
```
public void clear()
```


Koleksiyondaki tüm öğeleri kaldırır.

 **Examples:** 

Mevcut yazı tipi kaynaklarından eksik bir yazı tipi için en yakın eşleşmeyi bulmak üzere özelliğin nasıl ayarlanacağını gösterir.

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


Belirtilen indeksteki öğeyi alır.

 **Examples:** 

Desteklenmeyen formatlarla ilgili uyarıların nasıl alınacağını gösterir.

```

 WarningInfoCollection warings = new WarningInfoCollection();
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setWarningCallback(warings);
 Document doc = new Document(getMyDir() + "FB2 document.fb2", loadOptions);

 Assert.assertEquals("The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warings.get(0).getDescription());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int | Öğenin sıfır tabanlı indeksi. |

**Returns:**
[WarningInfo](../../com.aspose.words/warninginfo/) - An item at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Koleksiyonda bulunan öğe sayısını alır.

 **Examples:** 

Desteklenmeyen formatlarla ilgili uyarıların nasıl alınacağını gösterir.

```

 WarningInfoCollection warings = new WarningInfoCollection();
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setWarningCallback(warings);
 Document doc = new Document(getMyDir() + "FB2 document.fb2", loadOptions);

 Assert.assertEquals("The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warings.get(0).getDescription());
 
```

**Returns:**
int - Koleksiyonda bulunan öğe sayısı.
### iterator() {#iterator}
```
public Iterator iterator()
```


Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir yineleyici nesnesi döndürür.

**Returns:**
java.util.Iterator
### warning(WarningInfo info) {#warning-com.aspose.words.WarningInfo}
```
public void warning(WarningInfo info)
```


[IWarningCallback](../../com.aspose.words/iwarningcallback/) arayüzünü uygular. Bu koleksiyona bir uyarı ekler.

 **Examples:** 

Mevcut yazı tipi kaynaklarından eksik bir yazı tipi için en yakın eşleşmeyi bulmak üzere özelliğin nasıl ayarlanacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| info | [WarningInfo](../../com.aspose.words/warninginfo/) |  |

