---
title: Fill.SetImage
second_title: Référence de l'API Aspose.Words pour .NET
description: Fill méthode. Modifie le type de remplissage en image unique.
type: docs
weight: 250
url: /fr/net/aspose.words.drawing/fill/setimage/
---
## SetImage(string) {#setimage_2}

Modifie le type de remplissage en image unique.

```csharp
public void SetImage(string fileName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | Le chemin d'accès au fichier image. |

### Exemples

Montre comment définir le type de remplissage de forme comme image.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Il existe plusieurs façons de définir une image.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// 1 - Utilisation d'un nom de fichier système local :
shape.Fill.SetImage(ImageDir + "Logo.jpg");
doc.Save(ArtifactsDir + "Shape.FillImage.FileName.docx");

// 2 - Charge un fichier dans un tableau d'octets :
shape.Fill.SetImage(File.ReadAllBytes(ImageDir + "Logo.jpg"));
doc.Save(ArtifactsDir + "Shape.FillImage.ByteArray.docx");

// 3 - Depuis un flux :
using (FileStream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
    shape.Fill.SetImage(stream);
doc.Save(ArtifactsDir + "Shape.FillImage.Stream.docx");
```

### Voir également

* class [Fill](../)
* espace de noms [Aspose.Words.Drawing](../../fill/)
* Assemblée [Aspose.Words](../../../)

---

## SetImage(Stream) {#setimage_1}

Modifie le type de remplissage en image unique.

```csharp
public void SetImage(Stream stream)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| stream | Stream | Le flux qui contient les octets de l'image. |

### Voir également

* class [Fill](../)
* espace de noms [Aspose.Words.Drawing](../../fill/)
* Assemblée [Aspose.Words](../../../)

---

## SetImage(byte[]) {#setimage}

Modifie le type de remplissage en image unique.

```csharp
public void SetImage(byte[] imageBytes)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| imageBytes | Byte[] | Le tableau d’octets de l’image. |

### Voir également

* class [Fill](../)
* espace de noms [Aspose.Words.Drawing](../../fill/)
* Assemblée [Aspose.Words](../../../)


