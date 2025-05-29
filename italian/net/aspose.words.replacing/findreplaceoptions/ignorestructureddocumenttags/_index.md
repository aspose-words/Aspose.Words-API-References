---
title: FindReplaceOptions.IgnoreStructuredDocumentTags
linktitle: IgnoreStructuredDocumentTags
articleTitle: IgnoreStructuredDocumentTags
second_title: Aspose.Words per .NET
description: Scopri la proprietà FindReplaceOptions IgnoreStructuredDocumentTags. Controlla se il contenuto di StructuredDocumentTag viene ignorato con questa impostazione booleana di facile utilizzo.
type: docs
weight: 120
url: /it/net/aspose.words.replacing/findreplaceoptions/ignorestructureddocumenttags/
---
## FindReplaceOptions.IgnoreStructuredDocumentTags property

Ottiene o imposta un valore booleano che indica di ignorare il contenuto di[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) . Il valore predefinito è`falso` .

```csharp
public bool IgnoreStructuredDocumentTags { get; set; }
```

## Osservazioni

Quando questa opzione è impostata su`VERO` , il contenuto di[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) verrà trattato come un testo semplice.

Altrimenti,[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) verrà elaborato come Story autonomo e il modello sostitutivo verrà cercato separatamente per ciascuno[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) , in modo che se il modello attraversa un[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) , quindi la sostituzione non verrà eseguita per tale modello.

## Esempi

Mostra come ignorare il contenuto dei tag dalla sostituzione.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

// Questo paragrafo contiene SDT.
Paragraph p = (Paragraph)doc.FirstSection.Body.GetChild(NodeType.Paragraph, 2, true);
string textToSearch = p.ToString(SaveFormat.Text).Trim();

FindReplaceOptions options = new FindReplaceOptions() { IgnoreStructuredDocumentTags = true };
doc.Range.Replace(textToSearch, "replacement", options);

doc.Save(ArtifactsDir + "StructuredDocumentTag.IgnoreStructuredDocumentTags.docx");
```

### Guarda anche

* class [FindReplaceOptions](../)
* spazio dei nomi [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* assemblea [Aspose.Words](../../../)
