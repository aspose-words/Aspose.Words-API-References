---
title: DocumentBuilder.InsertOnlineVideo
linktitle: InsertOnlineVideo
articleTitle: InsertOnlineVideo
second_title: Aspose.Words pour .NET
description: DocumentBuilder InsertOnlineVideo méthode. Insère un objet vidéo en ligne dans le document et le redimensionne à la taille spécifiée en C#.
type: docs
weight: 410
url: /fr/net/aspose.words/documentbuilder/insertonlinevideo/
---
## InsertOnlineVideo(*string, double, double*) {#insertonlinevideo_1}

Insère un objet vidéo en ligne dans le document et le redimensionne à la taille spécifiée.

```csharp
public Shape InsertOnlineVideo(string videoUrl, double width, double height)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| videoUrl | String | L'URL de la vidéo. |
| width | Double | La largeur de l'image en points. Peut être une valeur négative ou nulle pour demander une échelle de 100 %. |
| height | Double | La hauteur de l'image en points. Peut être une valeur négative ou nulle pour demander une échelle de 100 %. |

### Return_Value

Le nœud d'image qui vient d'être inséré.

## Remarques

Vous pouvez modifier la taille de l'image, l'emplacement, la méthode de positionnement et d'autres paramètres à l'aide du [`Shape`](../../../aspose.words.drawing/shape/) objet renvoyé par cette méthode.

L'insertion de vidéos en ligne à partir des ressources suivantes est prise en charge :

* https://www.youtube.com/
* https://vimeo.com/

Si votre vidéo en ligne ne s'affiche pas correctement, utilisez`InsertOnlineVideo`, qui accepte le code HTML intégré personnalisé.

Le code d'intégration de la vidéo peut varier selon les fournisseurs, consultez le fournisseur correspondant de votre choix pour plus de détails.

## Exemples

Montre comment insérer une vidéo en ligne dans un document à l'aide d'une URL.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOnlineVideo("https://youtu.be/t_1LYZ102RA", 360, 270);

// On peut regarder la vidéo depuis Microsoft Word en cliquant sur la forme.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertVideoWithUrl.docx");
```

### Voir également

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## InsertOnlineVideo(*string, [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertonlinevideo}

Insère un objet vidéo en ligne dans le document et le redimensionne à la taille spécifiée.

```csharp
public Shape InsertOnlineVideo(string videoUrl, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| videoUrl | String | L'URL de la vidéo. |
| horzPos | RelativeHorizontalPosition | Spécifie l'endroit à partir duquel la distance jusqu'à l'image est mesurée. |
| left | Double | Distance en points depuis l'origine jusqu'au côté gauche de l'image. |
| vertPos | RelativeVerticalPosition | Spécifie l'endroit à partir duquel la distance jusqu'à l'image est mesurée. |
| top | Double | Distance en points depuis l'origine jusqu'au haut de l'image. |
| width | Double | La largeur de l'image en points. Peut être une valeur négative ou nulle pour demander une échelle de 100 %. |
| height | Double | La hauteur de l'image en points. Peut être une valeur négative ou nulle pour demander une échelle de 100 %. |
| wrapType | WrapType | Spécifie comment enrouler le texte autour de l'image. |

### Return_Value

Le nœud d'image qui vient d'être inséré.

## Remarques

Vous pouvez modifier la taille de l'image, l'emplacement, la méthode de positionnement et d'autres paramètres à l'aide du [`Shape`](../../../aspose.words.drawing/shape/) objet renvoyé par cette méthode.

L'insertion de vidéos en ligne à partir des ressources suivantes est prise en charge :

* https://www.youtube.com/
* https://vimeo.com/

Si votre vidéo en ligne ne s'affiche pas correctement, utilisez`InsertOnlineVideo`, qui accepte le code HTML intégré personnalisé.

Le code d'intégration de la vidéo peut varier selon les fournisseurs, consultez le fournisseur correspondant de votre choix pour plus de détails.

## Exemples

Montre comment insérer une vidéo en ligne dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838" ;

// Insère une forme qui lit une vidéo du Web lorsque vous cliquez dessus dans Microsoft Word.
// Cette forme rectangulaire contiendra une image basée sur la première image de la vidéo liée
// et une invite visuelle "bouton de lecture". La vidéo a un rapport hauteur/largeur de 16:9.
// Nous définirons la taille de la forme sur ce rapport, afin que l'image n'apparaisse pas étirée.
builder.InsertOnlineVideo(videoUrl, RelativeHorizontalPosition.LeftMargin, 0,
    RelativeVerticalPosition.TopMargin, 0, 320, 180, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOnlineVideo.docx");
```

### Voir également

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## InsertOnlineVideo(*string, string, byte[], double, double*) {#insertonlinevideo_3}

