---
title: DocumentBuilder.MoveToHeaderFooter
linktitle: MoveToHeaderFooter
articleTitle: MoveToHeaderFooter
second_title: Aspose.Words per .NET
description: Con il metodo MoveToHeaderFooter di DocumentBuilder puoi spostarti senza sforzo tra intestazioni e piè di pagina, migliorando l'efficienza nella modifica dei documenti.
type: docs
weight: 580
url: /it/net/aspose.words/documentbuilder/movetoheaderfooter/
---
## DocumentBuilder.MoveToHeaderFooter method

Sposta il cursore all'inizio di un'intestazione o di un piè di pagina nella sezione corrente.

```csharp
public void MoveToHeaderFooter(HeaderFooterType headerFooterType)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| headerFooterType | HeaderFooterType | Specifica l'intestazione o il piè di pagina a cui spostarsi. |

## Osservazioni

Dopo aver spostato il cursore su un'intestazione o un piè di pagina, puoi utilizzare il resto[`DocumentBuilder`](../) Metodi per modificare il contenuto dell'intestazione o del piè di pagina.

Se vuoi creare intestazioni e piè di pagina diversi per la prima pagina, devi impostare [`DifferentFirstPageHeaderFooter`](../../pagesetup/differentfirstpageheaderfooter/).

Se vuoi creare intestazioni e piè di pagina diversi per le pagine pari e dispari, devi impostare [`OddAndEvenPagesHeaderFooter`](../../pagesetup/oddandevenpagesheaderfooter/).

Utilizzo[`MoveToSection`](../movetosection/) per passare dall'intestazione al testo principale.

## Esempi

Mostra come inserire un'immagine e utilizzarla come filigrana.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci l'immagine nell'intestazione in modo che sia visibile su ogni pagina.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");
shape.WrapType = WrapType.None;
shape.BehindText = true;

// Posiziona l'immagine al centro della pagina.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

Mostra come creare intestazioni e piè di pagina in un documento utilizzando DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Specificare che si vogliono intestazioni e piè di pagina diversi per la prima pagina, le pagine pari e quelle dispari.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Crea le intestazioni, quindi aggiungi tre pagine al documento per visualizzare ciascun tipo di intestazione.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

### Guarda anche

* enum [HeaderFooterType](../../headerfootertype/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
