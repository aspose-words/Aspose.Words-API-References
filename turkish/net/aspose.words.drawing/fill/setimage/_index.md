---
title: Fill.SetImage
second_title: Aspose.Words for .NET API Referansı
description: Fill yöntem. Doldurma türünü tek görüntü olarak değiştirir.
type: docs
weight: 250
url: /tr/net/aspose.words.drawing/fill/setimage/
---
## SetImage(string) {#setimage_2}

Doldurma türünü tek görüntü olarak değiştirir.

```csharp
public void SetImage(string fileName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Resim dosyasının yolu. |

### Örnekler

Şekil dolgu türünün görüntü olarak nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Görüntüyü ayarlamanın birkaç yolu vardır.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// 1 - Yerel sistem dosya adını kullanma:
shape.Fill.SetImage(ImageDir + "Logo.jpg");
doc.Save(ArtifactsDir + "Shape.FillImage.FileName.docx");

// 2 - Bir bayt dizisine bir dosya yükleyin:
shape.Fill.SetImage(File.ReadAllBytes(ImageDir + "Logo.jpg"));
doc.Save(ArtifactsDir + "Shape.FillImage.ByteArray.docx");

// 3 - Bir akıştan:
using (FileStream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
    shape.Fill.SetImage(stream);
doc.Save(ArtifactsDir + "Shape.FillImage.Stream.docx");
```

### Ayrıca bakınız

* class [Fill](../)
* ad alanı [Aspose.Words.Drawing](../../fill/)
* toplantı [Aspose.Words](../../../)

---

## SetImage(Stream) {#setimage_1}

Doldurma türünü tek görüntü olarak değiştirir.

```csharp
public void SetImage(Stream stream)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Görüntü baytlarını içeren akış. |

### Ayrıca bakınız

* class [Fill](../)
* ad alanı [Aspose.Words.Drawing](../../fill/)
* toplantı [Aspose.Words](../../../)

---

## SetImage(byte[]) {#setimage}

Doldurma türünü tek görüntü olarak değiştirir.

```csharp
public void SetImage(byte[] imageBytes)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| imageBytes | Byte[] | Görüntü bayt dizisi. |

### Ayrıca bakınız

* class [Fill](../)
* ad alanı [Aspose.Words.Drawing](../../fill/)
* toplantı [Aspose.Words](../../../)


