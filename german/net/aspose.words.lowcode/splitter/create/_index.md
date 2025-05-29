---
title: Splitter.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words für .NET
description: Entdecken Sie mit unserer leicht verständlichen Anleitung, wie Sie effizient eine neue Instanz des Splitterprozessors erstellen, um eine nahtlose Integration und verbesserte Leistung zu gewährleisten.
type: docs
weight: 10
url: /de/net/aspose.words.lowcode/splitter/create/
---
## Splitter.Create method

Erstellt eine neue Instanz des Splitterprozessors.

```csharp
public static Splitter Create(SplitterContext context)
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

* class [SplitterContext](../../splittercontext/)
* class [Splitter](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)
