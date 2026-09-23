---
title: "IAiModelText"
linktitle: "IAiModelText"
second_title: "Aspose.Words pour Java"
description: "L'interface commune pour les modèles IA conçus pour générer une variété de contenu textuel en Java."
type: docs
weight: 748
url: /fr/java/com.aspose.words/iaimodeltext/
---
```
public interface IAiModelText
```

L'interface commune pour les modèles IA conçus pour générer une variété de contenu textuel.
## Méthodes

| Méthode | Description |
| --- | --- |
| [checkGrammar(Document sourceDocument, CheckGrammarOptions options)](#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions) | Vérifie la grammaire du document fourni. |
| [summarize(Document sourceDocument, SummarizeOptions options)](#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions) | Génère un résumé du document spécifié, avec des options pour ajuster la longueur du résumé. |
| [summarize(Document[] sourceDocuments, SummarizeOptions options)](#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions) | Génère des résumés pour un tableau de documents, avec des options pour contrôler la longueur du résumé et d'autres paramètres. |
| [translate(Document sourceDocument, int targetLanguage)](#translate-com.aspose.words.Document-int) |  |
### checkGrammar(Document sourceDocument, CheckGrammarOptions options) {#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions}
```
public abstract Document checkGrammar(Document sourceDocument, CheckGrammarOptions options)
```


Vérifie la grammaire du document fourni. Cette opération utilise le modèle IA connecté pour vérifier la grammaire du document.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | Le document dont la grammaire est vérifiée. |
| options | [CheckGrammarOptions](../../com.aspose.words/checkgrammaroptions/) | Paramètres optionnels pour contrôler la façon dont la grammaire sera vérifiée. |

**Returns:**
[Document](../../com.aspose.words/document/) - A new [Document](../../com.aspose.words/document/) with checked grammar.
### summarize(Document sourceDocument, SummarizeOptions options) {#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions}
```
public abstract Document summarize(Document sourceDocument, SummarizeOptions options)
```


Génère un résumé du document spécifié, avec des options pour ajuster la longueur du résumé. Cette opération utilise le modèle IA connecté pour le traitement du contenu.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | Le document à résumer. |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | Paramètres optionnels pour contrôler la longueur du résumé et d'autres paramètres. |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### summarize(Document[] sourceDocuments, SummarizeOptions options) {#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions}
```
public abstract Document summarize(Document[] sourceDocuments, SummarizeOptions options)
```


Génère des résumés pour un tableau de documents, avec des options pour contrôler la longueur du résumé et d'autres paramètres. Cette méthode utilise le modèle IA connecté pour le traitement de chaque document du tableau.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sourceDocuments | [Document\[\]](../../com.aspose.words/document/) | Un tableau de documents à résumer. |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | Paramètres optionnels pour contrôler la longueur du résumé et d'autres paramètres |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### translate(Document sourceDocument, int targetLanguage) {#translate-com.aspose.words.Document-int}
```
public abstract Document translate(Document sourceDocument, int targetLanguage)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) |  |
| targetLanguage | int |  |

**Returns:**
[Document](../../com.aspose.words/document/)
