---
title: ConverterContext Class
linktitle: ConverterContext
articleTitle: ConverterContext
second_title: Aspose.Words für .NET
description: Entdecken Sie die leistungsstarke Aspose.Words LowCode ConverterContext-Klasse für nahtlose Dokumentkonvertierung und verbesserte Workflow-Effizienz. Transformieren Sie Ihre Dokumente mühelos.
type: docs
weight: 4240
url: /de/net/aspose.words.lowcode/convertercontext/
---
## ConverterContext class

Dokumentkonverterkontext

```csharp
public class ConverterContext : ProcessorContext
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [ConverterContext](convertercontext/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | Vom Prozessor verwendete Schriftarteinstellungen. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | Vom Prozessor verwendete Dokumentlayoutoptionen. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | Vom Prozessor verwendeter Warn-Callback. |

## Beispiele

Zeigt, wie Dokumente mithilfe von Kontext mit einer einzigen Codezeile konvertiert werden.

```csharp
string doc = MyDir + "Big document.docx";

Converter.Create(new ConverterContext())
    .From(doc)
    .To(ArtifactsDir + "LowCode.ConvertContext.1.pdf")
    .Execute();

Converter.Create(new ConverterContext())
    .From(doc)
    .To(ArtifactsDir + "LowCode.ConvertContext.2.pdf", SaveFormat.Rtf)
    .Execute();

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Create(new ConverterContext())
    .From(doc, loadOptions)
    .To(ArtifactsDir + "LowCode.ConvertContext.3.docx", saveOptions)
    .Execute();

Converter.Create(new ConverterContext())
    .From(doc)
    .To(ArtifactsDir + "LowCode.ConvertContext.4.png", new ImageSaveOptions(SaveFormat.Png))
    .Execute();
```

Zeigt, wie Dokumente aus einem Stream mithilfe von Kontext mit einer einzigen Codezeile konvertiert werden.

```csharp
string doc = MyDir + "Document.docx";
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertContextStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Create(new ConverterContext())
            .From(streamIn)
            .To(streamOut, SaveFormat.Rtf)
            .Execute();

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertContextStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Create(new ConverterContext())
            .From(streamIn, loadOptions)
            .To(streamOut, saveOptions)
            .Execute();

    List<Stream> pages = new List<Stream>();
    Converter.Create(new ConverterContext())
        .From(doc)
        .To(pages, new ImageSaveOptions(SaveFormat.Png))
        .Execute();
}
```

### Siehe auch

* class [ProcessorContext](../processorcontext/)
* namensraum [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../)
