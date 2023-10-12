---
title: Fill.SetImage
second_title: Referencia de API de Aspose.Words para .NET
description: Fill método. Cambia el tipo de relleno a una sola imagen.
type: docs
weight: 250
url: /es/net/aspose.words.drawing/fill/setimage/
---
## SetImage(string) {#setimage_2}

Cambia el tipo de relleno a una sola imagen.

```csharp
public void SetImage(string fileName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | La ruta al archivo de imagen. |

### Ejemplos

Muestra cómo configurar el tipo de relleno de forma como imagen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Hay varias formas de configurar la imagen.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// 1 - Usando un nombre de archivo del sistema local:
shape.Fill.SetImage(ImageDir + "Logo.jpg");
doc.Save(ArtifactsDir + "Shape.FillImage.FileName.docx");

// 2 - Carga un archivo en una matriz de bytes:
shape.Fill.SetImage(File.ReadAllBytes(ImageDir + "Logo.jpg"));
doc.Save(ArtifactsDir + "Shape.FillImage.ByteArray.docx");

// 3 - Desde una secuencia:
using (FileStream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
    shape.Fill.SetImage(stream);
doc.Save(ArtifactsDir + "Shape.FillImage.Stream.docx");
```

### Ver también

* class [Fill](../)
* espacio de nombres [Aspose.Words.Drawing](../../fill/)
* asamblea [Aspose.Words](../../../)

---

## SetImage(Stream) {#setimage_1}

Cambia el tipo de relleno a una sola imagen.

```csharp
public void SetImage(Stream stream)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| stream | Stream | La secuencia que contiene los bytes de la imagen. |

### Ver también

* class [Fill](../)
* espacio de nombres [Aspose.Words.Drawing](../../fill/)
* asamblea [Aspose.Words](../../../)

---

## SetImage(byte[]) {#setimage}

Cambia el tipo de relleno a una sola imagen.

```csharp
public void SetImage(byte[] imageBytes)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| imageBytes | Byte[] | La matriz de bytes de imagen. |

### Ver también

* class [Fill](../)
* espacio de nombres [Aspose.Words.Drawing](../../fill/)
* asamblea [Aspose.Words](../../../)


