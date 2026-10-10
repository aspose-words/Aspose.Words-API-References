---
title: "IAiModelText"
linktitle: "IAiModelText"
second_title: "Aspose.Words Java için"
description: "Java'da çeşitli metin tabanlı içerikler üretmek üzere tasarlanmış AI modelleri için ortak arayüz."
type: docs
weight: 748
url: /tr/java/com.aspose.words/iaimodeltext/
---
```
public interface IAiModelText
```

Çeşitli metin tabanlı içerikler üretmek üzere tasarlanmış AI modelleri için ortak arayüz.
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [checkGrammar(Document sourceDocument, CheckGrammarOptions options)](#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions) | Sağlanan belgenin dilbilgisini kontrol eder. |
| [summarize(Document sourceDocument, SummarizeOptions options)](#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions) | Belirtilen belgenin özetini oluşturur, özetin uzunluğunu ayarlama seçenekleriyle. |
| [summarize(Document[] sourceDocuments, SummarizeOptions options)](#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions) | Bir dizi belge için özetler oluşturur, özet uzunluğunu ve diğer ayarları kontrol etme seçenekleriyle. |
| [translate(Document sourceDocument, int targetLanguage)](#translate-com.aspose.words.Document-int) |  |
### checkGrammar(Document sourceDocument, CheckGrammarOptions options) {#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions}
```
public abstract Document checkGrammar(Document sourceDocument, CheckGrammarOptions options)
```


Sağlanan belgenin dilbilgisini kontrol eder. Bu işlem, belgenin dilbilgisini kontrol etmek için bağlı AI modelini kullanır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | Dilbilgisi kontrolü yapılan belge. |
| options | [CheckGrammarOptions](../../com.aspose.words/checkgrammaroptions/) | Dilbilgisinin nasıl kontrol edileceğini belirleyen isteğe bağlı ayarlar. |

**Returns:**
[Document](../../com.aspose.words/document/) - A new [Document](../../com.aspose.words/document/) with checked grammar.
### summarize(Document sourceDocument, SummarizeOptions options) {#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions}
```
public abstract Document summarize(Document sourceDocument, SummarizeOptions options)
```


Belirtilen belgenin özetini oluşturur, özetin uzunluğunu ayarlama seçenekleriyle. Bu işlem, içerik işleme için bağlı AI modelini kullanır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | Özetlenecek belge. |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | Özet uzunluğunu ve diğer parametreleri kontrol eden isteğe bağlı ayarlar. |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### summarize(Document[] sourceDocuments, SummarizeOptions options) {#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions}
```
public abstract Document summarize(Document[] sourceDocuments, SummarizeOptions options)
```


Bir dizi belge için özetler oluşturur, özet uzunluğunu ve diğer ayarları kontrol etme seçenekleriyle. Bu yöntem, dizideki her belgeyi işlemek için bağlı AI modelini kullanır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sourceDocuments | [Document\[\]](../../com.aspose.words/document/) | Özetlenecek belgeler dizisi. |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | Özet uzunluğunu ve diğer parametreleri kontrol eden isteğe bağlı ayarlar |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### translate(Document sourceDocument, int targetLanguage) {#translate-com.aspose.words.Document-int}
```
public abstract Document translate(Document sourceDocument, int targetLanguage)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) |  |
| targetLanguage | int |  |

**Returns:**
[Document](../../com.aspose.words/document/)
