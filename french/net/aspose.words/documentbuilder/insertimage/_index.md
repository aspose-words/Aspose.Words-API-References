---
title: DocumentBuilder.InsertImage
second_title: Référence de l'API Aspose.Words pour .NET
description: DocumentBuilder méthode. Insère une image à partir dun .NETImage objet dans le document. Limage est insérée en ligne et à léchelle 100 .
type: docs
weight: 350
url: /fr/net/aspose.words/documentbuilder/insertimage/
---
## InsertImage(Image) {#insertimage_3}

Insère une image à partir d'un .NETImage objet dans le document. L'image est insérée en ligne et à l'échelle 100 %.

```csharp
public Shape InsertImage(Image image)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| image | Image | Image à insérer dans le document. |

### Return_Value

Le nœud d'image qui vient d'être inséré.

### Remarques

Vous pouvez modifier la taille de l'image, l'emplacement, la méthode de positionnement et d'autres paramètres à l'aide du [`Shape`](../../../aspose.words.drawing/shape/) objet renvoyé par cette méthode.

### Exemples

Montre comment insérer une image à partir d'un objet dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

// Vous trouverez ci-dessous trois manières d'insérer une image à partir d'une instance d'objet Image.
// 1 - Forme en ligne avec une taille par défaut basée sur les dimensions d'origine de l'image :
builder.InsertImage(image);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Forme en ligne avec des dimensions personnalisées :
builder.InsertImage(image, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Forme flottante aux dimensions personnalisées :
builder.InsertImage(image, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

### Voir également

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)

---

## InsertImage(string) {#insertimage_9}

Insère une image à partir d'un fichier ou d'une URL dans le document. L'image est insérée en ligne et à l'échelle 100 %.

```csharp
public Shape InsertImage(string fileName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | Le fichier avec l'image. Il peut s'agir de n'importe quel URI local ou distant valide. |

### Return_Value

Le nœud d'image qui vient d'être inséré.

### Remarques

Cette surcharge téléchargera automatiquement l'image avant de l'insérer dans le document si vous spécifiez un URI distant.

Vous pouvez modifier la taille de l'image, l'emplacement, la méthode de positionnement et d'autres paramètres à l'aide du [`Shape`](../../../aspose.words.drawing/shape/) objet renvoyé par cette méthode.

### Exemples

Montre comment insérer une image gif dans le document.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Nous pouvons insérer une image gif en utilisant un chemin ou un tableau d'octets.
// Cela ne fonctionne que si DocumentBuilder est optimisé pour Word version 2010 ou supérieure.
// Notez que l'accès aux octets de l'image provoque la conversion de Gif en Png.
Shape gifImage = builder.InsertImage(ImageDir + "Graphics Interchange Format.gif");

gifImage = builder.InsertImage(File.ReadAllBytes(ImageDir + "Graphics Interchange Format.gif"));

builder.Document.Save(ArtifactsDir + "InsertGif.docx");
```

Montre comment insérer une forme avec une image dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vous trouverez ci-dessous deux emplacements où la méthode "InsertShape" du générateur de documents
// peut générer l'image que la forme affichera.
// 1 - Passez un nom de fichier de système de fichiers local d'un fichier image :
builder.Write("Image from local file: ");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.Writeln();

// 2 - Passez une URL qui pointe vers une image.
builder.Write("Image from a URL: ");
builder.InsertImage(ImageUrl);
builder.Writeln();

doc.Save(ArtifactsDir + "Image.FromUrl.docx");
```

Montre comment insérer une image flottante au centre d'une page.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère une image flottante qui apparaîtra derrière le texte superposé et l'aligne au centre de la page.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

Montre comment déterminer quelle image sera insérée.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Scalable Vector Graphics.svg");

// Aspose.Words insère une image SVG dans le document au format PNG avec l'extension svgBlip
// qui contient la représentation originale de l'image SVG vectorielle.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.SvgWithSvgBlip.docx");

// Aspose.Words insère une image SVG dans le document au format PNG, tout comme Microsoft Word le fait pour l'ancien format.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.Svg.doc");

doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);

