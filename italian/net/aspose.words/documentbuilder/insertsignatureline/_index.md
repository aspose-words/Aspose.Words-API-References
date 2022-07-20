---
title: InsertSignatureLine
second_title: Aspose.Words per .NET API Reference
description: Inserisce una linea di firma nella posizione corrente.
type: docs
weight: 420
url: /it/net/aspose.words/documentbuilder/insertsignatureline/
---
## InsertSignatureLine(SignatureLineOptions) {#insertsignatureline}

Inserisce una linea di firma nella posizione corrente.

```csharp
public Shape InsertSignatureLine(SignatureLineOptions signatureLineOptions)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| signatureLineOptions | SignatureLineOptions | L'oggetto che memorizza i parametri di creazione della riga della firma. |

### Valore di ritorno

Il nodo della linea della firma appena inserito.

### Esempi

Mostra come firmare un documento con un certificato personale e una riga di firma.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

SignatureLineOptions signatureLineOptions = new SignatureLineOptions
{
    Signer = "vderyushev",
    SignerTitle = "QA",
    Email = "vderyushev@aspose.com",
    ShowDate = true,
    DefaultInstructions = false,
    Instructions = "Please sign here.",
    AllowComments = true
};

SignatureLine signatureLine = builder.InsertSignatureLine(signatureLineOptions).SignatureLine;
signatureLine.ProviderId = Guid.Parse("CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2");

Assert.False(signatureLine.IsSigned);
Assert.False(signatureLine.IsValid);

doc.Save(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.docx");

SignOptions signOptions = new SignOptions
{
    SignatureLineId = signatureLine.Id,
    ProviderId = signatureLine.ProviderId,
    Comments = "Document was signed by vderyushev",
    SignTime = DateTime.Now
};

CertificateHolder certHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

DigitalSignatureUtil.Sign(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.docx", 
    ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx", certHolder, signOptions);

// Riapri il nostro documento salvato e verifica che le proprietà "IsSigned" e "IsValid" siano entrambe "true",
// indicando che la riga della firma contiene una firma.
doc = new Document(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
signatureLine = shape.SignatureLine;

Assert.True(signatureLine.IsSigned);
Assert.True(signatureLine.IsValid);
```

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape)
* class [SignatureLineOptions](../../signaturelineoptions)
* class [DocumentBuilder](../../documentbuilder)
* spazio dei nomi [Aspose.Words](../../documentbuilder)
* assemblea [Aspose.Words](../../../)

---

## InsertSignatureLine(SignatureLineOptions, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, WrapType) {#insertsignatureline_1}

Inserisce una riga della firma nella posizione specificata.

```csharp
public Shape InsertSignatureLine(SignatureLineOptions signatureLineOptions, 
    RelativeHorizontalPosition horzPos, double left, RelativeVerticalPosition vertPos, double top, 
    WrapType wrapType)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| signatureLineOptions | SignatureLineOptions | L'oggetto che memorizza i parametri di creazione della riga della firma. |
| horzPos | RelativeHorizontalPosition | Specifica da dove viene misurata la distanza dalla linea della firma. |
| left | Double | Distanza in punti dall'origine al lato sinistro della linea di segnatura. |
| vertPos | RelativeVerticalPosition | Specifica da dove viene misurata la distanza dalla linea della firma. |
| top | Double | Distanza in punti dall'origine al lato superiore della linea della firma. |
| wrapType | WrapType | Specifica come avvolgere il testo attorno alla riga della firma. |

### Valore di ritorno

Il nodo della linea della firma appena inserito.

### Osservazioni

È possibile modificare la dimensione dell'immagine, la posizione, il metodo di posizionamento e altre impostazioni utilizzando [`Shape`](../../../aspose.words.drawing/shape) oggetto restituito da questo metodo.

### Esempi

Mostra come inserire una linea di firma in linea in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

SignatureLineOptions options = new SignatureLineOptions
{
    Signer = "John Doe",
    SignerTitle = "Manager",
    Email = "johndoe@aspose.com",
    ShowDate = true,
    DefaultInstructions = false,
    Instructions = "Please sign here.",
    AllowComments = true
};

builder.InsertSignatureLine(options, RelativeHorizontalPosition.RightMargin, 2.0,
    RelativeVerticalPosition.Page, 3.0, WrapType.Inline);

// La riga della firma può essere firmata in Microsoft Word facendo doppio clic su di essa.
doc.Save(ArtifactsDir + "DocumentBuilder.SignatureLineInline.docx");
```

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape)
* class [SignatureLineOptions](../../signaturelineoptions)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition)
* enum [WrapType](../../../aspose.words.drawing/wraptype)
* class [DocumentBuilder](../../documentbuilder)
* spazio dei nomi [Aspose.Words](../../documentbuilder)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
