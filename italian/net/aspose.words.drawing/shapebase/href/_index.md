---
title: ShapeBase.HRef
linktitle: HRef
articleTitle: HRef
second_title: Aspose.Words per .NET
description: Scopri la proprietà ShapeBase HRef per gestire facilmente gli indirizzi completi dei collegamenti ipertestuali per le tue forme, migliorando l'interattività e la funzionalità del tuo design.
type: docs
weight: 250
url: /it/net/aspose.words.drawing/shapebase/href/
---
## ShapeBase.HRef property

Ottiene o imposta l'indirizzo completo del collegamento ipertestuale per una forma.

```csharp
public string HRef { get; set; }
```

## Osservazioni

Il valore predefinito è una stringa vuota.

Di seguito sono riportati alcuni esempi di valori validi per questa proprietà:

URI completo:`https://www.aspose.com/`.

Nome completo del file:`C:\\Documenti\\ReportVendite.doc`.

URI relativo:`../../../risorsa.txt`

Nome file relativo:`..\\Documenti\\RapportoVendite.doc`.

Aggiungi ai segnalibri in un altro documento:`https://www.aspose.com/Products/Default.aspx#Suites`

Aggiungi ai preferiti in questo documento:`#NomeSegnalibro`.

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
