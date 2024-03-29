---
title: SignatureLine Class
linktitle: SignatureLine
articleTitle: SignatureLine
second_title: Aspose.Words per .NET
description: Aspose.Words.Drawing.SignatureLine classe. Fornisce laccesso alle proprietà della riga della firma in C#.
type: docs
weight: 1300
url: /it/net/aspose.words.drawing/signatureline/
---
## SignatureLine class

Fornisce l'accesso alle proprietà della riga della firma.

Per saperne di più, visita il[Lavora con le firme digitali](https://docs.aspose.com/words/net/working-with-digital-signatures/) articolo di documentazione.

```csharp
public class SignatureLine
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [AllowComments](../../aspose.words.drawing/signatureline/allowcomments/) { get; set; } | Ottiene o imposta un valore che indica che il firmatario può aggiungere commenti nella finestra di dialogo Firma. Il valore predefinito per questa proprietà è`falso` . |
| [DefaultInstructions](../../aspose.words.drawing/signatureline/defaultinstructions/) { get; set; } | Ottiene o imposta un valore che indica che le istruzioni predefinite vengono visualizzate nella finestra di dialogo Firma. Il valore predefinito per questa proprietà è`VERO` . |
| [Email](../../aspose.words.drawing/signatureline/email/) { get; set; } | Ottiene o imposta l'indirizzo e-mail del firmatario suggerito. Il valore predefinito per questa proprietà è**stringa vuota** (Empty). |
| [Id](../../aspose.words.drawing/signatureline/id/) { get; set; } | Ottiene o imposta l'identificatore per questa riga della firma. |
| [Instructions](../../aspose.words.drawing/signatureline/instructions/) { get; set; } | Ottiene o imposta le istruzioni per il firmatario visualizzate alla firma della riga della firma. Questa proprietà viene ignorata se[`DefaultInstructions`](./defaultinstructions/)è impostato. Il valore predefinito per questa proprietà è**stringa vuota** (Empty). |
| [IsSigned](../../aspose.words.drawing/signatureline/issigned/) { get; } | Indica che la riga della firma è firmata tramite firma digitale. |
| [IsValid](../../aspose.words.drawing/signatureline/isvalid/) { get; } | Indica che la riga della firma è firmata tramite firma digitale e questa firma digitale è valida. |
| [ProviderId](../../aspose.words.drawing/signatureline/providerid/) { get; set; } | Ottiene o imposta l'identificatore del fornitore della firma per questa riga della firma. Il valore predefinito è "{00000000-0000-0000-0000-000000000000}". |
| [ShowDate](../../aspose.words.drawing/signatureline/showdate/) { get; set; } | Ottiene o imposta un valore che indica che la data del segno è visualizzata nella riga della firma. Il valore predefinito per questa proprietà è`VERO` . |
| [Signer](../../aspose.words.drawing/signatureline/signer/) { get; set; } | Ottiene o imposta il firmatario suggerito per la riga della firma. Il valore predefinito per questa proprietà è**stringa vuota** (Empty). |
| [SignerTitle](../../aspose.words.drawing/signatureline/signertitle/) { get; set; } | Ottiene o imposta il titolo del firmatario suggerito (ad esempio, Manager). Il valore predefinito per questa proprietà è**stringa vuota** (Empty). |

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

* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
