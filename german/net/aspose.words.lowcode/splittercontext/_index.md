---
title: SplitterContext Class
linktitle: SplitterContext
articleTitle: SplitterContext
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.LowCode.SplitterContext für effizientes Dokumentaufteilen und verbessern Sie Ihren Workflow durch nahtlose Integration und leistungsstarke Funktionalität.
type: docs
weight: 4430
url: /de/net/aspose.words.lowcode/splittercontext/
---
## SplitterContext class

Dokument-Splitter-Kontext.

```csharp
public class SplitterContext : ProcessorContext
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [SplitterContext](splittercontext/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | Vom Prozessor verwendete Schriftarteinstellungen. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | Vom Prozessor verwendete Dokumentlayoutoptionen. |
| [SplitOptions](../../aspose.words.lowcode/splittercontext/splitoptions/) { get; } | Optionen zur Dokumentaufteilung. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | Vom Prozessor verwendeter Warn-Callback. |

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

* class [ProcessorContext](../processorcontext/)
* namensraum [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../)
