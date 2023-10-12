---
title: DocSaveOptions.SavePictureBullet
second_title: Aspose.Words per .NET API Reference
description: DocSaveOptions proprietà. Quandofalso  i dati PictureBullet non vengono salvati nel documento di output. Il valore predefinito èVERO .
type: docs
weight: 50
url: /it/net/aspose.words.saving/docsaveoptions/savepicturebullet/
---
## DocSaveOptions.SavePictureBullet property

Quando`falso` , i dati PictureBullet non vengono salvati nel documento di output. Il valore predefinito è`VERO` .

```csharp
public bool SavePictureBullet { get; set; }
```

### Osservazioni

Questa opzione viene fornita per Word 97, che non può funzionare correttamente con i dati PictureBullet. Per rimuovere i dati PictureBullet, imposta l'opzione su "false".

### Esempi

Mostra come omettere i dati PictureBullet dal documento durante il salvataggio.

```csharp
Document doc = new Document(MyDir + "Image bullet points.docx");
// Alcuni elaboratori di testo, come Microsoft Word 97, non sono compatibili con i dati PictureBullet.
// Impostando un flag nell'oggetto SaveOptions,
// possiamo convertire tutti i punti elenco delle immagini in punti elenco ordinari durante il salvataggio.
DocSaveOptions saveOptions = new DocSaveOptions(SaveFormat.Doc);
saveOptions.SavePictureBullet = false;

doc.Save(ArtifactsDir + "DocSaveOptions.PictureBullets.doc", saveOptions);
```

### Guarda anche

* class [DocSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../docsaveoptions/)
* assemblea [Aspose.Words](../../../)


