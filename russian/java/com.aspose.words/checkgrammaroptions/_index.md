---
title: "CheckGrammarOptions"
linktitle: "CheckGrammarOptions"
second_title: "Aspose.Words для Java"
description: "Позволяет указать различные параметры при проверке грамматики документа с использованием ИИ в Java."
type: docs
weight: 101
url: /ru/java/com.aspose.words/checkgrammaroptions/
---

**Inheritance:**
java.lang.Object
```
public class CheckGrammarOptions
```

Позволяет указать различные параметры при проверке грамматики документа с использованием ИИ.

 **Examples:** 

Показывает, как проверить грамматику документа.

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
## Методы

| Метод | Описание |
| --- | --- |
| [getImproveStylistics()](#getImproveStylistics) | Позволяет указать, будет ли ИИ пытаться улучшить стилистику проверяемого текста. |
| [getMakeRevisions()](#getMakeRevisions) | Позволяет указать, возвращать ли окончательный или исправленный документ с проверенным текстом. |
| [getPreserveFormatting()](#getPreserveFormatting) | Позволяет указать, будет ли [AiModel.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/aimodel/\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) пытаться сохранить макет и форматирование оригинального документа, или нет. |
| [setImproveStylistics(boolean value)](#setImproveStylistics-boolean) | Позволяет указать, будет ли ИИ пытаться улучшить стилистику проверяемого текста. |
| [setMakeRevisions(boolean value)](#setMakeRevisions-boolean) | Позволяет указать, возвращать ли окончательный или исправленный документ с проверенным текстом. |
| [setPreserveFormatting(boolean value)](#setPreserveFormatting-boolean) | Позволяет указать, будет ли [AiModel.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/aimodel/\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) пытаться сохранить макет и форматирование оригинального документа, или нет. |
### getImproveStylistics() {#getImproveStylistics}
```
public boolean getImproveStylistics()
```


Позволяет указать, будет ли ИИ пытаться улучшить стилистику проверяемого текста. Значение по умолчанию —  false .

**Returns:**
boolean - Соответствующее  boolean  значение.
### getMakeRevisions() {#getMakeRevisions}
```
public boolean getMakeRevisions()
```


Позволяет указать, какой документ — окончательный или исправленный — возвращать с проверенным текстом. Значение по умолчанию — false.

**Returns:**
boolean - Соответствующее  boolean  значение.
### getPreserveFormatting() {#getPreserveFormatting}
```
public boolean getPreserveFormatting()
```


Позволяет указать, будет ли [AiModel.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/aimodel/\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) пытаться сохранить макет и форматирование исходного документа, или нет. Значение по умолчанию — true.

 **Remarks:** 

Когда параметр установлен в false, качество проверки грамматики выше, чем когда он установлен в true. Однако в этом случае оригинальное форматирование текста не сохраняется.

**Returns:**
boolean - Соответствующее  boolean  значение.
### setImproveStylistics(boolean value) {#setImproveStylistics-boolean}
```
public void setImproveStylistics(boolean value)
```


Позволяет указать, будет ли ИИ пытаться улучшить стилистику проверяемого текста. Значение по умолчанию —  false .

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setMakeRevisions(boolean value) {#setMakeRevisions-boolean}
```
public void setMakeRevisions(boolean value)
```


Позволяет указать, какой документ — окончательный или исправленный — возвращать с проверенным текстом. Значение по умолчанию — false.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setPreserveFormatting(boolean value) {#setPreserveFormatting-boolean}
```
public void setPreserveFormatting(boolean value)
```


Позволяет указать, будет ли [AiModel.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/aimodel/\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) пытаться сохранить макет и форматирование исходного документа, или нет. Значение по умолчанию — true.

 **Remarks:** 

Когда параметр установлен в false, качество проверки грамматики выше, чем когда он установлен в true. Однако в этом случае оригинальное форматирование текста не сохраняется.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

