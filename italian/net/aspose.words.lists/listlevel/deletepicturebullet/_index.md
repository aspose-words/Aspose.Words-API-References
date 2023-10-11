---
title: ListLevel.DeletePictureBullet
second_title: Aspose.Words per .NET API Reference
description: ListLevel metodo. Elimina limmagine puntata per il livello di elenco corrente.
type: docs
weight: 160
url: /it/net/aspose.words.lists/listlevel/deletepicturebullet/
---
## ListLevel.DeletePictureBullet method

Elimina l'immagine puntata per il livello di elenco corrente.

```csharp
public void DeletePictureBullet()
```

### Osservazioni

Il punto elenco predefinito verrà visualizzato dopo l'eliminazione.

### Esempi

Mostra come impostare un'icona immagine personalizzata per le etichette degli elementi dell'elenco.

```csharp
Document doc = new Document();

List list = doc.Lists.Add(ListTemplate.BulletCircle);

// Crea un punto elenco immagine per il livello di elenco corrente e imposta un'immagine da un file system locale
// come icona che verrà visualizzata dai punti elenco per questo livello di elenco.
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
* spazio dei nomi [Aspose.Words.Lists](../../listlevel/)
* assemblea [Aspose.Words](../../../)


