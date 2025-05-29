---
title: Fill.SetImage
linktitle: SetImage
articleTitle: SetImage
second_title: Aspose.Words per .NET
description: Migliora il tuo design con il metodo SetImage. Passa facilmente a un singolo tipo di riempimento immagine per ottenere effetti visivi straordinari e un'integrazione perfetta.
type: docs
weight: 250
url: /it/net/aspose.words.drawing/fill/setimage/
---
## SetImage(*string*) {#setimage_2}

Cambia il tipo di riempimento in immagine singola.

```csharp
public void SetImage(string fileName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | Percorso al file immagine. |

## Esempi

Mostra come impostare il tipo di riempimento della forma come immagine.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Esistono diversi modi per impostare l'immagine.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// 1 - Utilizzo di un nome file di sistema locale:
shape.Fill.SetImage(ImageDir + "Logo.jpg");
doc.Save(ArtifactsDir + "Shape.FillImage.FileName.docx");

// 2 - Carica un file in un array di byte:
shape.Fill.SetImage(File.ReadAllBytes(ImageDir + "Logo.jpg"));
doc.Save(ArtifactsDir + "Shape.FillImage.ByteArray.docx");

// 3 - Da un flusso:
using (FileStream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
    shape.Fill.SetImage(stream);
doc.Save(ArtifactsDir + "Shape.FillImage.Stream.docx");
```

### Guarda anche

* class [Fill](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)

---

## SetImage(*Stream*) {#setimage_1}

Cambia il tipo di riempimento in immagine singola.

```csharp
public void SetImage(Stream stream)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| stream | Stream | Il flusso che contiene i byte dell'immagine. |

## Esempi

Mostra come impostare il tipo di riempimento della forma come immagine.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Esistono diversi modi per impostare l'immagine.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// 1 - Utilizzo di un nome file di sistema locale:
shape.Fill.SetImage(ImageDir + "Logo.jpg");
doc.Save(ArtifactsDir + "Shape.FillImage.FileName.docx");

// 2 - Carica un file in un array di byte:
shape.Fill.SetImage(File.ReadAllBytes(ImageDir + "Logo.jpg"));
doc.Save(ArtifactsDir + "Shape.FillImage.ByteArray.docx");

// 3 - Da un flusso:
using (FileStream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
    shape.Fill.SetImage(stream);
doc.Save(ArtifactsDir + "Shape.FillImage.Stream.docx");
```

### Guarda anche

* class [Fill](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)

---

## SetImage(*byte[]*) {#setimage}

Cambia il tipo di riempimento in immagine singola.

```csharp
public void SetImage(byte[] imageBytes)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| imageBytes | Byte[] | Array di byte dell'immagine. |

## Esempi

Mostra come impostare il tipo di riempimento della forma come immagine.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Esistono diversi modi per impostare l'immagine.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// 1 - Utilizzo di un nome file di sistema locale:
shape.Fill.SetImage(ImageDir + "Logo.jpg");
doc.Save(ArtifactsDir + "Shape.FillImage.FileName.docx");

// 2 - Carica un file in un array di byte:
shape.Fill.SetImage(File.ReadAllBytes(ImageDir + "Logo.jpg"));
doc.Save(ArtifactsDir + "Shape.FillImage.ByteArray.docx");

// 3 - Da un flusso:
using (FileStream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
    shape.Fill.SetImage(stream);
doc.Save(ArtifactsDir + "Shape.FillImage.Stream.docx");
```

### Guarda anche

* class [Fill](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
