---
title: "ImportFormatMode"
linktitle: "ImportFormatMode"
second_title: "Aspose.Words Java için"
description: "Java'da başka bir belgeden içerik içe aktarılırken biçimlendirmenin nasıl birleştirileceğini belirtir."
type: docs
weight: 400
url: /tr/java/com.aspose.words/importformatmode/
---

**Inheritance:**
java.lang.Object
```
public class ImportFormatMode
```

Başka bir belgeden içerik içe aktarılırken biçimlendirmenin nasıl birleştirileceğini belirtir.

 **Remarks:** 

Bir belgeden diğerine düğümler kopyaladığınızda, bu seçenek aynı ada sahip ancak farklı biçimlendirmeye sahip stiller olduğunda biçimlendirmenin nasıl çözüleceğini belirtir.

Biçimlendirme aşağıdaki gibi çözülür:

1.  Yerleşik stiller, bölge bağımsız stil tanımlayıcısı kullanılarak eşleştirilir. Kullanıcı tanımlı stiller, büyük/küçük harfe duyarlı stil adı kullanılarak eşleştirilir.
2.  Hedef belgede eşleşen bir stil bulunamazsa, stil (ve ona referans veren tüm stiller) hedef belgeye kopyalanır ve içe aktarılan düğümler yeni stile referans gösterecek şekilde güncellenir.
3.  Eğer hedef belgede eşleşen bir stil zaten varsa, ne olacağı importFormatMode parametresine bağlıdır ve bu parametre **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** metoduna geçirilir, aşağıda açıklandığı gibi.

When using the [USE\\_DESTINATION\\_STYLES](../../com.aspose.words/importformatmode/\\#USE-DESTINATION-STYLES) seçeneği kullanılırken, eğer hedef belgede eşleşen bir stil zaten varsa, stil kopyalanmaz ve içe aktarılan düğümler mevcut stile referans verecek şekilde güncellenir.

Kullanılan [USE\\_DESTINATION\\_STYLES](../../com.aspose.words/importformatmode/\\#USE-DESTINATION-STYLES) seçeneğinin dezavantajı, içe aktarılan metnin hedef belgede kaynak belgeye kıyasla farklı görünebilmesidir. Örneğin, kaynak belgede \"Heading 1\" stili Arial 16pt yazı tipini kullanırken, hedef belgede \"Heading 1\" stili Times New Roman 14pt yazı tipini kullanır. \"Heading 1\" stilindeki metin başka bir doğrudan biçimlendirme olmadan içe aktarıldığında, hedef belgede Times New Roman 14pt olarak görünecektir.

[KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) option allows to make sure the imported content looks the same in the destination document like it looks in the source document. If a matching style already exists in the destination document, the source style formatting is expanded into direct Node attributes and the style is changed to Normal. If the style does not exist in the destination document, then the source style is imported into the destination document and applied to the imported node. Note, that it is not always possible to preserve the source style even if it does not exist in the destination document. In this case formatting of such style will be expanded into direct Node attributes in favor of preserving original Node formatting.

Kullanılan [KEEP\\_SOURCE\\_FORMATTING](../../com.aspose.words/importformatmode/\\#KEEP-SOURCE-FORMATTING) seçeneğinin dezavantajı, birden fazla içe aktarma yaparsanız, hedef belgede çok sayıda stil oluşabilir ve bu da bu belge için Microsoft Word'de tutarlı stil biçimlendirmesi kullanmayı zorlaştırabilir.

[KEEP\\_DIFFERENT\\_STYLES](../../com.aspose.words/importformatmode/\\#KEEP-DIFFERENT-STYLES) seçeneğini kullanmak, sağladıkları biçimlendirme kaynak belgedeki stillerle aynıysa hedef stillerin yeniden kullanılmasını sağlar. Hedef belgede stil kaynak belgeden farklıysa, stil içe aktarılır.

 **Examples:** 

Bir belgeyi başka bir belgeye nasıl ekleyeceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.insertBreak(BreakType.PAGE_BREAK);

 Document docToInsert = new Document(getMyDir() + "Formatted elements.docx");

 builder.insertDocument(docToInsert, ImportFormatMode.KEEP_SOURCE_FORMATTING);
 builder.getDocument().save(getArtifactsDir() + "DocumentBuilder.InsertDocument.docx");
 
```

**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [KEEP_DIFFERENT_STYLES](#KEEP-DIFFERENT-STYLES) | Sadece kaynak belgede bulunanlardan farklı olan stiller kopyalanır. |
| [KEEP_SOURCE_FORMATTING](#KEEP-SOURCE-FORMATTING) | Gerekli tüm stilleri hedef belgeye kopyalayın, gerekirse benzersiz stil adları oluşturun. |
| [USE_DESTINATION_STYLES](#USE-DESTINATION-STYLES) | Hedef belgenin stillerini kullanın ve yeni stilleri kopyalayın. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String importFormatModeName)](#fromName-java.lang.String) |  |
| [getName(int importFormatMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int importFormatMode)](#toString-int) |  |
### KEEP_DIFFERENT_STYLES {#KEEP-DIFFERENT-STYLES}
```
public static int KEEP_DIFFERENT_STYLES
```


Sadece kaynak belgede bulunanlardan farklı olan stiller kopyalanır.

### KEEP_SOURCE_FORMATTING {#KEEP-SOURCE-FORMATTING}
```
public static int KEEP_SOURCE_FORMATTING
```


Gerekli tüm stilleri hedef belgeye kopyalayın, gerekirse benzersiz stil adları oluşturun.

### USE_DESTINATION_STYLES {#USE-DESTINATION-STYLES}
```
public static int USE_DESTINATION_STYLES
```


Hedef belgenin stillerini kullanın ve yeni stilleri kopyalayın. Bu varsayılan seçenektir.

### length {#length}
```
public static int length
```


### fromName(String importFormatModeName) {#fromName-java.lang.String}
```
public static int fromName(String importFormatModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| importFormatModeName | java.lang.String |  |

**Returns:**
int
### getName(int importFormatMode) {#getName-int}
```
public static String getName(int importFormatMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| importFormatMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int importFormatMode) {#toString-int}
```
public static String toString(int importFormatMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| importFormatMode | int |  |

**Returns:**
java.lang.String
