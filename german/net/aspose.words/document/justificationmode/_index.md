---
title: Document.JustificationMode
second_title: Aspose.Words für .NET-API-Referenz
description: Document eigendom. Ruft die Zeichenabstandsanpassung eines Dokuments ab oder legt diese fest.
type: docs
weight: 230
url: /de/net/aspose.words/document/justificationmode/
---
## Document.JustificationMode property

Ruft die Zeichenabstandsanpassung eines Dokuments ab oder legt diese fest.

```csharp
public JustificationMode JustificationMode { get; set; }
```

### Beispiele

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
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)


