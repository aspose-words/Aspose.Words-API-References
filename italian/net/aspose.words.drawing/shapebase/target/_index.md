---
title: ShapeBase.Target
linktitle: Target
articleTitle: Target
second_title: Aspose.Words per .NET
description: Scopri la proprietà ShapeBase Target per impostare o recuperare facilmente i frame di destinazione dei collegamenti ipertestuali per le tue forme, migliorando la navigazione e l'esperienza dell'utente.
type: docs
weight: 560
url: /it/net/aspose.words.drawing/shapebase/target/
---
## ShapeBase.Target property

Ottiene o imposta il frame di destinazione per il collegamento ipertestuale della forma.

```csharp
public string Target { get; set; }
```

## Osservazioni

Il valore predefinito è una stringa vuota.

## Esempi

Mostra come inserire una forma che contiene un'immagine e che è anche un collegamento ipertestuale.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.HRef = "https://forum.aspose.com/";
shape.Target = "New Window";
shape.ScreenTip = "Aspose.Words Support Forums";

// Facendo clic con il tasto sinistro del mouse sulla forma in Microsoft Word si aprirà una nuova finestra del browser Web
// e ci porta al collegamento ipertestuale nella proprietà "HRef".
doc.Save(ArtifactsDir + "Image.InsertImageWithHyperlink.docx");
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
