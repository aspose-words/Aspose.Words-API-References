---
title: Processor.From
linktitle: From
articleTitle: From
second_title: Aspose.Words pour .NET
description: Améliorez votre flux de travail avec notre processeur qui gère efficacement les documents d'entrée pour un traitement transparent et une productivité améliorée.
type: docs
weight: 20
url: /fr/net/aspose.words.lowcode/processor/from/
---
## From(*string, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#from_1}

Spécifie le document d'entrée pour le traitement.

```csharp
public Processor From(string input, LoadOptions loadOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| input | String | Nom du fichier du document d'entrée. |
| loadOptions | LoadOptions | Options de chargement facultatives utilisées pour charger le document. |

### Return_Value

Renvoie le processeur avec le fichier d'entrée spécifié.

## Remarques

Si le processeur n'accepte qu'un seul fichier en entrée, seul le dernier fichier spécifié sera traité. [`Merger`](../../merger/) le processeur accepte plusieurs fichiers en entrée, en conséquence tous les documents spécifiés seront fusionnés. [`Converter`](../../converter/) le processeur n'accepte qu'un seul fichier en entrée, donc seul le dernier fichier spécifié sera converti.

## Exemples

Montre comment convertir des documents avec une seule ligne de code en utilisant le contexte.

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

Montre comment fusionner des documents en un seul document de sortie à l'aide du contexte.

```csharp
//Il existe plusieurs façons de fusionner des documents :
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

### Voir également

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Processor](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## From(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#from}

Spécifie le document d'entrée pour le traitement.

```csharp
public Processor From(Stream input, LoadOptions loadOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| input | Stream | Flux de documents d'entrée. |
| loadOptions | LoadOptions | Options de chargement facultatives utilisées pour charger le document. |

### Return_Value

Renvoie le processeur avec le flux de fichiers d'entrée spécifié.

## Remarques

Si le processeur n'accepte qu'un seul fichier en entrée, seul le dernier fichier spécifié sera traité. [`Merger`](../../merger/) le processeur accepte plusieurs fichiers en entrée, en conséquence tous les documents spécifiés seront fusionnés. [`Converter`](../../converter/) le processeur n'accepte qu'un seul fichier en entrée, donc seul le dernier fichier spécifié sera converti.

## Exemples

Montre comment convertir des documents à partir d'un flux avec une seule ligne de code en utilisant le contexte.

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

Montre comment fusionner des documents d'un flux dans un seul document de sortie à l'aide du contexte.

```csharp
//Il existe plusieurs façons de fusionner des documents :
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

### Voir également

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Processor](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)
