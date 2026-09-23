---
title: "IAiModelText"
linktitle: "IAiModelText"
second_title: "Aspose.Words für Java"
description: "Die gemeinsame Schnittstelle für KI-Modelle, die entwickelt wurden, um eine Vielzahl von textbasierten Inhalten in Java zu erzeugen."
type: docs
weight: 748
url: /de/java/com.aspose.words/iaimodeltext/
---
```
public interface IAiModelText
```

Die gemeinsame Schnittstelle für KI-Modelle, die entwickelt wurden, um eine Vielzahl von textbasierten Inhalten zu erzeugen.
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [checkGrammar(Document sourceDocument, CheckGrammarOptions options)](#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions) | Überprüft die Grammatik des bereitgestellten Dokuments. |
| [summarize(Document sourceDocument, SummarizeOptions options)](#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions) | Erstellt eine Zusammenfassung des angegebenen Dokuments, mit Optionen zur Anpassung der Länge der Zusammenfassung. |
| [summarize(Document[] sourceDocuments, SummarizeOptions options)](#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions) | Erstellt Zusammenfassungen für ein Array von Dokumenten, mit Optionen zur Steuerung der Zusammenfassungslänge und anderer Einstellungen. |
| [translate(Document sourceDocument, int targetLanguage)](#translate-com.aspose.words.Document-int) |  |
### checkGrammar(Document sourceDocument, CheckGrammarOptions options) {#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions}
```
public abstract Document checkGrammar(Document sourceDocument, CheckGrammarOptions options)
```


Überprüft die Grammatik des bereitgestellten Dokuments. Dieser Vorgang nutzt das verbundene KI-Modell zur Grammatikprüfung des Dokuments.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | Das Dokument, das auf Grammatik überprüft wird. |
| options | [CheckGrammarOptions](../../com.aspose.words/checkgrammaroptions/) | Optionale Einstellungen zur Steuerung, wie die Grammatik überprüft wird. |

**Returns:**
[Document](../../com.aspose.words/document/) - A new [Document](../../com.aspose.words/document/) with checked grammar.
### summarize(Document sourceDocument, SummarizeOptions options) {#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions}
```
public abstract Document summarize(Document sourceDocument, SummarizeOptions options)
```


Erstellt eine Zusammenfassung des angegebenen Dokuments, mit Optionen zur Anpassung der Länge der Zusammenfassung. Dieser Vorgang nutzt das verbundene KI-Modell zur Inhaltsverarbeitung.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | Das zu zusammenfassende Dokument. |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | Optionale Einstellungen zur Steuerung der Zusammenfassungslänge und anderer Parameter. |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### summarize(Document[] sourceDocuments, SummarizeOptions options) {#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions}
```
public abstract Document summarize(Document[] sourceDocuments, SummarizeOptions options)
```


Erstellt Zusammenfassungen für ein Array von Dokumenten, mit Optionen zur Steuerung der Zusammenfassungslänge und anderer Einstellungen. Diese Methode nutzt das verbundene KI-Modell zur Verarbeitung jedes Dokuments im Array.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sourceDocuments | [Document\[\]](../../com.aspose.words/document/) | Ein Array von Dokumenten, die zusammengefasst werden sollen. |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | Optionale Einstellungen zur Steuerung der Zusammenfassungslänge und anderer Parameter |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### translate(Document sourceDocument, int targetLanguage) {#translate-com.aspose.words.Document-int}
```
public abstract Document translate(Document sourceDocument, int targetLanguage)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) |  |
| targetLanguage | int |  |

**Returns:**
[Document](../../com.aspose.words/document/)
