---
title: SplitterContext.SplitOptions
linktitle: SplitOptions
articleTitle: SplitOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie mit der SplitOptions-Eigenschaft von SplitterContext Ihr Dokumentenmanagement optimieren und Inhalte effizient und flexibel aufteilen können. Verbessern Sie noch heute Ihren Workflow.
type: docs
weight: 20
url: /de/net/aspose.words.lowcode/splittercontext/splitoptions/
---
## SplitterContext.SplitOptions property

Optionen zur Dokumentaufteilung.

```csharp
public SplitOptions SplitOptions { get; }
```

## Beispiele

Zeigt, wie ein Dokument mithilfe des Kontexts seitenweise aufgeteilt wird.

```csharp
string doc = MyDir + "Big document.docx";

SplitterContext splitterContext = new SplitterContext();
splitterContext.SplitOptions.SplitCriteria = SplitCriteria.Page;

Splitter.Create(splitterContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.SplitContextDocument.docx")
    .Execute();
```

Zeigt, wie Dokumente mithilfe des Kontexts seitenweise aus dem Stream aufgeteilt werden.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    SplitterContext splitterContext = new SplitterContext();
    splitterContext.SplitOptions.SplitCriteria = SplitCriteria.Page;

    List<Stream> pages = new List<Stream>();
    Splitter.Create(splitterContext)
        .From(streamIn)
        .To(pages, SaveFormat.Docx)
        .Execute();
}
```

### Siehe auch

* class [SplitOptions](../../splitoptions/)
* class [SplitterContext](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)
