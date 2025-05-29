---
title: Fill.SetImage
linktitle: SetImage
articleTitle: SetImage
second_title: Aspose.Words pour .NET
description: Améliorez votre design avec la méthode SetImage. Passez facilement à un type de remplissage d'image unique pour des visuels époustouflants et une intégration fluide.
type: docs
weight: 250
url: /fr/net/aspose.words.drawing/fill/setimage/
---
## SetImage(*string*) {#setimage_2}

Modifie le type de remplissage en image unique.

```csharp
public void SetImage(string fileName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | Le chemin vers le fichier image. |

## Exemples

Montre comment définir le type de remplissage de forme comme image.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Il existe plusieurs façons de définir une image.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// 1 - Utilisation d'un nom de fichier système local :
shape.Fill.SetImage(ImageDir + "Logo.jpg");
doc.Save(ArtifactsDir + "Shape.FillImage.FileName.docx");

// 2 - Charger un fichier dans un tableau d'octets :
shape.Fill.SetImage(File.ReadAllBytes(ImageDir + "Logo.jpg"));
doc.Save(ArtifactsDir + "Shape.FillImage.ByteArray.docx");

// 3 - À partir d'un flux :
using (FileStream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
    shape.Fill.SetImage(stream);
doc.Save(ArtifactsDir + "Shape.FillImage.Stream.docx");
```

### Voir également

* class [Fill](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)

---

## SetImage(*Stream*) {#setimage_1}

Modifie le type de remplissage en image unique.

```csharp
public void SetImage(Stream stream)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| stream | Stream | Le flux qui contient les octets de l'image. |

## Exemples

Montre comment définir le type de remplissage de forme comme image.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Il existe plusieurs façons de définir une image.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// 1 - Utilisation d'un nom de fichier système local :
shape.Fill.SetImage(ImageDir + "Logo.jpg");
doc.Save(ArtifactsDir + "Shape.FillImage.FileName.docx");

// 2 - Charger un fichier dans un tableau d'octets :
shape.Fill.SetImage(File.ReadAllBytes(ImageDir + "Logo.jpg"));
doc.Save(ArtifactsDir + "Shape.FillImage.ByteArray.docx");

// 3 - À partir d'un flux :
using (FileStream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
    shape.Fill.SetImage(stream);
doc.Save(ArtifactsDir + "Shape.FillImage.Stream.docx");
```

### Voir également

* class [Fill](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)

---

## SetImage(*byte[]*) {#setimage}

Modifie le type de remplissage en image unique.

```csharp
public void SetImage(byte[] imageBytes)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| imageBytes | Byte[] | Le tableau d'octets de l'image. |

## Exemples

Montre comment définir le type de remplissage de forme comme image.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Il existe plusieurs façons de définir une image.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// 1 - Utilisation d'un nom de fichier système local :
shape.Fill.SetImage(ImageDir + "Logo.jpg");
doc.Save(ArtifactsDir + "Shape.FillImage.FileName.docx");

// 2 - Charger un fichier dans un tableau d'octets :
shape.Fill.SetImage(File.ReadAllBytes(ImageDir + "Logo.jpg"));
doc.Save(ArtifactsDir + "Shape.FillImage.ByteArray.docx");

// 3 - À partir d'un flux :
using (FileStream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
    shape.Fill.SetImage(stream);
doc.Save(ArtifactsDir + "Shape.FillImage.Stream.docx");
```

### Voir également

* class [Fill](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