Insère un objet vidéo en ligne dans le document et le redimensionne à la taille spécifiée.

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    double width, double height)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| videoUrl | String | L'URL de la vidéo. |
| videoEmbedCode | String | Le code d'intégration de la vidéo. |
| thumbnailImageBytes | Byte[] | Octets de l’image miniature. |
| width | Double | La largeur de l'image en points. Peut être une valeur négative ou nulle pour demander une échelle de 100 %. |
| height | Double | La hauteur de l'image en points. Peut être une valeur négative ou nulle pour demander une échelle de 100 %. |

### Return_Value

Le nœud d'image qui vient d'être inséré.

## Remarques

Vous pouvez modifier la taille de l'image, l'emplacement, la méthode de positionnement et d'autres paramètres à l'aide du [`Shape`](../../../aspose.words.drawing/shape/) objet renvoyé par cette méthode.

## Exemples

Montre comment insérer une vidéo en ligne dans un document avec une vignette personnalisée.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838" ;
string videoEmbedCode =
    "<iframe src=\"https://player.vimeo.com/video/52477838\" width=\"640\" height=\"360\" frameborder=\"0\" " +
    "title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

byte[] thumbnailImageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(thumbnailImageBytes))
{
    using (Image image = Image.FromStream(stream))
    {
        // Vous trouverez ci-dessous deux manières de créer une forme avec une vignette personnalisée, qui renvoie vers une vidéo en ligne
        // qui sera joué lorsque nous cliquons sur la forme dans Microsoft Word.
        // 1 - Insérez une forme en ligne au niveau du curseur d'insertion du nœud du générateur :
        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image.Width, image.Height);

        builder.InsertBreak(BreakType.PageBreak);

        // 2 - Insérer une forme flottante :
        double left = builder.PageSetup.RightMargin - image.Width;
        double top = builder.PageSetup.BottomMargin - image.Height;

        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes,
            RelativeHorizontalPosition.RightMargin, left, RelativeVerticalPosition.BottomMargin, top,
            image.Width, image.Height, WrapType.Square);
    }
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

### Voir également

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## InsertOnlineVideo(*string, string, byte[], [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertonlinevideo_2}

Insère un objet vidéo en ligne dans le document et le redimensionne à la taille spécifiée.

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    RelativeHorizontalPosition horzPos, double left, RelativeVerticalPosition vertPos, double top, 
    double width, double height, WrapType wrapType)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| videoUrl | String | L'URL de la vidéo. |
| videoEmbedCode | String | Le code d'intégration de la vidéo. |
| thumbnailImageBytes | Byte[] | Octets de l’image miniature. |
| horzPos | RelativeHorizontalPosition | Spécifie l'endroit à partir duquel la distance jusqu'à l'image est mesurée. |
| left | Double | Distance en points depuis l'origine jusqu'au côté gauche de l'image. |
| vertPos | RelativeVerticalPosition | Spécifie l'endroit à partir duquel la distance jusqu'à l'image est mesurée. |
| top | Double | Distance en points depuis l'origine jusqu'au haut de l'image. |
| width | Double | La largeur de l'image en points. Peut être une valeur négative ou nulle pour demander une échelle de 100 %. |
| height | Double | La hauteur de l'image en points. Peut être une valeur négative ou nulle pour demander une échelle de 100 %. |
| wrapType | WrapType | Spécifie comment enrouler le texte autour de l'image. |

### Return_Value

Le nœud d'image qui vient d'être inséré.

## Remarques

Vous pouvez modifier la taille de l'image, l'emplacement, la méthode de positionnement et d'autres paramètres à l'aide du [`Shape`](../../../aspose.words.drawing/shape/) objet renvoyé par cette méthode.

## Exemples

Montre comment insérer une vidéo en ligne dans un document avec une vignette personnalisée.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838" ;
string videoEmbedCode =
    "<iframe src=\"https://player.vimeo.com/video/52477838\" width=\"640\" height=\"360\" frameborder=\"0\" " +
    "title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

byte[] thumbnailImageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(thumbnailImageBytes))
{
    using (Image image = Image.FromStream(stream))
    {
        // Vous trouverez ci-dessous deux manières de créer une forme avec une vignette personnalisée, qui renvoie vers une vidéo en ligne
        // qui sera joué lorsque nous cliquons sur la forme dans Microsoft Word.
        // 1 - Insérez une forme en ligne au niveau du curseur d'insertion du nœud du générateur :
        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image.Width, image.Height);

        builder.InsertBreak(BreakType.PageBreak);

        // 2 - Insérer une forme flottante :
        double left = builder.PageSetup.RightMargin - image.Width;
        double top = builder.PageSetup.BottomMargin - image.Height;

        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes,
            RelativeHorizontalPosition.RightMargin, left, RelativeVerticalPosition.BottomMargin, top,
            image.Width, image.Height, WrapType.Square);
    }
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

### Voir également

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