// Aspose.Words insère une image SVG dans le document en tant que métafichier EMF pour conserver l'image en représentation vectorielle.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.Emf.docx");
```

Montre comment insérer une image du système de fichiers local dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vous trouverez ci-dessous trois manières d'insérer une image à partir d'un nom de fichier système local.
// 1 - Forme en ligne avec une taille par défaut basée sur les dimensions d'origine de l'image :
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - Forme en ligne avec des dimensions personnalisées :
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Forme flottante aux dimensions personnalisées :
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### Voir également

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)

---

## InsertImage(Stream) {#insertimage_6}

Insère une image d'un flux dans le document. L'image est insérée en ligne et à l'échelle 100 %.

```csharp
public Shape InsertImage(Stream stream)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| stream | Stream | Le flux qui contient l'image. |

### Return_Value

Le nœud d'image qui vient d'être inséré.

### Remarques

Vous pouvez modifier la taille de l'image, l'emplacement, la méthode de positionnement et d'autres paramètres à l'aide du [`Shape`](../../../aspose.words.drawing/shape/) objet renvoyé par cette méthode.

### Exemples

Montre comment insérer une forme avec une image à partir d'un flux dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    builder.Write("Image from stream: ");
    builder.InsertImage(stream);
}

doc.Save(ArtifactsDir + "Image.FromStream.docx");
```

Montre comment insérer une image à partir d'un flux dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // Vous trouverez ci-dessous trois manières d'insérer une image à partir d'un flux.
    // 1 - Forme en ligne avec une taille par défaut basée sur les dimensions d'origine de l'image :
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Forme en ligne avec des dimensions personnalisées :
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Forme flottante aux dimensions personnalisées :
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### Voir également

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)

---

## InsertImage(byte[]) {#insertimage}

Insère une image d'un tableau d'octets dans le document. L'image est insérée en ligne et à l'échelle 100 %.

```csharp
public Shape InsertImage(byte[] imageBytes)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| imageBytes | Byte[] | Le tableau d'octets qui contient l'image. |

### Return_Value

Le nœud d'image qui vient d'être inséré.

### Remarques

Vous pouvez modifier la taille de l'image, l'emplacement, la méthode de positionnement et d'autres paramètres à l'aide du [`Shape`](../../../aspose.words.drawing/shape/) objet renvoyé par cette méthode.

### Exemples

Montre comment insérer une image à partir d'un tableau d'octets dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

