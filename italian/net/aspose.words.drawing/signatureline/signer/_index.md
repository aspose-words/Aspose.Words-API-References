---
title: SignatureLine.Signer
linktitle: Signer
articleTitle: Signer
second_title: Aspose.Words per .NET
description: Migliora i tuoi documenti con la proprietà SignatureLine Signer. Imposta facilmente i firmatari suggeriti per le righe di firma, semplificando il processo di firma senza sforzo.
type: docs
weight: 100
url: /it/net/aspose.words.drawing/signatureline/signer/
---
## SignatureLine.Signer property

Ottiene o imposta il firmatario suggerito della riga della firma. Il valore predefinito per questa proprietà è**stringa vuota** (Empty ).

```csharp
public string Signer { get; set; }
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

// Inserire una forma che conterrà una riga della firma, di cui vedremo l'aspetto
// personalizza utilizzando l'oggetto "SignatureLineOptions" che abbiamo creato sopra.
// Se inseriamo una forma le cui coordinate hanno origine nell'angolo in basso a destra della pagina,
// dovremo fornire le coordinate x e y negative per rendere visibile la forma.
Shape shape = builder.InsertSignatureLine(options, RelativeHorizontalPosition.RightMargin, -170.0,
        RelativeVerticalPosition.BottomMargin, -60.0, WrapType.None);

Assert.True(shape.IsSignatureLine);

// Verifichiamo le proprietà della nostra riga di firma tramite il suo oggetto Shape.
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
