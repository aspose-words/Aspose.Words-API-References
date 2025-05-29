---
title: Processor.To
linktitle: To
articleTitle: To
second_title: Aspose.Words pour .NET
description: Optimisez votre flux de travail avec notre méthode de traitement qui définit clairement les fichiers de sortie, améliorant ainsi l'efficacité et rationalisant vos tâches de gestion des données.
type: docs
weight: 30
url: /fr/net/aspose.words.lowcode/processor/to/
---
## To(*string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#to_5}

Spécifie le fichier de sortie pour le processeur.

```csharp
public Processor To(string output, SaveOptions saveOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| output | String | Nom du fichier de sortie. |
| saveOptions | SaveOptions | Options d'enregistrement facultatives. Si elles ne sont pas spécifiées, le format d'enregistrement est déterminé par l'extension du fichier. |

### Return_Value

Renvoie le processeur avec le fichier de sortie spécifié.

## Remarques

Si la sortie se compose de plusieurs fichiers, le nom du fichier de sortie spécifié est utilisé pour générer le nom de fichier pour chaque partie suivant la règle : 'outputFile_partIndex.extension'.

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

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Processor](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## To(*string, [SaveFormat](../../../aspose.words/saveformat/)*) {#to_4}

Spécifie le fichier de sortie pour le processeur.

```csharp
public Processor To(string output, SaveFormat saveFormat)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| output | String | Nom du fichier de sortie. |
| saveFormat | SaveFormat | Format d'enregistrement. Si non spécifié, le format d'enregistrement est déterminé par l'extension du fichier. |

### Return_Value

Renvoie le processeur avec le fichier de sortie spécifié.

## Remarques

Si la sortie se compose de plusieurs fichiers, le nom du fichier de sortie spécifié est utilisé pour générer le nom de fichier pour chaque partie suivant la règle : 'outputFile_partIndex.extension'.

## Exemples

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Processor](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## To(*Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#to_3}

Spécifie le flux de sortie pour le processeur.

```csharp
public Processor To(Stream output, SaveOptions saveOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| output | Stream | Flux de sortie. |
| saveOptions | SaveOptions | Enregistrer les options. |

### Return_Value

Renvoie le processeur avec le flux de sortie spécifié.

## Remarques

Si la sortie se compose de plusieurs fichiers, seule la première partie sera enregistrée dans le flux spécifié.

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

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Processor](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## To(*Stream, [SaveFormat](../../../aspose.words/saveformat/)*) {#to_2}

Spécifie le flux de sortie pour le processeur.

```csharp
public Processor To(Stream output, SaveFormat saveFormat)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| output | Stream | Flux de sortie. |
| saveFormat | SaveFormat | Enregistrer le format. |

### Return_Value

Renvoie le processeur avec le flux de sortie spécifié.

## Remarques

Si la sortie se compose de plusieurs fichiers, seule la première partie sera enregistrée dans le flux spécifié.

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Processor](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## To(*List&lt;Stream&gt;, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#to_1}

Spécifie la liste des flux de documents de sortie.

```csharp
public Processor To(List<Stream> output, SaveOptions saveOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| output | List`1 | Liste des flux de documents de sortie. |
| saveOptions | SaveOptions | Enregistrer les options. |

### Return_Value

Renvoie le processeur avec la liste des flux de documents de sortie spécifiés.

## Remarques

Si la sortie est constituée de plusieurs fichiers (tels que des images ou des parties de document divisées), un flux pour chaque partie est ajouté à la liste spécifiée. Si la sortie est un seul fichier, un seul flux est ajouté à la liste. Il est de la responsabilité de l'utilisateur final de se débarrasser des flux créés.

### Voir également

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Processor](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## To(*List&lt;Stream&gt;, [SaveFormat](../../../aspose.words/saveformat/)*) {#to}

Spécifie la liste des flux de documents de sortie.

```csharp
public Processor To(List<Stream> output, SaveFormat saveFormat)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| output | List`1 | Liste des flux de documents de sortie. |
| saveFormat | SaveFormat | Enregistrer le format. |

### Return_Value

Renvoie le processeur avec la liste des flux de documents de sortie spécifiés.

## Remarques

Si la sortie est constituée de plusieurs fichiers (tels que des images ou des parties de document divisées), un flux pour chaque partie est ajouté à la liste spécifiée. Si la sortie est un seul fichier, un seul flux est ajouté à la liste. Il est de la responsabilité de l'utilisateur final de se débarrasser des flux créés.

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Processor](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)
