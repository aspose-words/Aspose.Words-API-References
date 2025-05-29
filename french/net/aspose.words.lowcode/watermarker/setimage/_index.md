---
title: Watermarker.SetImage
linktitle: SetImage
articleTitle: SetImage
second_title: Aspose.Words pour .NET
description: Améliorez vos documents avec la méthode Watermarker SetImage. Ajoutez facilement des filigranes d'image personnalisés pour une touche professionnelle.
type: docs
weight: 20
url: /fr/net/aspose.words.lowcode/watermarker/setimage/
---
## SetImage(*string, string, string*) {#setimage_6}

Ajoute un filigrane d'image dans le document.

```csharp
public static void SetImage(string inputFileName, string outputFileName, 
    string watermarkImageFileName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |
| watermarkImageFileName | String | Image affichée en filigrane. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

## Exemples

Montre comment insérer une image de filigrane dans le document.

```csharp
string doc = MyDir + "Document.docx";
string watermarkImage = ImageDir + "Logo.jpg";

Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkImage.1.docx", watermarkImage);
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.2.docx", SaveFormat.Docx, watermarkImage);

ImageWatermarkOptions options = new ImageWatermarkOptions();
options.Scale = 50;
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.3.docx", watermarkImage, options);
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.4.docx", SaveFormat.Docx, watermarkImage, options);
```

### Voir également

* class [Watermarker](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## SetImage(*string, string, string, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage_7}

Ajoute un filigrane d'image dans le document avec des options.

```csharp
public static void SetImage(string inputFileName, string outputFileName, 
    string watermarkImageFileName, ImageWatermarkOptions options)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |
| watermarkImageFileName | String | Image affichée en filigrane. |
| options | ImageWatermarkOptions | Définit des options supplémentaires pour le filigrane de l'image. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

## Exemples

Montre comment insérer une image de filigrane dans le document.

```csharp
string doc = MyDir + "Document.docx";
string watermarkImage = ImageDir + "Logo.jpg";

Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkImage.1.docx", watermarkImage);
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.2.docx", SaveFormat.Docx, watermarkImage);

ImageWatermarkOptions options = new ImageWatermarkOptions();
options.Scale = 50;
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.3.docx", watermarkImage, options);
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.4.docx", SaveFormat.Docx, watermarkImage, options);
```

### Voir également

* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## SetImage(*string, string, [SaveFormat](../../../aspose.words/saveformat/), string, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage_4}

Ajoute un filigrane d'image dans le document avec des options et un format d'enregistrement spécifié.

```csharp
public static void SetImage(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    string watermarkImageFileName, ImageWatermarkOptions options = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |
| saveFormat | SaveFormat | Le format de sauvegarde. |
| watermarkImageFileName | String | Image affichée en filigrane. |
| options | ImageWatermarkOptions | Définit des options supplémentaires pour le filigrane de l'image. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

## Exemples

Montre comment insérer une image de filigrane dans le document.

```csharp
string doc = MyDir + "Document.docx";
string watermarkImage = ImageDir + "Logo.jpg";

Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkImage.1.docx", watermarkImage);
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.2.docx", SaveFormat.Docx, watermarkImage);

ImageWatermarkOptions options = new ImageWatermarkOptions();
options.Scale = 50;
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.3.docx", watermarkImage, options);
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.4.docx", SaveFormat.Docx, watermarkImage, options);
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## SetImage(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage_5}

Ajoute un filigrane d'image dans le document avec des options et un format d'enregistrement spécifié.

```csharp
public static void SetImage(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    string watermarkImageFileName, ImageWatermarkOptions options = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |
| saveOptions | SaveOptions | Les options de sauvegarde. |
| watermarkImageFileName | String | Image affichée en filigrane. |
| options | ImageWatermarkOptions | Définit des options supplémentaires pour le filigrane de l'image. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

### Voir également

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## SetImage(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), Image, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage}

Ajoute un filigrane d'image dans le document à partir de flux avec des options.

```csharp
public static void SetImage(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    Image watermarkImage, ImageWatermarkOptions options = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux d'entrée. |
| outputStream | Stream | Le flux de sortie. |
| saveFormat | SaveFormat | Le format de sauvegarde. |
| watermarkImage | Image | Image affichée en filigrane. |
| options | ImageWatermarkOptions | Définit des options supplémentaires pour le filigrane de l'image. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images dans le flux spécifié.

## Exemples

Montre comment insérer une image de filigrane dans le document à partir d'un flux.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.SetWatermarkText.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Watermarker.SetImage(streamIn, streamOut, SaveFormat.Docx, System.Drawing.Image.FromFile(ImageDir + "Logo.jpg"));
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.SetWatermarkText.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Watermarker.SetImage(streamIn, streamOut, SaveFormat.Docx, System.Drawing.Image.FromFile(ImageDir + "Logo.jpg"), new ImageWatermarkOptions() { Scale = 50 });
}
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## SetImage(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), Image, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage_2}

Ajoute un filigrane d'image dans le document à partir de flux avec des options.

```csharp
public static void SetImage(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    Image watermarkImage, ImageWatermarkOptions options = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux d'entrée. |
| outputStream | Stream | Le flux de sortie. |
| saveOptions | SaveOptions | Les options de sauvegarde. |
| watermarkImage | Image | Image affichée en filigrane. |
| options | ImageWatermarkOptions | Définit des options supplémentaires pour le filigrane de l'image. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images dans le flux spécifié.

### Voir également

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## SetImage(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), Stream, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage_1}

Ajoute un filigrane d'image dans le document à partir de flux avec des options.

```csharp
public static void SetImage(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    Stream watermarkImageStream, ImageWatermarkOptions options = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux d'entrée. |
| outputStream | Stream | Le flux de sortie. |
| saveFormat | SaveFormat | Le format de sauvegarde. |
| watermarkImageStream | Stream | Flux d'images affiché sous forme de filigrane. |
| options | ImageWatermarkOptions | Définit des options supplémentaires pour le filigrane de l'image. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images dans le flux spécifié.

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## SetImage(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), Stream, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage_3}

Ajoute un filigrane d'image dans le document à partir de flux avec des options.

```csharp
public static void SetImage(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    Stream watermarkImageStream, ImageWatermarkOptions options = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux d'entrée. |
| outputStream | Stream | Le flux de sortie. |
| saveOptions | SaveOptions | Les options de sauvegarde. |
| watermarkImageStream | Stream | Flux d'images affiché sous forme de filigrane. |
| options | ImageWatermarkOptions | Définit des options supplémentaires pour le filigrane de l'image. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images dans le flux spécifié.

### Voir également

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)
