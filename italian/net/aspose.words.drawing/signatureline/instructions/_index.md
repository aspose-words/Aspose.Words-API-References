---
title: SignatureLine.Instructions
linktitle: Instructions
articleTitle: Instructions
second_title: Aspose.Words per .NET
description: SignatureLine Instructions proprietà. Ottiene o imposta le istruzioni per il firmatario visualizzate alla firma della riga della firma. Questa proprietà viene ignorata seDefaultInstructionsè impostato. Il valore predefinito per questa proprietà èstringa vuota Empty in C#.
type: docs
weight: 50
url: /it/net/aspose.words.drawing/signatureline/instructions/
---
## SignatureLine.Instructions property

Ottiene o imposta le istruzioni per il firmatario visualizzate alla firma della riga della firma. Questa proprietà viene ignorata se[`DefaultInstructions`](../defaultinstructions/)è impostato. Il valore predefinito per questa proprietà è**stringa vuota** (Empty).

```csharp
public string Instructions { get; set; }
```

## Esempi

Mostra come creare una riga per una firma e inserirla in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

SignatureLineOptions options = new SignatureLineOptions
{
    AllowComments = true,
    DefaultInstructions = true,
    Email = "john.doe@management.com",
    Instructions = "Please sign here",
    ShowDate = true,
    Signer = "John Doe",
    SignerTitle = "Senior Manager"
};

// Inserisci una forma che conterrà una riga della firma, di cui modificheremo l'aspetto
// personalizza utilizzando l'oggetto "SignatureLineOptions" che abbiamo creato sopra.
// Se inseriamo una forma le cui coordinate hanno origine nell'angolo in basso a destra della pagina,
// dovremo fornire le coordinate xey negative per visualizzare la forma.
Shape shape = builder.InsertSignatureLine(options, RelativeHorizontalPosition.RightMargin, -170.0, 
        RelativeVerticalPosition.BottomMargin, -60.0, WrapType.None);

Assert.True(shape.IsSignatureLine);

// Verifica le proprietà della nostra riga della firma tramite il suo oggetto Shape.
SignatureLine signatureLine = shape.SignatureLine;

Assert.AreEqual("john.doe@management.com", signatureLine.Email);
Assert.AreEqual("John Doe", signatureLine.Signer);
Assert.AreEqual("Senior Manager", signatureLine.SignerTitle);
Assert.AreEqual("Please sign here", signatureLine.Instructions);
Assert.True(signatureLine.ShowDate);
Assert.True(signatureLine.AllowComments);
Assert.True(signatureLine.DefaultInstructions);

doc.Save(ArtifactsDir + "Shape.SignatureLine.docx");
```

### Guarda anche

* class [SignatureLine](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
