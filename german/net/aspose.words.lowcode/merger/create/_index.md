---
title: Merger.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words für .NET
description: Entdecken Sie die Methode „Merger Create“, um mühelos eine neue Instanz eines Serienbriefprozessors für eine optimierte Dokumentenverarbeitung und verbesserte Effizienz zu erstellen.
type: docs
weight: 10
url: /de/net/aspose.words.lowcode/merger/create/
---
## Create() {#create}

Erstellt eine neue Instanz des Serienbriefprozessors.

```csharp
public static Merger Create()
```

### Siehe auch

* class [Merger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Create(*[MergerContext](../../mergercontext/)*) {#create_1}

Erstellt eine neue Instanz des Serienbriefprozessors.

```csharp
public static Merger Create(MergerContext context)
```

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

* class [MergerContext](../../mergercontext/)
* class [Merger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)
