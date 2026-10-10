---
title: "CheckGrammarOptions"
linktitle: "CheckGrammarOptions"
second_title: "Aspose.Words pour Java"
description: "Permet de spécifier diverses options lors de la vérification grammaticale d'un document à l'aide de l'IA en Java."
type: docs
weight: 101
url: /fr/java/com.aspose.words/checkgrammaroptions/
---

**Inheritance:**
java.lang.Object
```
public class CheckGrammarOptions
```

Permet de spécifier diverses options lors de la vérification grammaticale d'un document à l'aide de l'IA.

 **Examples:** 

Montre comment vérifier la grammaire d'un document.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [getImproveStylistics()](#getImproveStylistics) | Permet de spécifier que l'IA essaiera d'améliorer le style du texte en cours de révision. |
| [getMakeRevisions()](#getMakeRevisions) | Permet de spécifier que le document final ou révisé soit renvoyé avec le texte corrigé. |
| [getPreserveFormatting()](#getPreserveFormatting) | Permet de spécifier que [AiModel.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/aimodel/\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) essaiera de préserver la mise en page et le formatage du document original, ou non. |
| [setImproveStylistics(boolean value)](#setImproveStylistics-boolean) | Permet de spécifier que l'IA essaiera d'améliorer le style du texte en cours de révision. |
| [setMakeRevisions(boolean value)](#setMakeRevisions-boolean) | Permet de spécifier que le document final ou révisé soit renvoyé avec le texte corrigé. |
| [setPreserveFormatting(boolean value)](#setPreserveFormatting-boolean) | Permet de spécifier que [AiModel.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/aimodel/\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) essaiera de préserver la mise en page et le formatage du document original, ou non. |
### getImproveStylistics() {#getImproveStylistics}
```
public boolean getImproveStylistics()
```


Permet de spécifier que l'IA essaiera d'améliorer le style du texte en cours de révision. La valeur par défaut est false.

**Returns:**
boolean - La valeur  boolean  correspondante.
### getMakeRevisions() {#getMakeRevisions}
```
public boolean getMakeRevisions()
```


Permet de spécifier soit le document final, soit le document révisé à retourner avec le texte corrigé. La valeur par défaut est  false .

**Returns:**
boolean - La valeur  boolean  correspondante.
### getPreserveFormatting() {#getPreserveFormatting}
```
public boolean getPreserveFormatting()
```


Permet de spécifier soit [AiModel.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/aimodel/\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) qui tentera de préserver la mise en page et le formatage du document original, soit pas. La valeur par défaut est  true .

 **Remarks:** 

Lorsque l'option est définie sur  false , la qualité de la vérification grammaticale est supérieure à celle lorsque cette option est définie sur  true . Cependant, le formatage original du texte n'est pas conservé dans ce cas.

**Returns:**
boolean - La valeur  boolean  correspondante.
### setImproveStylistics(boolean value) {#setImproveStylistics-boolean}
```
public void setImproveStylistics(boolean value)
```


Permet de spécifier que l'IA essaiera d'améliorer le style du texte en cours de révision. La valeur par défaut est false.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setMakeRevisions(boolean value) {#setMakeRevisions-boolean}
```
public void setMakeRevisions(boolean value)
```


Permet de spécifier soit le document final, soit le document révisé à retourner avec le texte corrigé. La valeur par défaut est  false .

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setPreserveFormatting(boolean value) {#setPreserveFormatting-boolean}
```
public void setPreserveFormatting(boolean value)
```


Permet de spécifier soit [AiModel.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/aimodel/\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) qui tentera de préserver la mise en page et le formatage du document original, soit pas. La valeur par défaut est  true .

 **Remarks:** 

Lorsque l'option est définie sur  false , la qualité de la vérification grammaticale est supérieure à celle lorsque cette option est définie sur  true . Cependant, le formatage original du texte n'est pas conservé dans ce cas.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

