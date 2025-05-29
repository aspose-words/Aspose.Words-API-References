---
title: DocSaveOptions.SavePictureBullet
linktitle: SavePictureBullet
articleTitle: SavePictureBullet
second_title: Aspose.Words per .NET
description: Scopri come la proprietà SavePictureBullet di DocSaveOptions migliora l'output dei tuoi documenti. Gestisci facilmente il salvataggio dei dati PictureBullet per risultati ottimali.
type: docs
weight: 60
url: /it/net/aspose.words.saving/docsaveoptions/savepicturebullet/
---
## DocSaveOptions.SavePictureBullet property

Quando`falso` , i dati PictureBullet non vengono salvati nel documento di output. Il valore predefinito è`VERO` .

```csharp
public bool SavePictureBullet { get; set; }
```

## Osservazioni

Questa opzione è disponibile per Word 97, che non può funzionare correttamente con i dati PictureBullet. Per rimuovere i dati PictureBullet, impostare l'opzione su "false".

## Esempi

Mostra come omettere i dati PictureBullet dal documento durante il salvataggio.

```csharp
Document doc = new Document(MyDir + "Image bullet points.docx");
// Alcuni elaboratori di testi, come Microsoft Word 97, sono incompatibili con i dati PictureBullet.
// Impostando un flag nell'oggetto SaveOptions,
// possiamo convertire tutti i punti elenco delle immagini in punti elenco normali durante il salvataggio.
DocSaveOptions saveOptions = new DocSaveOptions(SaveFormat.Doc);
saveOptions.SavePictureBullet = false;

doc.Save(ArtifactsDir + "DocSaveOptions.PictureBullets.doc", saveOptions);
```

### Guarda anche

* class [DocSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
