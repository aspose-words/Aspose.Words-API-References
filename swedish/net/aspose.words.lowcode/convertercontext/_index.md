---
title: ConverterContext Class
linktitle: ConverterContext
articleTitle: ConverterContext
second_title: Aspose.Words för .NET
description: Upptäck den kraftfulla Aspose.Words LowCode ConverterContext-klassen för sömlös dokumentkonvertering och förbättrad arbetsflödeseffektivitet. Transformera dina dokument utan ansträngning.
type: docs
weight: 4240
url: /sv/net/aspose.words.lowcode/convertercontext/
---
## ConverterContext class

Dokumentkonverterare context

```csharp
public class ConverterContext : ProcessorContext
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [ConverterContext](convertercontext/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | Typsnittsinställningar som används av processorn. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | Dokumentlayoutalternativ som används av processorn. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | Varningsåteranrop som används av processorn. |

## Exempel

Visar hur man konverterar dokument med en enda kodrad med hjälp av kontext.

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

Visar hur man konverterar dokument från en ström med en enda kodrad med hjälp av kontext.

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

### Se även

* class [ProcessorContext](../processorcontext/)
* namnutrymme [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../)
