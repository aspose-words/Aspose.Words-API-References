---
title: "CheckGrammarOptions"
linktitle: "CheckGrammarOptions"
second_title: "Aspose.Words für Java"
description: "Ermöglicht das Festlegen verschiedener Optionen beim Prüfen der Grammatik eines Dokuments mit KI in Java."
type: docs
weight: 101
url: /de/java/com.aspose.words/checkgrammaroptions/
---

**Inheritance:**
java.lang.Object
```
public class CheckGrammarOptions
```

Ermöglicht die Angabe verschiedener Optionen beim Überprüfen der Grammatik eines Dokuments mit KI.

 **Examples:** 

Zeigt, wie man die Grammatik eines Dokuments prüft.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getImproveStylistics()](#getImproveStylistics) | Ermöglicht die Angabe, dass KI versucht, die Stilistik des zu prüfenden Textes zu verbessern. |
| [getMakeRevisions()](#getMakeRevisions) | Ermöglicht die Angabe, ob das endgültige oder überarbeitete Dokument mit korrigiertem Text zurückgegeben werden soll. |
| [getPreserveFormatting()](#getPreserveFormatting) | Ermöglicht die Angabe, ob entweder [AiModel.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/aimodel/\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) versucht, das Layout und die Formatierung des Originaldokuments beizubehalten, oder nicht. |
| [setImproveStylistics(boolean value)](#setImproveStylistics-boolean) | Ermöglicht die Angabe, dass KI versucht, die Stilistik des zu prüfenden Textes zu verbessern. |
| [setMakeRevisions(boolean value)](#setMakeRevisions-boolean) | Ermöglicht die Angabe, ob das endgültige oder überarbeitete Dokument mit korrigiertem Text zurückgegeben werden soll. |
| [setPreserveFormatting(boolean value)](#setPreserveFormatting-boolean) | Ermöglicht die Angabe, ob entweder [AiModel.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/aimodel/\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) versucht, das Layout und die Formatierung des Originaldokuments beizubehalten, oder nicht. |
### getImproveStylistics() {#getImproveStylistics}
```
public boolean getImproveStylistics()
```


Ermöglicht die Angabe, dass die KI versucht, die Stilistik des zu prüfenden Textes zu verbessern. Der Standardwert ist false.

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getMakeRevisions() {#getMakeRevisions}
```
public boolean getMakeRevisions()
```


Ermöglicht die Angabe, ob das endgültige oder überarbeitete Dokument mit korrigiertem Text zurückgegeben wird. Der Standardwert ist false.

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getPreserveFormatting() {#getPreserveFormatting}
```
public boolean getPreserveFormatting()
```


Ermöglicht die Angabe, ob entweder [AiModel.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/aimodel/\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) versucht, das Layout und die Formatierung des Originaldokuments beizubehalten, oder nicht. Der Standardwert ist true.

 **Remarks:** 

Wenn die Option auf false gesetzt ist, ist die Qualität der Grammatikprüfung höher als wenn diese Option auf true gesetzt ist. Allerdings wird in diesem Fall die ursprüngliche Formatierung des Textes nicht beibehalten.

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### setImproveStylistics(boolean value) {#setImproveStylistics-boolean}
```
public void setImproveStylistics(boolean value)
```


Ermöglicht die Angabe, dass die KI versucht, die Stilistik des zu prüfenden Textes zu verbessern. Der Standardwert ist false.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setMakeRevisions(boolean value) {#setMakeRevisions-boolean}
```
public void setMakeRevisions(boolean value)
```


Ermöglicht die Angabe, ob das endgültige oder überarbeitete Dokument mit korrigiertem Text zurückgegeben wird. Der Standardwert ist false.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setPreserveFormatting(boolean value) {#setPreserveFormatting-boolean}
```
public void setPreserveFormatting(boolean value)
```


Ermöglicht die Angabe, ob entweder [AiModel.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/aimodel/\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) versucht, das Layout und die Formatierung des Originaldokuments beizubehalten, oder nicht. Der Standardwert ist true.

 **Remarks:** 

Wenn die Option auf false gesetzt ist, ist die Qualität der Grammatikprüfung höher als wenn diese Option auf true gesetzt ist. Allerdings wird in diesem Fall die ursprüngliche Formatierung des Textes nicht beibehalten.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

