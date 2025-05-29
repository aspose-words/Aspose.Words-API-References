---
title: ConverterContext Class
linktitle: ConverterContext
articleTitle: ConverterContext
second_title: Aspose.Words per .NET
description: Scopri la potente classe Aspose.Words LowCode ConverterContext per una conversione fluida dei documenti e una maggiore efficienza del flusso di lavoro. Trasforma i tuoi documenti senza sforzo.
type: docs
weight: 4240
url: /it/net/aspose.words.lowcode/convertercontext/
---
## ConverterContext class

Contesto del convertitore di documenti

```csharp
public class ConverterContext : ProcessorContext
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [ConverterContext](convertercontext/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | Impostazioni del font utilizzate dal processore. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | Opzioni di layout del documento utilizzate dal processore. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | Callback di avviso utilizzato dal processore. |

## Esempi

Mostra come convertire documenti con una singola riga di codice utilizzando il contesto.

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

Mostra come convertire documenti da un flusso con una singola riga di codice utilizzando il contesto.

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

### Guarda anche

* class [ProcessorContext](../processorcontext/)
* spazio dei nomi [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../)
