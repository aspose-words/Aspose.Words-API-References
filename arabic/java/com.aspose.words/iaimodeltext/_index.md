---
title: "IAiModelText"
linktitle: "IAiModelText"
second_title: "Aspose.Words لـ Java"
description: "الواجهة العامة لنماذج الذكاء الاصطناعي المصممة لتوليد مجموعة متنوعة من المحتوى النصي في جافا."
type: docs
weight: 748
url: /ar/java/com.aspose.words/iaimodeltext/
---
```
public interface IAiModelText
```

الواجهة العامة لنماذج الذكاء الاصطناعي المصممة لتوليد مجموعة متنوعة من المحتوى النصي.
## الطرق

| طريقة | الوصف |
| --- | --- |
| [checkGrammar(Document sourceDocument, CheckGrammarOptions options)](#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions) | يتحقق من قواعد اللغة في المستند المقدم. |
| [summarize(Document sourceDocument, SummarizeOptions options)](#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions) | ينشئ ملخصًا للمستند المحدد، مع خيارات لضبط طول الملخص. |
| [summarize(Document[] sourceDocuments, SummarizeOptions options)](#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions) | ينشئ ملخصات لمجموعة من المستندات، مع خيارات للتحكم في طول الملخص وإعدادات أخرى. |
| [translate(Document sourceDocument, int targetLanguage)](#translate-com.aspose.words.Document-int) |  |
### checkGrammar(Document sourceDocument, CheckGrammarOptions options) {#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions}
```
public abstract Document checkGrammar(Document sourceDocument, CheckGrammarOptions options)
```


يتحقق من قواعد اللغة في المستند المقدم. تستفيد هذه العملية من نموذج الذكاء الاصطناعي المتصل للتحقق من قواعد اللغة في المستند.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | المستند الذي يتم التحقق من قواعد لغته. |
| options | [CheckGrammarOptions](../../com.aspose.words/checkgrammaroptions/) | إعدادات اختيارية للتحكم في طريقة التحقق من القواعد. |

**Returns:**
[Document](../../com.aspose.words/document/) - A new [Document](../../com.aspose.words/document/) with checked grammar.
### summarize(Document sourceDocument, SummarizeOptions options) {#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions}
```
public abstract Document summarize(Document sourceDocument, SummarizeOptions options)
```


ينشئ ملخصًا للمستند المحدد، مع خيارات لضبط طول الملخص. تستفيد هذه العملية من نموذج الذكاء الاصطناعي المتصل لمعالجة المحتوى.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | المستند الذي سيُملَّخ. |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | إعدادات اختيارية للتحكم في طول الملخص ومعلمات أخرى. |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### summarize(Document[] sourceDocuments, SummarizeOptions options) {#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions}
```
public abstract Document summarize(Document[] sourceDocuments, SummarizeOptions options)
```


ينشئ ملخصات لمجموعة من المستندات، مع خيارات للتحكم في طول الملخص وإعدادات أخرى. تستخدم هذه الطريقة نموذج الذكاء الاصطناعي المتصل لمعالجة كل مستند في المجموعة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| sourceDocuments | [Document\[\]](../../com.aspose.words/document/) | مجموعة من المستندات التي سيتم تلخيصها. |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | إعدادات اختيارية للتحكم في طول الملخص ومعلمات أخرى |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### translate(Document sourceDocument, int targetLanguage) {#translate-com.aspose.words.Document-int}
```
public abstract Document translate(Document sourceDocument, int targetLanguage)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) |  |
| targetLanguage | int |  |

**Returns:**
[Document](../../com.aspose.words/document/)
