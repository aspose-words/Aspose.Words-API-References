---
title: "CheckGrammarOptions"
linktitle: "CheckGrammarOptions"
second_title: "Aspose.Words para Java"
description: "Permite especificar varias opciones al comprobar la gramática de un documento usando IA en Java."
type: docs
weight: 101
url: /es/java/com.aspose.words/checkgrammaroptions/
---

**Inheritance:**
java.lang.Object
```
public class CheckGrammarOptions
```

Permite especificar varias opciones al comprobar la gramática de un documento usando IA.

 **Examples:** 

Muestra cómo comprobar la gramática de un documento.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [getImproveStylistics()](#getImproveStylistics) | Permite especificar que la IA intentará mejorar el estilo del texto que se está revisando. |
| [getMakeRevisions()](#getMakeRevisions) | Permite especificar si se debe devolver el documento final o revisado con el texto corregido. |
| [getPreserveFormatting()](#getPreserveFormatting) | Permite especificar que [AiModel.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/aimodel/\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) intentará preservar el diseño y el formato del documento original, o no. |
| [setImproveStylistics(boolean value)](#setImproveStylistics-boolean) | Permite especificar que la IA intentará mejorar el estilo del texto que se está revisando. |
| [setMakeRevisions(boolean value)](#setMakeRevisions-boolean) | Permite especificar si se debe devolver el documento final o revisado con el texto corregido. |
| [setPreserveFormatting(boolean value)](#setPreserveFormatting-boolean) | Permite especificar que [AiModel.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/aimodel/\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) intentará preservar el diseño y el formato del documento original, o no. |
### getImproveStylistics() {#getImproveStylistics}
```
public boolean getImproveStylistics()
```


Permite especificar que la IA intentará mejorar el estilo del texto que se está revisando. El valor predeterminado es false.

**Returns:**
boolean - El valor  boolean  correspondiente.
### getMakeRevisions() {#getMakeRevisions}
```
public boolean getMakeRevisions()
```


Permite especificar si se devuelve el documento final o revisado con el texto corregido. El valor predeterminado es false.

**Returns:**
boolean - El valor  boolean  correspondiente.
### getPreserveFormatting() {#getPreserveFormatting}
```
public boolean getPreserveFormatting()
```


Permite especificar si [AiModel.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/aimodel/\\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) intentará preservar el diseño y formato del documento original, o no. El valor predeterminado es true.

 **Remarks:** 

Cuando la opción está establecida en false, la calidad de la corrección gramatical es mayor que cuando la opción está establecida en true. Sin embargo, el formato original del texto no se conserva en este caso.

**Returns:**
boolean - El valor  boolean  correspondiente.
### setImproveStylistics(boolean value) {#setImproveStylistics-boolean}
```
public void setImproveStylistics(boolean value)
```


Permite especificar que la IA intentará mejorar el estilo del texto que se está revisando. El valor predeterminado es false.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setMakeRevisions(boolean value) {#setMakeRevisions-boolean}
```
public void setMakeRevisions(boolean value)
```


Permite especificar si se devuelve el documento final o revisado con el texto corregido. El valor predeterminado es false.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setPreserveFormatting(boolean value) {#setPreserveFormatting-boolean}
```
public void setPreserveFormatting(boolean value)
```


Permite especificar si [AiModel.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/aimodel/\\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) intentará preservar el diseño y formato del documento original, o no. El valor predeterminado es true.

 **Remarks:** 

Cuando la opción está establecida en false, la calidad de la corrección gramatical es mayor que cuando la opción está establecida en true. Sin embargo, el formato original del texto no se conserva en este caso.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

