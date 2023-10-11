---
title: ShapeBase.HRef
second_title: Aspose.Words per .NET API Reference
description: ShapeBase proprietà. Ottiene o imposta lindirizzo completo del collegamento ipertestuale per una forma.
type: docs
weight: 230
url: /it/net/aspose.words.drawing/shapebase/href/
---
## ShapeBase.HRef property

Ottiene o imposta l'indirizzo completo del collegamento ipertestuale per una forma.

```csharp
public string HRef { get; set; }
```

### Osservazioni

Il valore predefinito è una stringa vuota.

Di seguito sono riportati esempi di valori validi per questa proprietà:

URI completo:`https://www.aspose.com/`.

Nome completo del file:`C:\\Documenti\\RapportoVendite.doc`.

URI relativo:`../../../risorsa.txt`

Nome file relativo:`..\\Documenti\\RapportoVendite.doc`.

Segnalibro all'interno di un altro documento:`https://www.aspose.com/Products/Default.aspx#Suites`

Segnalibro all'interno di questo documento:`#NomeLibro`.

### Esempi

Mostra come inserire una forma che contiene un'immagine ed è anche un collegamento ipertestuale.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.HRef = "https://forum.aspose.com/";
shape.Target = "New Window";
shape.ScreenTip = "Aspose.Words Support Forums";

// Ctrl + facendo clic con il pulsante sinistro del mouse sulla forma in Microsoft Word si aprirà una nuova finestra del browser Web
// e portaci al collegamento ipertestuale nella proprietà "HRef".
doc.Save(ArtifactsDir + "Image.InsertImageWithHyperlink.docx");
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../shapebase/)
* assemblea [Aspose.Words](../../../)


