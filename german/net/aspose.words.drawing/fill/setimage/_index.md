---
title: Fill.SetImage
linktitle: SetImage
articleTitle: SetImage
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihr Design mit der SetImage-Methode. Wechseln Sie einfach zu einem einzelnen Bildfülltyp für beeindruckende Visualisierungen und nahtlose Integration.
type: docs
weight: 250
url: /de/net/aspose.words.drawing/fill/setimage/
---
## SetImage(*string*) {#setimage_2}

Ändert den Fülltyp in Einzelbild.

```csharp
public void SetImage(string fileName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Der Pfad zur Bilddatei. |

## Beispiele

Zeigt, wie der Formfülltyp auf Bild eingestellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Es gibt mehrere Möglichkeiten, das Bild einzustellen.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// 1 – Verwenden eines lokalen Systemdateinamens:
shape.Fill.SetImage(ImageDir + "Logo.jpg");
doc.Save(ArtifactsDir + "Shape.FillImage.FileName.docx");

// 2 - Laden Sie eine Datei in ein Byte-Array:
shape.Fill.SetImage(File.ReadAllBytes(ImageDir + "Logo.jpg"));
doc.Save(ArtifactsDir + "Shape.FillImage.ByteArray.docx");

// 3 - Aus einem Stream:
using (FileStream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
    shape.Fill.SetImage(stream);
doc.Save(ArtifactsDir + "Shape.FillImage.Stream.docx");
```

### Siehe auch

* class [Fill](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)

---

## SetImage(*Stream*) {#setimage_1}

Ändert den Fülltyp in Einzelbild.

```csharp
public void SetImage(Stream stream)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | Stream | Der Stream, der die Bildbytes enthält. |

## Beispiele

Zeigt, wie der Formfülltyp auf Bild eingestellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Es gibt mehrere Möglichkeiten, das Bild einzustellen.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// 1 – Verwenden eines lokalen Systemdateinamens:
shape.Fill.SetImage(ImageDir + "Logo.jpg");
doc.Save(ArtifactsDir + "Shape.FillImage.FileName.docx");

// 2 - Laden Sie eine Datei in ein Byte-Array:
shape.Fill.SetImage(File.ReadAllBytes(ImageDir + "Logo.jpg"));
doc.Save(ArtifactsDir + "Shape.FillImage.ByteArray.docx");

// 3 - Aus einem Stream:
using (FileStream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
    shape.Fill.SetImage(stream);
doc.Save(ArtifactsDir + "Shape.FillImage.Stream.docx");
```

### Siehe auch

* class [Fill](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)

---

## SetImage(*byte[]*) {#setimage}

Ändert den Fülltyp in Einzelbild.

```csharp
public void SetImage(byte[] imageBytes)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| imageBytes | Byte[] | Das Bildbyte-Array. |

## Beispiele

Zeigt, wie der Formfülltyp auf Bild eingestellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Es gibt mehrere Möglichkeiten, das Bild einzustellen.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// 1 – Verwenden eines lokalen Systemdateinamens:
shape.Fill.SetImage(ImageDir + "Logo.jpg");
doc.Save(ArtifactsDir + "Shape.FillImage.FileName.docx");

// 2 - Laden Sie eine Datei in ein Byte-Array:
shape.Fill.SetImage(File.ReadAllBytes(ImageDir + "Logo.jpg"));
doc.Save(ArtifactsDir + "Shape.FillImage.ByteArray.docx");

// 3 - Aus einem Stream:
using (FileStream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
    shape.Fill.SetImage(stream);
doc.Save(ArtifactsDir + "Shape.FillImage.Stream.docx");
```

### Siehe auch

* class [Fill](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
