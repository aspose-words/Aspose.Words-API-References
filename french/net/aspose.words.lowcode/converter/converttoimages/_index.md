---
title: Converter.ConvertToImages
linktitle: ConvertToImages
articleTitle: ConvertToImages
second_title: Aspose.Words pour .NET
description: Transformez vos documents sans effort avec ConvertToImages. Convertissez rapidement et facilement des pages en fichiers image de haute qualité pour un partage et un stockage optimisés.
type: docs
weight: 30
url: /fr/net/aspose.words.lowcode/converter/converttoimages/
---
## ConvertToImages(*string, [SaveFormat](../../../aspose.words/saveformat/)*) {#converttoimages_5}

Convertit les pages du fichier d'entrée spécifié en images au format spécifié et renvoie un tableau de flux contenant les images.

```csharp
public static Stream[] ConvertToImages(string inputFile, SaveFormat saveFormat)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFile | String | Le nom du fichier d'entrée. |
| saveFormat | SaveFormat | Format d'enregistrement. Seuls les formats d'enregistrement d'image sont autorisés. |

### Return_Value

Renvoie un tableau de flux d'images. Ces flux doivent être supprimés par l'utilisateur final.

## Exemples

Montre comment convertir un document en flux d'images.

```csharp
string doc = MyDir + "Big document.docx";

Stream[] streams = Converter.ConvertToImages(doc, SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(doc, imageSaveOptions);

streams = Converter.ConvertToImages(new Document(doc), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(doc), imageSaveOptions);
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## ConvertToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_6}

Convertit les pages du fichier d'entrée spécifié en images à l'aide des options d'enregistrement spécifiées et renvoie un tableau de flux contenant les images.

```csharp
public static Stream[] ConvertToImages(string inputFile, ImageSaveOptions saveOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFile | String | Le nom du fichier d'entrée. |
| saveOptions | ImageSaveOptions | Options d'enregistrement d'image. |

### Return_Value

Renvoie un tableau de flux d'images. Ces flux doivent être supprimés par l'utilisateur final.

## Exemples

Montre comment convertir un document en flux d'images.

```csharp
string doc = MyDir + "Big document.docx";

Stream[] streams = Converter.ConvertToImages(doc, SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(doc, imageSaveOptions);

streams = Converter.ConvertToImages(new Document(doc), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(doc), imageSaveOptions);
```

### Voir également

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## ConvertToImages(*Stream, [SaveFormat](../../../aspose.words/saveformat/)*) {#converttoimages_3}

Convertit les pages du flux d'entrée spécifié en images au format spécifié et renvoie un tableau de flux contenant les images.

```csharp
public static Stream[] ConvertToImages(Stream inputStream, SaveFormat saveFormat)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux d'entrée. |
| saveFormat | SaveFormat | Format d'enregistrement. Seuls les formats d'enregistrement d'image sont autorisés. |

### Return_Value

Renvoie un tableau de flux d'images. Ces flux doivent être supprimés par l'utilisateur final.

## Exemples

Montre comment convertir un document en images à partir d'un flux.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] streams = Converter.ConvertToImages(streamIn, SaveFormat.Jpeg);

    ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
    imageSaveOptions.PageSet = new PageSet(1);
    streams = Converter.ConvertToImages(streamIn, imageSaveOptions);

    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = false };
    Converter.ConvertToImages(streamIn, loadOptions, imageSaveOptions);
}
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## ConvertToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_4}

Convertit les pages du flux d'entrée spécifié en images à l'aide des options d'enregistrement spécifiées et renvoie un tableau de flux contenant les images.

```csharp
public static Stream[] ConvertToImages(Stream inputStream, ImageSaveOptions saveOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux d'entrée. |
| saveOptions | ImageSaveOptions | Options d'enregistrement d'image. |

### Return_Value

Renvoie un tableau de flux d'images. Ces flux doivent être supprimés par l'utilisateur final.

## Exemples

Montre comment convertir un document en images à partir d'un flux.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] streams = Converter.ConvertToImages(streamIn, SaveFormat.Jpeg);

    ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
    imageSaveOptions.PageSet = new PageSet(1);
    streams = Converter.ConvertToImages(streamIn, imageSaveOptions);

    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = false };
    Converter.ConvertToImages(streamIn, loadOptions, imageSaveOptions);
}
```

### Voir également

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## ConvertToImages(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/), [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_2}

Convertit les pages du flux d'entrée spécifié en images à l'aide des options de chargement et d'enregistrement fournies et renvoie un tableau de flux contenant les images.

```csharp
public static Stream[] ConvertToImages(Stream inputStream, LoadOptions loadOptions, 
    ImageSaveOptions saveOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux d'entrée. |
| loadOptions | LoadOptions | Les options de chargement du document d'entrée. |
| saveOptions | ImageSaveOptions | Options d'enregistrement d'image. |

### Return_Value

Renvoie un tableau de flux d'images. Ces flux doivent être supprimés par l'utilisateur final.

## Exemples

Montre comment convertir un document en images à partir d'un flux.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] streams = Converter.ConvertToImages(streamIn, SaveFormat.Jpeg);

    ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
    imageSaveOptions.PageSet = new PageSet(1);
    streams = Converter.ConvertToImages(streamIn, imageSaveOptions);

    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = false };
    Converter.ConvertToImages(streamIn, loadOptions, imageSaveOptions);
}
```

### Voir également

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## ConvertToImages(*[Document](../../../aspose.words/document/), [SaveFormat](../../../aspose.words/saveformat/)*) {#converttoimages}

Convertit les pages du document spécifié en images au format spécifié et renvoie un tableau de flux contenant les images.

```csharp
public static Stream[] ConvertToImages(Document doc, SaveFormat saveFormat)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| doc | Document | Le document d'entrée. |
| saveFormat | SaveFormat | Format d'enregistrement. Seuls les formats d'enregistrement d'image sont autorisés. |

### Return_Value

Renvoie un tableau de flux d'images. Ces flux doivent être supprimés par l'utilisateur final.

## Exemples

Montre comment convertir un document en flux d'images.

```csharp
string doc = MyDir + "Big document.docx";

Stream[] streams = Converter.ConvertToImages(doc, SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(doc, imageSaveOptions);

streams = Converter.ConvertToImages(new Document(doc), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(doc), imageSaveOptions);
```

### Voir également

* class [Document](../../../aspose.words/document/)
* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## ConvertToImages(*[Document](../../../aspose.words/document/), [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_1}

Convertit les pages du document spécifié en images à l'aide des options d'enregistrement spécifiées et renvoie un tableau de flux contenant les images.

```csharp
public static Stream[] ConvertToImages(Document doc, ImageSaveOptions saveOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| doc | Document | Le document d'entrée. |
| saveOptions | ImageSaveOptions | Options d'enregistrement d'image. |

### Return_Value

Renvoie un tableau de flux d'images. Ces flux doivent être supprimés par l'utilisateur final.

## Exemples

Montre comment convertir un document en flux d'images.

```csharp
string doc = MyDir + "Big document.docx";

Stream[] streams = Converter.ConvertToImages(doc, SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(doc, imageSaveOptions);

streams = Converter.ConvertToImages(new Document(doc), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(doc), imageSaveOptions);
```

### Voir également

* class [Document](../../../aspose.words/document/)
* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)
