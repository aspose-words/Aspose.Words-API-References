---
title: "IAiModelText"
linktitle: "IAiModelText"
second_title: "Aspose.Words para Java"
description: "La interfaz común para los modelos de IA diseñados para generar una variedad de contenido basado en texto en Java."
type: docs
weight: 748
url: /es/java/com.aspose.words/iaimodeltext/
---
```
public interface IAiModelText
```

La interfaz común para los modelos de IA diseñados para generar una variedad de contenido basado en texto.
## Métodos

| Método | Descripción |
| --- | --- |
| [checkGrammar(Document sourceDocument, CheckGrammarOptions options)](#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions) | Comprueba la gramática del documento proporcionado. |
| [summarize(Document sourceDocument, SummarizeOptions options)](#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions) | Genera un resumen del documento especificado, con opciones para ajustar la longitud del resumen. |
| [summarize(Document[] sourceDocuments, SummarizeOptions options)](#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions) | Genera resúmenes para una matriz de documentos, con opciones para controlar la longitud del resumen y otras configuraciones. |
| [translate(Document sourceDocument, int targetLanguage)](#translate-com.aspose.words.Document-int) |  |
### checkGrammar(Document sourceDocument, CheckGrammarOptions options) {#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions}
```
public abstract Document checkGrammar(Document sourceDocument, CheckGrammarOptions options)
```


Comprueba la gramática del documento proporcionado. Esta operación utiliza el modelo de IA conectado para comprobar la gramática del documento.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | El documento que se está comprobando para gramática. |
| options | [CheckGrammarOptions](../../com.aspose.words/checkgrammaroptions/) | Configuraciones opcionales para controlar cómo se comprobará la gramática. |

**Returns:**
[Document](../../com.aspose.words/document/) - A new [Document](../../com.aspose.words/document/) with checked grammar.
### summarize(Document sourceDocument, SummarizeOptions options) {#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions}
```
public abstract Document summarize(Document sourceDocument, SummarizeOptions options)
```


Genera un resumen del documento especificado, con opciones para ajustar la longitud del resumen. Esta operación utiliza el modelo de IA conectado para el procesamiento de contenido.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | El documento a resumir. |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | Configuraciones opcionales para controlar la longitud del resumen y otros parámetros. |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### summarize(Document[] sourceDocuments, SummarizeOptions options) {#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions}
```
public abstract Document summarize(Document[] sourceDocuments, SummarizeOptions options)
```


Genera resúmenes para una matriz de documentos, con opciones para controlar la longitud del resumen y otras configuraciones. Este método utiliza el modelo de IA conectado para procesar cada documento en la matriz.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sourceDocuments | [Document\[\]](../../com.aspose.words/document/) | Una matriz de documentos a resumir. |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | Configuraciones opcionales para controlar la longitud del resumen y otros parámetros |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### translate(Document sourceDocument, int targetLanguage) {#translate-com.aspose.words.Document-int}
```
public abstract Document translate(Document sourceDocument, int targetLanguage)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) |  |
| targetLanguage | int |  |

**Returns:**
[Document](../../com.aspose.words/document/)
