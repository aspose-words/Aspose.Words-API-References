---
title: "CheckGrammarOptions"
linktitle: "CheckGrammarOptions"
second_title: "Aspose.Words per Java"
description: "Consente di specificare varie opzioni durante il controllo grammaticale di un documento usando AI in Java."
type: docs
weight: 101
url: /it/java/com.aspose.words/checkgrammaroptions/
---

**Inheritance:**
java.lang.Object
```
public class CheckGrammarOptions
```

Consente di specificare varie opzioni durante il controllo grammaticale di un documento usando l'IA.

 **Examples:** 

Mostra come controllare la grammatica di un documento.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getImproveStylistics()](#getImproveStylistics) | Consente di specificare se l'AI cercherà di migliorare la stilistica del testo in fase di correzione. |
| [getMakeRevisions()](#getMakeRevisions) | Consente di specificare se restituire un documento finale o revisionato con il testo corretto. |
| [getPreserveFormatting()](#getPreserveFormatting) | Consente di specificare se [AiModel.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/aimodel/\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) cercherà di preservare il layout e la formattazione del documento originale, o meno. |
| [setImproveStylistics(boolean value)](#setImproveStylistics-boolean) | Consente di specificare se l'AI cercherà di migliorare la stilistica del testo in fase di correzione. |
| [setMakeRevisions(boolean value)](#setMakeRevisions-boolean) | Consente di specificare se restituire un documento finale o revisionato con il testo corretto. |
| [setPreserveFormatting(boolean value)](#setPreserveFormatting-boolean) | Consente di specificare se [AiModel.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/aimodel/\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) cercherà di preservare il layout e la formattazione del documento originale, o meno. |
### getImproveStylistics() {#getImproveStylistics}
```
public boolean getImproveStylistics()
```


Consente di specificare se l'AI cercherà di migliorare la stilistica del testo in fase di correzione. Il valore predefinito è false.

**Returns:**
boolean - Il valore booleano corrispondente.
### getMakeRevisions() {#getMakeRevisions}
```
public boolean getMakeRevisions()
```


Consente di specificare se restituire il documento finale o revisionato con il testo corretto. Il valore predefinito è false.

**Returns:**
boolean - Il valore booleano corrispondente.
### getPreserveFormatting() {#getPreserveFormatting}
```
public boolean getPreserveFormatting()
```


Consente di specificare se [AiModel.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/aimodel/\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) cercherà di preservare il layout e la formattazione del documento originale, o meno. Il valore predefinito è true.

 **Remarks:** 

Quando l'opzione è impostata su false, la qualità del controllo grammaticale è superiore rispetto a quando l'opzione è impostata su true. Tuttavia, in questo caso la formattazione originale del testo non viene preservata.

**Returns:**
boolean - Il valore booleano corrispondente.
### setImproveStylistics(boolean value) {#setImproveStylistics-boolean}
```
public void setImproveStylistics(boolean value)
```


Consente di specificare se l'AI cercherà di migliorare la stilistica del testo in fase di correzione. Il valore predefinito è false.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setMakeRevisions(boolean value) {#setMakeRevisions-boolean}
```
public void setMakeRevisions(boolean value)
```


Consente di specificare se restituire il documento finale o revisionato con il testo corretto. Il valore predefinito è false.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setPreserveFormatting(boolean value) {#setPreserveFormatting-boolean}
```
public void setPreserveFormatting(boolean value)
```


Consente di specificare se [AiModel.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/aimodel/\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) cercherà di preservare il layout e la formattazione del documento originale, o meno. Il valore predefinito è true.

 **Remarks:** 

Quando l'opzione è impostata su false, la qualità del controllo grammaticale è superiore rispetto a quando l'opzione è impostata su true. Tuttavia, in questo caso la formattazione originale del testo non viene preservata.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

