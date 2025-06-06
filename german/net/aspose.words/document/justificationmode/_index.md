---
title: Document.JustificationMode
linktitle: JustificationMode
articleTitle: JustificationMode
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie den Zeichenabstand Ihres Dokuments mit der JustificationMode-Eigenschaft optimieren. Verbessern Sie mühelos die Lesbarkeit und die Präsentation!
type: docs
weight: 240
url: /de/net/aspose.words/document/justificationmode/
---
## Document.JustificationMode property

Ruft die Zeichenabstandsanpassung eines Dokuments ab oder legt diese fest.

```csharp
public JustificationMode JustificationMode { get; set; }
```

## Beispiele

Zeigt, wie die Steuerung des Zeichenabstands verwaltet wird.

```csharp
Document doc = new Document(MyDir + "Document.docx");

JustificationMode justificationMode = doc.JustificationMode;
if (justificationMode == JustificationMode.Expand)
    doc.JustificationMode = JustificationMode.Compress;

doc.Save(ArtifactsDir + "Document.SetJustificationMode.docx");
```

### Siehe auch

* enum [JustificationMode](../../../aspose.words.settings/justificationmode/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
