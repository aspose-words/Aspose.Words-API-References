---
title: MergerContext Class
linktitle: MergerContext
articleTitle: MergerContext
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words LowCode MergerContext-Klasse für nahtloses Zusammenführen von Dokumenten und steigern Sie die Produktivität mit leistungsstarken und effizienten Lösungen.
type: docs
weight: 4310
url: /de/net/aspose.words.lowcode/mergercontext/
---
## MergerContext class

Kontext der Dokumentzusammenführung.

```csharp
public class MergerContext : ProcessorContext
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [MergerContext](mergercontext/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | Vom Prozessor verwendete Schriftarteinstellungen. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | Vom Prozessor verwendete Dokumentlayoutoptionen. |
| [MergeFormatMode](../../aspose.words.lowcode/mergercontext/mergeformatmode/) { get; set; } | Gibt an, wie kollidierende Formatierungen zusammengeführt werden. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | Vom Prozessor verwendeter Warn-Callback. |

## Beispiele

Zeigt, wie Dokumente mithilfe des Kontexts zu einem einzigen Ausgabedokument zusammengeführt werden.

```csharp
//Es gibt mehrere Möglichkeiten, Dokumente zusammenzuführen:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1)
    .From(inputDoc2)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.1.docx")
    .Execute();

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1, firstLoadOptions)
    .From(inputDoc2, secondLoadOptions)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.2.docx", SaveFormat.Docx)
    .Execute();

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1)
    .From(inputDoc2)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.3.docx", saveOptions)
    .Execute();
```

Zeigt, wie Dokumente aus einem Stream mithilfe des Kontexts in ein einzelnes Ausgabedokument zusammengeführt werden.

```csharp
//Es gibt mehrere Möglichkeiten, Dokumente zusammenzuführen:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamContextDocuments.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
            .From(firstStreamIn)
            .From(secondStreamIn)
            .To(streamOut, saveOptions)
            .Execute();

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamContextDocuments.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
            .From(firstStreamIn, firstLoadOptions)
            .From(secondStreamIn, secondLoadOptions)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
    }
}
```

### Siehe auch

* class [ProcessorContext](../processorcontext/)
* namensraum [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../)