using (MemoryStream ms = new MemoryStream())
{
    image.Save(ms, ImageFormat.Png);
    byte[] imageByteArray = ms.ToArray();

    // Vous trouverez ci-dessous trois manières d'insérer une image à partir d'un tableau d'octets.
    // 1 - Forme en ligne avec une taille par défaut basée sur les dimensions d'origine de l'image :
    builder.InsertImage(imageByteArray);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Forme en ligne avec des dimensions personnalisées :
    builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Forme flottante aux dimensions personnalisées :
    builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin, 
    100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

Montre comment insérer une image à partir d'un tableau d'octets dans un document (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Le décodage de l'image la convertira au format .png.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    using (SKImage image = SKImage.FromBitmap(bitmap))
    {
        using (SKData data = image.Encode())
        {
            byte[] imageByteArray = data.ToArray();

            // Vous trouverez ci-dessous trois manières d'insérer une image à partir d'un tableau d'octets.
            // 1 - Forme en ligne avec une taille par défaut basée sur les dimensions d'origine de l'image :
            builder.InsertImage(imageByteArray);

            builder.InsertBreak(BreakType.PageBreak);

            // 2 - Forme en ligne avec des dimensions personnalisées :
            builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

            builder.InsertBreak(BreakType.PageBreak);

            // 3 - Forme flottante aux dimensions personnalisées :
            builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
                100, 200, 100, WrapType.Square);
        }
    }
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArrayNetStandard2.docx");
```

### Voir également

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)

---

## InsertImage(Image, double, double) {#insertimage_5}

Insère une image en ligne à partir d'un .NETImage objet dans le document et le redimensionne à la taille spécifiée.

```csharp
public Shape InsertImage(Image image, double width, double height)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| image | Image | Image à insérer dans le document. |
| width | Double | La largeur de l'image en points. Peut être une valeur négative ou nulle pour demander une échelle de 100 %. |
| height | Double | La hauteur de l'image en points. Peut être une valeur négative ou nulle pour demander une échelle de 100 %. |

### Return_Value

Le nœud d'image qui vient d'être inséré.

### Remarques

Vous pouvez modifier la taille de l'image, l'emplacement, la méthode de positionnement et d'autres paramètres à l'aide du [`Shape`](../../../aspose.words.drawing/shape/) objet renvoyé par cette méthode.

### Exemples

Montre comment insérer une image à partir d'un objet dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

// Vous trouverez ci-dessous trois manières d'insérer une image à partir d'une instance d'objet Image.
// 1 - Forme en ligne avec une taille par défaut basée sur les dimensions d'origine de l'image :
builder.InsertImage(image);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Forme en ligne avec des dimensions personnalisées :
builder.InsertImage(image, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Forme flottante aux dimensions personnalisées :
builder.InsertImage(image, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

Montre comment insérer une image d'un objet dans un document (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Le décodage de l'image la convertira au format .png.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    // Vous trouverez ci-dessous trois manières d'insérer une image à partir d'une instance d'objet Image.
    // 1 - Forme en ligne avec une taille par défaut basée sur les dimensions d'origine de l'image :
    builder.InsertImage(bitmap);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Forme en ligne avec des dimensions personnalisées :
    builder.InsertImage(bitmap, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Forme flottante aux dimensions personnalisées :
    builder.InsertImage(bitmap, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObjectNetStandard2.docx");
```

### Voir également

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)

---

## InsertImage(string, double, double) {#insertimage_11}

Insère une image en ligne à partir d'un fichier ou d'une URL dans le document et la redimensionne à la taille spécifiée.

```csharp
public Shape InsertImage(string fileName, double width, double height)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | Le fichier qui contient l'image. |
| width | Double | La largeur de l'image en points. Peut être une valeur négative ou nulle pour demander une échelle de 100 %. |
| height | Double | La hauteur de l'image en points. Peut être une valeur négative ou nulle pour demander une échelle de 100 %. |

### Return_Value

Le nœud d'image qui vient d'être inséré.

### Remarques

Vous pouvez modifier la taille de l'image, l'emplacement, la méthode de positionnement et d'autres paramètres à l'aide du [`Shape`](../../../aspose.words.drawing/shape/) objet renvoyé par cette méthode.

### Exemples

Montre comment insérer une image du système de fichiers local dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vous trouverez ci-dessous trois manières d'insérer une image à partir d'un nom de fichier système local.
// 1 - Forme en ligne avec une taille par défaut basée sur les dimensions d'origine de l'image :
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - Forme en ligne avec des dimensions personnalisées :
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Forme flottante aux dimensions personnalisées :
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### Voir également

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)

---

## InsertImage(Stream, double, double) {#insertimage_8}

Insère une image en ligne à partir d'un flux dans le document et la redimensionne à la taille spécifiée.

```csharp
public Shape InsertImage(Stream stream, double width, double height)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| stream | Stream | Le flux qui contient l'image. |
| width | Double | La largeur de l'image en points. Peut être une valeur négative ou nulle pour demander une échelle de 100 %. |
| height | Double | La hauteur de l'image en points. Peut être une valeur négative ou nulle pour demander une échelle de 100 %. |

### Return_Value

Le nœud d'image qui vient d'être inséré.

### Remarques

Vous pouvez modifier la taille de l'image, l'emplacement, la méthode de positionnement et d'autres paramètres à l'aide du [`Shape`](../../../aspose.words.drawing/shape/) objet renvoyé par cette méthode.

### Exemples

Montre comment insérer une image à partir d'un flux dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // Vous trouverez ci-dessous trois manières d'insérer une image à partir d'un flux.
    // 1 - Forme en ligne avec une taille par défaut basée sur les dimensions d'origine de l'image :
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Forme en ligne avec des dimensions personnalisées :
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Forme flottante aux dimensions personnalisées :
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### Voir également

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)

---

## InsertImage(byte[], double, double) {#insertimage_2}

Insère une image en ligne à partir d'un tableau d'octets dans le document et la met à l'échelle à la taille spécifiée.

```csharp
public Shape InsertImage(byte[] imageBytes, double width, double height)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| imageBytes | Byte[] | Le tableau d'octets qui contient l'image. |
| width | Double | La largeur de l'image en points. Peut être une valeur négative ou nulle pour demander une échelle de 100 %. |
| height | Double | La hauteur de l'image en points. Peut être une valeur négative ou nulle pour demander une échelle de 100 %. |

### Return_Value

Le nœud d'image qui vient d'être inséré.

### Remarques

Vous pouvez modifier la taille de l'image, l'emplacement, la méthode de positionnement et d'autres paramètres à l'aide du [`Shape`](../../../aspose.words.drawing/shape/) objet renvoyé par cette méthode.

### Exemples

Montre comment insérer une image à partir d'un tableau d'octets dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

using (MemoryStream ms = new MemoryStream())
{
    image.Save(ms, ImageFormat.Png);
    byte[] imageByteArray = ms.ToArray();

    // Vous trouverez ci-dessous trois manières d'insérer une image à partir d'un tableau d'octets.
    // 1 - Forme en ligne avec une taille par défaut basée sur les dimensions d'origine de l'image :
    builder.InsertImage(imageByteArray);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Forme en ligne avec des dimensions personnalisées :
    builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Forme flottante aux dimensions personnalisées :
    builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin, 
    100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

Montre comment insérer une image à partir d'un tableau d'octets dans un document (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Le décodage de l'image la convertira au format .png.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    using (SKImage image = SKImage.FromBitmap(bitmap))
    {
        using (SKData data = image.Encode())
        {
            byte[] imageByteArray = data.ToArray();

            // Vous trouverez ci-dessous trois manières d'insérer une image à partir d'un tableau d'octets.
            // 1 - Forme en ligne avec une taille par défaut basée sur les dimensions d'origine de l'image :
            builder.InsertImage(imageByteArray);

            builder.InsertBreak(BreakType.PageBreak);

            // 2 - Forme en ligne avec des dimensions personnalisées :
            builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

            builder.InsertBreak(BreakType.PageBreak);

            // 3 - Forme flottante aux dimensions personnalisées :
            builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
                100, 200, 100, WrapType.Square);
        }
    }
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArrayNetStandard2.docx");
```

### Voir également

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)

---

## InsertImage(Image, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertimage_4}

Insère une image à partir d'un .NETImage objet à la position et à la taille spécifiées.

```csharp
public Shape InsertImage(Image image, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| image | Image | Image à insérer dans le document. |
| horzPos | RelativeHorizontalPosition | Spécifie l'endroit à partir duquel la distance à l'image est mesurée. |
| left | Double | Distance en points entre l'origine et le côté gauche de l'image. |
| vertPos | RelativeVerticalPosition | Spécifie d'où la distance à l'image est mesurée. |
| top | Double | Distance en points entre l'origine et le haut de l'image. |
| width | Double | La largeur de l'image en points. Peut être une valeur négative ou nulle pour demander une échelle de 100 %. |
| height | Double | La hauteur de l'image en points. Peut être une valeur négative ou nulle pour demander une échelle de 100 %. |
| wrapType | WrapType | Spécifie comment habiller le texte autour de l'image. |

### Return_Value

Le nœud d'image qui vient d'être inséré.

### Remarques

Vous pouvez modifier la taille de l'image, l'emplacement, la méthode de positionnement et d'autres paramètres à l'aide du [`Shape`](../../../aspose.words.drawing/shape/) objet renvoyé par cette méthode.

### Exemples

Montre comment insérer une image à partir d'un objet dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

// Vous trouverez ci-dessous trois manières d'insérer une image à partir d'une instance d'objet Image.
// 1 - Forme en ligne avec une taille par défaut basée sur les dimensions d'origine de l'image :
builder.InsertImage(image);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Forme en ligne avec des dimensions personnalisées :
builder.InsertImage(image, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Forme flottante aux dimensions personnalisées :
builder.InsertImage(image, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

Montre comment insérer une image d'un objet dans un document (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Le décodage de l'image la convertira au format .png.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    // Vous trouverez ci-dessous trois manières d'insérer une image à partir d'une instance d'objet Image.
    // 1 - Forme en ligne avec une taille par défaut basée sur les dimensions d'origine de l'image :
    builder.InsertImage(bitmap);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Forme en ligne avec des dimensions personnalisées :
    builder.InsertImage(bitmap, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Forme flottante aux dimensions personnalisées :
    builder.InsertImage(bitmap, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObjectNetStandard2.docx");
```

### Voir également

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)

---

## InsertImage(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertimage_10}

Insère une image à partir d'un fichier ou d'une URL à la position et à la taille spécifiées.

```csharp
public Shape InsertImage(string fileName, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | Le fichier qui contient l'image. |
| horzPos | RelativeHorizontalPosition | Spécifie l'endroit à partir duquel la distance à l'image est mesurée. |
| left | Double | Distance en points entre l'origine et le côté gauche de l'image. |
| vertPos | RelativeVerticalPosition | Spécifie d'où la distance à l'image est mesurée. |
| top | Double | Distance en points entre l'origine et le haut de l'image. |
| width | Double | La largeur de l'image en points. Peut être une valeur négative ou nulle pour demander une échelle de 100 %. |
| height | Double | La hauteur de l'image en points. Peut être une valeur négative ou nulle pour demander une échelle de 100 %. |
| wrapType | WrapType | Spécifie comment habiller le texte autour de l'image. |

### Return_Value

Le nœud d'image qui vient d'être inséré.

### Remarques

Vous pouvez modifier la taille de l'image, l'emplacement, la méthode de positionnement et d'autres paramètres à l'aide du [`Shape`](../../../aspose.words.drawing/shape/) objet renvoyé par cette méthode.

### Exemples

Montre comment insérer une image.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Il existe deux manières d'utiliser un générateur de document pour sourcer une image, puis de l'insérer en tant que forme flottante.
// 1 - Depuis un fichier du système de fichiers local :
builder.InsertImage(ImageDir + "Transparent background logo.png", RelativeHorizontalPosition.Margin, 100,
    RelativeVerticalPosition.Margin, 0, 200, 200, WrapType.Square);

// 2 - A partir d'une URL :
builder.InsertImage(ImageUrl, RelativeHorizontalPosition.Margin, 100,
    RelativeVerticalPosition.Margin, 250, 200, 200, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFloatingImage.docx");
```

Montre comment insérer une image du système de fichiers local dans un document tout en préservant ses dimensions.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// La méthode InsertImage crée une forme flottante avec l'image transmise dans ses données d'image.
// Nous pouvons spécifier les dimensions de la forme en les passant à cette méthode.
Shape imageShape = builder.InsertImage(ImageDir + "Logo.jpg", RelativeHorizontalPosition.Margin, 0,
    RelativeVerticalPosition.Margin, 0, -1, -1, WrapType.Square);

// Passer des valeurs négatives comme dimensions prévues définira automatiquement
// les dimensions de la forme basées sur les dimensions de son image.
Assert.AreEqual(300.0d, imageShape.Width);
Assert.AreEqual(300.0d, imageShape.Height);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertImageOriginalSize.docx");
```

Montre comment insérer une image du système de fichiers local dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vous trouverez ci-dessous trois manières d'insérer une image à partir d'un nom de fichier système local.
// 1 - Forme en ligne avec une taille par défaut basée sur les dimensions d'origine de l'image :
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - Forme en ligne avec des dimensions personnalisées :
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Forme flottante aux dimensions personnalisées :
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### Voir également

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)

---

## InsertImage(Stream, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertimage_7}

Insère une image à partir d'un flux à la position et à la taille spécifiées.

```csharp
public Shape InsertImage(Stream stream, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| stream | Stream | Le flux qui contient l'image. |
| horzPos | RelativeHorizontalPosition | Spécifie l'endroit à partir duquel la distance à l'image est mesurée. |
| left | Double | Distance en points entre l'origine et le côté gauche de l'image. |
| vertPos | RelativeVerticalPosition | Spécifie d'où la distance à l'image est mesurée. |
| top | Double | Distance en points entre l'origine et le haut de l'image. |
| width | Double | La largeur de l'image en points. Peut être une valeur négative ou nulle pour demander une échelle de 100 %. |
| height | Double | La hauteur de l'image en points. Peut être une valeur négative ou nulle pour demander une échelle de 100 %. |
| wrapType | WrapType | Spécifie comment habiller le texte autour de l'image. |

### Return_Value

Le nœud d'image qui vient d'être inséré.

### Remarques

Vous pouvez modifier la taille de l'image, l'emplacement, la méthode de positionnement et d'autres paramètres à l'aide du [`Shape`](../../../aspose.words.drawing/shape/) objet renvoyé par cette méthode.

### Exemples

Montre comment insérer une image à partir d'un flux dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // Vous trouverez ci-dessous trois manières d'insérer une image à partir d'un flux.
    // 1 - Forme en ligne avec une taille par défaut basée sur les dimensions d'origine de l'image :
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Forme en ligne avec des dimensions personnalisées :
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Forme flottante aux dimensions personnalisées :
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### Voir également

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)

---

## InsertImage(byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertimage_1}

Insère une image à partir d'un tableau d'octets à la position et à la taille spécifiées.

```csharp
public Shape InsertImage(byte[] imageBytes, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| imageBytes | Byte[] | Le tableau d'octets qui contient l'image. |
| horzPos | RelativeHorizontalPosition | Spécifie l'endroit à partir duquel la distance à l'image est mesurée. |
| left | Double | Distance en points entre l'origine et le côté gauche de l'image. |
| vertPos | RelativeVerticalPosition | Spécifie d'où la distance à l'image est mesurée. |
| top | Double | Distance en points entre l'origine et le haut de l'image. |
| width | Double | La largeur de l'image en points. Peut être une valeur négative ou nulle pour demander une échelle de 100 %. |
| height | Double | La hauteur de l'image en points. Peut être une valeur négative ou nulle pour demander une échelle de 100 %. |
| wrapType | WrapType | Spécifie comment habiller le texte autour de l'image. |

### Return_Value

Le nœud d'image qui vient d'être inséré.

### Remarques

Vous pouvez modifier la taille de l'image, l'emplacement, la méthode de positionnement et d'autres paramètres à l'aide du [`Shape`](../../../aspose.words.drawing/shape/) objet renvoyé par cette méthode.

### Exemples

Montre comment insérer une image à partir d'un tableau d'octets dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

using (MemoryStream ms = new MemoryStream())
{
    image.Save(ms, ImageFormat.Png);
    byte[] imageByteArray = ms.ToArray();

    // Vous trouverez ci-dessous trois manières d'insérer une image à partir d'un tableau d'octets.
    // 1 - Forme en ligne avec une taille par défaut basée sur les dimensions d'origine de l'image :
    builder.InsertImage(imageByteArray);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Forme en ligne avec des dimensions personnalisées :
    builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Forme flottante aux dimensions personnalisées :
    builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin, 
    100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

Montre comment insérer une image à partir d'un tableau d'octets dans un document (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Le décodage de l'image la convertira au format .png.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    using (SKImage image = SKImage.FromBitmap(bitmap))
    {
        using (SKData data = image.Encode())
        {
            byte[] imageByteArray = data.ToArray();

            // Vous trouverez ci-dessous trois manières d'insérer une image à partir d'un tableau d'octets.
            // 1 - Forme en ligne avec une taille par défaut basée sur les dimensions d'origine de l'image :
            builder.InsertImage(imageByteArray);

            builder.InsertBreak(BreakType.PageBreak);

            // 2 - Forme en ligne avec des dimensions personnalisées :
            builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

            builder.InsertBreak(BreakType.PageBreak);

            // 3 - Forme flottante aux dimensions personnalisées :
            builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
                100, 200, 100, WrapType.Square);
        }
    }
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArrayNetStandard2.docx");
```

### Voir également

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)


