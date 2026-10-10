---
title: "CheckGrammarOptions"
linktitle: "CheckGrammarOptions"
second_title: "Aspose.Words Java için"
description: "Java'da AI kullanarak bir belgenin dilbilgisini kontrol ederken çeşitli seçenekler belirtmeye olanak tanır."
type: docs
weight: 101
url: /tr/java/com.aspose.words/checkgrammaroptions/
---

**Inheritance:**
java.lang.Object
```
public class CheckGrammarOptions
```

AI kullanarak bir belgenin dilbilgisini kontrol ederken çeşitli seçenekleri belirtmeye izin verir.

 **Examples:** 

Bir belgenin dilbilgisinin nasıl kontrol edileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 String apiKey = System.getenv("API_KEY");
 // Use OpenAI generative language models.
 AiModel model = AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey);

 CheckGrammarOptions grammarOptions = new CheckGrammarOptions();
 grammarOptions.setImproveStylistics(true);

 Document proofedDoc = model.checkGrammar(doc, grammarOptions);
 proofedDoc.save(getArtifactsDir() + "AI.AiGrammar.docx");
 
```
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getImproveStylistics()](#getImproveStylistics) | AI'nın incelenen metnin stilistiklerini iyileştirmeye çalışmasını belirtebilmenizi sağlar. |
| [getMakeRevisions()](#getMakeRevisions) | İspatlanmış metinle birlikte döndürülecek nihai veya revize edilmiş belgeyi belirtebilmenizi sağlar. |
| [getPreserveFormatting()](#getPreserveFormatting) | Bu, [AiModel.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/aimodel/\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) metodunun orijinal belgenin düzenini ve biçimlendirmesini korumaya çalışıp çalışmayacağını belirtebilmenizi sağlar. |
| [setImproveStylistics(boolean value)](#setImproveStylistics-boolean) | AI'nın incelenen metnin stilistiklerini iyileştirmeye çalışmasını belirtebilmenizi sağlar. |
| [setMakeRevisions(boolean value)](#setMakeRevisions-boolean) | İspatlanmış metinle birlikte döndürülecek nihai veya revize edilmiş belgeyi belirtebilmenizi sağlar. |
| [setPreserveFormatting(boolean value)](#setPreserveFormatting-boolean) | Bu, [AiModel.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/aimodel/\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) metodunun orijinal belgenin düzenini ve biçimlendirmesini korumaya çalışıp çalışmayacağını belirtebilmenizi sağlar. |
### getImproveStylistics() {#getImproveStylistics}
```
public boolean getImproveStylistics()
```


AI'nın incelenen metnin stilistiklerini iyileştirmeye çalışmasını belirtebilmenizi sağlar. Varsayılan değer false'tur.

**Returns:**
boolean - İlgili  boolean  değeri.
### getMakeRevisions() {#getMakeRevisions}
```
public boolean getMakeRevisions()
```


İspatlanmış metinle birlikte döndürülecek nihai veya revize edilmiş belgeyi belirtmeye izin verir. Varsayılan değer false.

**Returns:**
boolean - İlgili  boolean  değeri.
### getPreserveFormatting() {#getPreserveFormatting}
```
public boolean getPreserveFormatting()
```


İlk belgenin düzenini ve biçimlendirmesini korumaya çalışacak ya da çalışmayacak şekilde [AiModel.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/aimodel/\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) belirtmeye izin verir. Varsayılan değer true.

 **Remarks:** 

Seçenek false olarak ayarlandığında, dilbilgisi denetiminin kalitesi true olarak ayarlandığından daha yüksektir. Ancak bu durumda metnin orijinal biçimlendirmesi korunmaz.

**Returns:**
boolean - İlgili  boolean  değeri.
### setImproveStylistics(boolean value) {#setImproveStylistics-boolean}
```
public void setImproveStylistics(boolean value)
```


AI'nın incelenen metnin stilistiklerini iyileştirmeye çalışmasını belirtebilmenizi sağlar. Varsayılan değer false'tur.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setMakeRevisions(boolean value) {#setMakeRevisions-boolean}
```
public void setMakeRevisions(boolean value)
```


İspatlanmış metinle birlikte döndürülecek nihai veya revize edilmiş belgeyi belirtmeye izin verir. Varsayılan değer false.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setPreserveFormatting(boolean value) {#setPreserveFormatting-boolean}
```
public void setPreserveFormatting(boolean value)
```


İlk belgenin düzenini ve biçimlendirmesini korumaya çalışacak ya da çalışmayacak şekilde [AiModel.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/aimodel/\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) belirtmeye izin verir. Varsayılan değer true.

 **Remarks:** 

Seçenek false olarak ayarlandığında, dilbilgisi denetiminin kalitesi true olarak ayarlandığından daha yüksektir. Ancak bu durumda metnin orijinal biçimlendirmesi korunmaz.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

