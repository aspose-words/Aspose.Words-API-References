---
title: ListLevel.DeletePictureBullet
linktitle: DeletePictureBullet
articleTitle: DeletePictureBullet
second_title: Aspose.Words per .NET
description: Rimuovi facilmente i punti elenco immagine dal tuo livello di elenco attuale con il metodo ListLevel DeletePictureBullet. Semplifica la formattazione dei tuoi documenti oggi stesso!
type: docs
weight: 160
url: /it/net/aspose.words.lists/listlevel/deletepicturebullet/
---
## ListLevel.DeletePictureBullet method

Elimina il punto elenco dell'immagine per il livello di elenco corrente.

```csharp
public void DeletePictureBullet()
```

## Osservazioni

Dopo l'eliminazione verrà visualizzato il punto elenco predefinito.

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
