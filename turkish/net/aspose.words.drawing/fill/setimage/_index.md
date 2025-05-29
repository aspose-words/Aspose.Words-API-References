---
title: Fill.SetImage
linktitle: SetImage
articleTitle: SetImage
second_title: .NET için Aspose.Words
description: SetImage yöntemiyle tasarımınızı geliştirin. Çarpıcı görseller ve kusursuz entegrasyon için tek bir resim dolgu türüne kolayca geçin.
type: docs
weight: 250
url: /tr/net/aspose.words.drawing/fill/setimage/
---
## SetImage(*string*) {#setimage_2}

Dolgu türünü tek görüntüye değiştirir.

```csharp
public void SetImage(string fileName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Resim dosyasının yolu. |

## Örnekler

Şekil dolgu tipinin resim olarak nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Görüntüyü ayarlamanın birkaç yolu vardır.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// 1 - Yerel bir sistem dosya adı kullanarak:
shape.Fill.SetImage(ImageDir + "Logo.jpg");
doc.Save(ArtifactsDir + "Shape.FillImage.FileName.docx");

// 2 - Bir dosyayı bir bayt dizisine yükleyin:
shape.Fill.SetImage(File.ReadAllBytes(ImageDir + "Logo.jpg"));
doc.Save(ArtifactsDir + "Shape.FillImage.ByteArray.docx");

// 3 - Bir akıştan:
using (FileStream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
    shape.Fill.SetImage(stream);
doc.Save(ArtifactsDir + "Shape.FillImage.Stream.docx");
```

### Ayrıca bakınız

* class [Fill](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)

---

## SetImage(*Stream*) {#setimage_1}

Dolgu türünü tek görüntüye değiştirir.

```csharp
public void SetImage(Stream stream)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Resim baytlarını içeren akış. |

## Örnekler

Şekil dolgu tipinin resim olarak nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Görüntüyü ayarlamanın birkaç yolu vardır.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// 1 - Yerel bir sistem dosya adı kullanarak:
shape.Fill.SetImage(ImageDir + "Logo.jpg");
doc.Save(ArtifactsDir + "Shape.FillImage.FileName.docx");

// 2 - Bir dosyayı bir bayt dizisine yükleyin:
shape.Fill.SetImage(File.ReadAllBytes(ImageDir + "Logo.jpg"));
doc.Save(ArtifactsDir + "Shape.FillImage.ByteArray.docx");

// 3 - Bir akıştan:
using (FileStream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
    shape.Fill.SetImage(stream);
doc.Save(ArtifactsDir + "Shape.FillImage.Stream.docx");
```

### Ayrıca bakınız

* class [Fill](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)

---

## SetImage(*byte[]*) {#setimage}

Dolgu türünü tek görüntüye değiştirir.

```csharp
public void SetImage(byte[] imageBytes)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| imageBytes | Byte[] | Görüntü bayt dizisi. |

## Örnekler

Şekil dolgu tipinin resim olarak nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Görüntüyü ayarlamanın birkaç yolu vardır.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// 1 - Yerel bir sistem dosya adı kullanarak:
shape.Fill.SetImage(ImageDir + "Logo.jpg");
doc.Save(ArtifactsDir + "Shape.FillImage.FileName.docx");

// 2 - Bir dosyayı bir bayt dizisine yükleyin:
shape.Fill.SetImage(File.ReadAllBytes(ImageDir + "Logo.jpg"));
doc.Save(ArtifactsDir + "Shape.FillImage.ByteArray.docx");

// 3 - Bir akıştan:
using (FileStream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
    shape.Fill.SetImage(stream);
doc.Save(ArtifactsDir + "Shape.FillImage.Stream.docx");
```

### Ayrıca bakınız

* class [Fill](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
