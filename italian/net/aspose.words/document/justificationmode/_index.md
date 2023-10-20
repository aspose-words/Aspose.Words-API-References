---
title: Document.JustificationMode
linktitle: JustificationMode
articleTitle: JustificationMode
second_title: Aspose.Words per .NET
description: Document JustificationMode proprietà. Ottiene o imposta la regolazione della spaziatura dei caratteri di un documento in C#.
type: docs
weight: 230
url: /it/net/aspose.words/document/justificationmode/
---
## Document.JustificationMode property

Ottiene o imposta la regolazione della spaziatura dei caratteri di un documento.

```csharp
public JustificationMode JustificationMode { get; set; }
```

## Esempi

Mostra come gestire il controllo della spaziatura dei caratteri.

```csharp
Document doc = new Document(MyDir + "Document.docx");

JustificationMode justificationMode = doc.JustificationMode;
if (justificationMode == JustificationMode.Expand)                
    doc.JustificationMode = JustificationMode.Compress;

doc.Save(ArtifactsDir + "Document.SetJustificationMode.docx");
```

### Guarda anche

* enum [JustificationMode](../../../aspose.words.settings/justificationmode/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
