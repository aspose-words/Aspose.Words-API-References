---
title: Converter.Convert
linktitle: Convert
articleTitle: Convert
second_title: Aspose.Words pour .NET
description: Convertissez vos documents sans effort grâce à la méthode Convert de notre convertisseur. Transformez vos fichiers d'entrée aux formats souhaités avec facilité et précision.
type: docs
weight: 20
url: /fr/net/aspose.words.lowcode/converter/convert/
---
## Convert(*string, string*) {#convert_4}

Convertit le document d'entrée donné en document de sortie en utilisant les noms de fichiers d'entrée-sortie spécifiés et leurs extensions.

```csharp
public static void Convert(string inputFile, string outputFile)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFile | String | Le nom du fichier d'entrée. |
| outputFile | String | Le nom du fichier de sortie. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

## Exemples

Montre comment convertir des documents avec une seule ligne de code.

```csharp
string doc = MyDir + "Document.docx";

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.pdf");

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveFormat.rtf", SaveFormat.Rtf);

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Convert(doc, loadOptions, ArtifactsDir + "LowCode.Convert.LoadOptions.docx", saveOptions);

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveOptions.docx", saveOptions);
```

### Voir également

* class [Converter](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Convert(*string, string, [SaveFormat](../../../aspose.words/saveformat/)*) {#convert_5}

Convertit le document d'entrée donné en document de sortie en utilisant les noms de fichiers d'entrée-sortie spécifiés et le format du document final.

```csharp
public static void Convert(string inputFile, string outputFile, SaveFormat saveFormat)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFile | String | Le nom du fichier d'entrée. |
| outputFile | String | Le nom du fichier de sortie. |
| saveFormat | SaveFormat | Le format de sauvegarde. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

## Exemples

Montre comment convertir des documents avec une seule ligne de code.

```csharp
string doc = MyDir + "Document.docx";

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.pdf");

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveFormat.rtf", SaveFormat.Rtf);

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Convert(doc, loadOptions, ArtifactsDir + "LowCode.Convert.LoadOptions.docx", saveOptions);

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveOptions.docx", saveOptions);
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Convert(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#convert_6}

Convertit le document d'entrée donné en document de sortie en utilisant les noms de fichiers d'entrée et de sortie spécifiés et les options d'enregistrement.

```csharp
public static void Convert(string inputFile, string outputFile, SaveOptions saveOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFile | String | Le nom du fichier d'entrée. |
| outputFile | String | Le nom du fichier de sortie. |
| saveOptions | SaveOptions | Les options de sauvegarde. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

## Exemples

Montre comment convertir des documents avec une seule ligne de code.

```csharp
string doc = MyDir + "Document.docx";

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.pdf");

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveFormat.rtf", SaveFormat.Rtf);

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Convert(doc, loadOptions, ArtifactsDir + "LowCode.Convert.LoadOptions.docx", saveOptions);

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveOptions.docx", saveOptions);
```

### Voir également

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Converter](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Convert(*string, [LoadOptions](../../../aspose.words.loading/loadoptions/), string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#convert_3}

Convertit le document d'entrée donné en document de sortie en utilisant les noms de fichiers d'entrée/sortie spécifiés et ses options de chargement/enregistrement.

```csharp
public static void Convert(string inputFile, LoadOptions loadOptions, string outputFile, 
    SaveOptions saveOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFile | String | Le nom du fichier d'entrée. |
| loadOptions | LoadOptions | Les options de chargement du document d'entrée. |
| outputFile | String | Le nom du fichier de sortie. |
| saveOptions | SaveOptions | Les options de sauvegarde. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

## Exemples

Montre comment convertir des documents avec une seule ligne de code.

```csharp
string doc = MyDir + "Document.docx";

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.pdf");

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveFormat.rtf", SaveFormat.Rtf);

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Convert(doc, loadOptions, ArtifactsDir + "LowCode.Convert.LoadOptions.docx", saveOptions);

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveOptions.docx", saveOptions);
```

### Voir également

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Converter](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Convert(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/)*) {#convert_1}

Convertit le document d'entrée donné en un seul document de sortie à l'aide des flux d'entrée et de sortie spécifiés.

```csharp
public static void Convert(Stream inputStream, Stream outputStream, SaveFormat saveFormat)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux d'entrée. |
| outputStream | Stream | Le flux de sortie. |
| saveFormat | SaveFormat | Le format de sauvegarde. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images dans le flux spécifié.

## Exemples

Montre comment convertir des documents avec une seule ligne de code (Stream).

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, SaveFormat.Docx);

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, loadOptions, streamOut, saveOptions);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, saveOptions);
}
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Convert(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#convert_2}

Convertit le document d'entrée donné en un seul document de sortie à l'aide des flux d'entrée et de sortie spécifiés.

```csharp
public static void Convert(Stream inputStream, Stream outputStream, SaveOptions saveOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Les flux d'entrée. |
| outputStream | Stream | Le flux de sortie. |
| saveOptions | SaveOptions | Les options de sauvegarde. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images dans le flux spécifié.

## Exemples

Montre comment convertir des documents avec une seule ligne de code (Stream).

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, SaveFormat.Docx);

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, loadOptions, streamOut, saveOptions);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, saveOptions);
}
```

### Voir également

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Converter](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Convert(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/), Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#convert}

Convertit le document d'entrée donné en un seul document de sortie à l'aide des flux d'entrée et de sortie spécifiés.

```csharp
public static void Convert(Stream inputStream, LoadOptions loadOptions, Stream outputStream, 
    SaveOptions saveOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Les flux d'entrée. |
| loadOptions | LoadOptions | Les options de chargement du document d'entrée. |
| outputStream | Stream | Le flux de sortie. |
| saveOptions | SaveOptions | Les options de sauvegarde. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images dans le flux spécifié.

## Exemples

Montre comment convertir des documents avec une seule ligne de code (Stream).

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, SaveFormat.Docx);

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, loadOptions, streamOut, saveOptions);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, saveOptions);
}
```

### Voir également

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Converter](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)
