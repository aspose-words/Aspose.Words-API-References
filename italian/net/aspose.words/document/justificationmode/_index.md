---
title: Document.JustificationMode
second_title: Aspose.Words per .NET API Reference
description: Document proprietà. Ottiene o imposta la regolazione della spaziatura dei caratteri di un documento.
type: docs
weight: 230
url: /it/net/aspose.words/document/justificationmode/
---
## Document.JustificationMode property

Ottiene o imposta la regolazione della spaziatura dei caratteri di un documento.

```csharp
public JustificationMode JustificationMode { get; set; }
```

### Esempi

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
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)


