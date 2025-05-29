---
title: PageSetup.BorderSurroundsFooter
linktitle: BorderSurroundsFooter
articleTitle: BorderSurroundsFooter
second_title: Aspose.Words per .NET
description: Scopri come la proprietà BorderSurroundsFooter di PageSetup può migliorare il layout del tuo documento controllando l'inclusione del piè di pagina nei bordi della pagina.
type: docs
weight: 60
url: /it/net/aspose.words/pagesetup/bordersurroundsfooter/
---
## PageSetup.BorderSurroundsFooter property

Specifica se il bordo della pagina include o esclude il piè di pagina.

```csharp
public bool BorderSurroundsFooter { get; set; }
```

## Osservazioni

Nota: la modifica di questa proprietà influisce su tutte le sezioni del documento.

## Esempi

Mostra come applicare un bordo alla pagina e all'intestazione/piè di pagina.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! This is the main body text.");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer.");
builder.MoveToDocumentEnd();

// Inserisci un bordo blu a doppia linea.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.Borders.LineStyle = LineStyle.Double;
pageSetup.Borders.Color = Color.Blue;

// L'oggetto PageSetup di una sezione ha i flag "BorderSurroundsHeader" e "BorderSurroundsFooter" che determinano
// se un bordo di pagina circonda il testo principale, includendo rispettivamente anche l'intestazione o il piè di pagina.
// Imposta il flag "BorderSurroundsHeader" su "true" per circondare l'intestazione con il nostro bordo,
// e quindi imposta il flag "BorderSurroundsFooter" per lasciare il piè di pagina all'esterno del bordo.
pageSetup.BorderSurroundsHeader = true;
pageSetup.BorderSurroundsFooter = false;

doc.Save(ArtifactsDir + "PageSetup.PageBorder.docx");
```

### Guarda anche

* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
