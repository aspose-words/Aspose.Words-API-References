---
title: ListLevel.CreatePictureBullet
linktitle: CreatePictureBullet
articleTitle: CreatePictureBullet
second_title: Aspose.Words per .NET
description: Scopri il metodo CreatePictureBullet di ListLevel per migliorare senza sforzo i tuoi elenchi con punti elenco personalizzati, aggiungendo chiarezza e appeal visivo.
type: docs
weight: 150
url: /it/net/aspose.words.lists/listlevel/createpicturebullet/
---
## ListLevel.CreatePictureBullet method

Crea la forma di un punto elenco per il livello di elenco corrente.

```csharp
public void CreatePictureBullet()
```

## Osservazioni

Notare che,[`NumberStyle`](../numberstyle/) sarà impostato suBullet e [`NumberFormat`](../numberformat/) su "\xF0B7" per visualizzare correttamente il punto elenco dell'immagine. L'immagine della croce rossa verrà impostata come punto elenco dell'immagine al momento della creazione. Per modificarla, utilizzare[`ImageData`](../imagedata/).

## Esempi

Mostra come impostare un'icona immagine personalizzata per le etichette delle voci di elenco.

```csharp
Document doc = new Document();

List list = doc.Lists.Add(ListTemplate.BulletCircle);

// Crea un punto elenco immagine per il livello di elenco corrente e imposta un'immagine da un file system locale
// come l'icona che verrà visualizzata dai punti elenco per questo livello di elenco.
list.ListLevels[0].CreatePictureBullet();
list.ListLevels[0].ImageData.SetImage(ImageDir + "Logo icon.ico");

Assert.IsTrue(list.ListLevels[0].ImageData.HasImage);

DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = list;
builder.Writeln("Hello world!");
builder.Write("Hello again!");

doc.Save(ArtifactsDir + "Lists.CreatePictureBullet.docx");

list.ListLevels[0].DeletePictureBullet();

Assert.IsNull(list.ListLevels[0].ImageData);
```

### Guarda anche

* class [ListLevel](../)
* spazio dei nomi [Aspose.Words.Lists](../../../aspose.words.lists/)
* assemblea [Aspose.Words](../../../)
