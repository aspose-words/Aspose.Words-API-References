---
title: Document.RevisionsView
second_title: Aspose.Words per .NET API Reference
description: Document proprietà. Ottiene o imposta un valore che indica se lavorare con la versione originale o rivista di un documento.
type: docs
weight: 360
url: /it/net/aspose.words/document/revisionsview/
---
## Document.RevisionsView property

Ottiene o imposta un valore che indica se lavorare con la versione originale o rivista di un documento.

```csharp
public RevisionsView RevisionsView { get; set; }
```

### Osservazioni

Il valore predefinito è .

### Esempi

Mostra come passare dalla visualizzazione modificata a quella originale di un documento.

```csharp
Document doc = new Document(MyDir + "Revisions at list levels.docx");
doc.UpdateListLabels();

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;
Assert.AreEqual("1.", paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual(string.Empty, paragraphs[2].ListLabel.LabelString);

// Visualizza l'oggetto documento come se tutte le revisioni fossero accettate. Attualmente supporta le etichette degli elenchi.
doc.RevisionsView = RevisionsView.Final;

Assert.AreEqual(string.Empty, paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("1.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[2].ListLabel.LabelString);
```

### Guarda anche

* enum [RevisionsView](../../revisionsview/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)


