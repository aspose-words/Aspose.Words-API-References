---
title: DocumentBuilder
linktitle: DocumentBuilder
articleTitle: DocumentBuilder
second_title: Aspose.Words per .NET
description: Crea documenti efficaci senza sforzo con DocumentBuilder. Inizializza una nuova istanza e semplifica la gestione dei tuoi documenti oggi stesso!
type: docs
weight: 10
url: /it/net/aspose.words/documentbuilder/documentbuilder/
---
## DocumentBuilder() {#constructor}

Inizializza una nuova istanza di questa classe.

```csharp
public DocumentBuilder()
```

## Osservazioni

Crea un nuovo[`DocumentBuilder`](../)oggetto e lo collega a un nuovo[`Document`](../../document/) oggetto.

## Esempi

Mostra come inserire testo formattato utilizzando DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Specificare la formattazione del carattere, quindi aggiungere il testo.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

### Guarda anche

* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## DocumentBuilder(*[DocumentBuilderOptions](../../documentbuilderoptions/)*) {#constructor_3}

Inizializza una nuova istanza di questa classe.

```csharp
public DocumentBuilder(DocumentBuilderOptions options)
```

## Osservazioni

Crea un nuovo[`DocumentBuilder`](../)oggetto e lo collega a un nuovo[`Document`](../../document/) object. È possibile specificare ulteriori opzioni di creazione del documento.

## Esempi

Mostra come ignorare la formattazione della tabella per il contenuto successivo.

```csharp
Document doc = new Document();
DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
builderOptions.ContextTableFormatting = true;
DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

// Aggiunge contenuto prima della tabella.
// La dimensione predefinita del carattere è 12.
builder.Writeln("Font size 12 here.");
builder.StartTable();
builder.InsertCell();
// Modifica la dimensione del carattere all'interno della tabella.
builder.Font.Size = 5;
builder.Write("Font size 5 here");
builder.InsertCell();
builder.Write("Font size 5 here");
builder.EndRow();
builder.EndTable();

// Se ContextTableFormatting è true, la formattazione della tabella non viene applicata al contenuto successivo.
// Se ContextTableFormatting è falso, la formattazione della tabella viene applicata al contenuto successivo.
builder.Writeln("Font size 12 here.");

doc.Save(ArtifactsDir + "Table.ContextTableFormatting.docx");
```

### Guarda anche

* class [DocumentBuilderOptions](../../documentbuilderoptions/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## DocumentBuilder(*[Document](../../document/)*) {#constructor_1}

Inizializza una nuova istanza di questa classe.

```csharp
public DocumentBuilder(Document doc)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| doc | Document | IL[`Document`](../../document/) oggetto a cui attaccarsi. |

## Osservazioni

Crea un nuovo[`DocumentBuilder`](../) oggetto, si collega a quello specificato[`Document`](../../document/) oggetto. Il cursore è posizionato all'inizio del documento.

## Esempi

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

Mostra come inserire un indice (TOC) in un documento utilizzando gli stili di intestazione come voci.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserire un indice per la prima pagina del documento.
// Configura la tabella in modo che selezioni i paragrafi con titoli di livello da 1 a 3.
// Inoltre, imposta le sue voci come collegamenti ipertestuali che ci porteranno
// alla posizione dell'intestazione quando si fa clic con il pulsante sinistro del mouse in Microsoft Word.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Popola il sommario aggiungendo paragrafi con stili di intestazione.
// Ciascuna intestazione con un livello compreso tra 1 e 3 creerà una voce nella tabella.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 2");
builder.Writeln("Heading 3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;
builder.Writeln("Heading 3.1.1");
builder.Writeln("Heading 3.1.2");
builder.Writeln("Heading 3.1.3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;
builder.Writeln("Heading 3.1.3.1");
builder.Writeln("Heading 3.1.3.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.2");
builder.Writeln("Heading 3.3");

// Un indice è un campo di un tipo che deve essere aggiornato per mostrare un risultato aggiornato.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### Guarda anche

* class [Document](../../document/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## DocumentBuilder(*[Document](../../document/), [DocumentBuilderOptions](../../documentbuilderoptions/)*) {#constructor_2}

Inizializza una nuova istanza di questa classe.

```csharp
public DocumentBuilder(Document doc, DocumentBuilderOptions options)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| doc | Document | IL[`Document`](../../document/) oggetto a cui attaccarsi. |
| options | DocumentBuilderOptions | Opzioni aggiuntive per il processo di creazione del documento. |

## Osservazioni

Crea un nuovo[`DocumentBuilder`](../) oggetto, si collega a quello specificato[`Document`](../../document/) oggetto. Il cursore è posizionato all'inizio del documento.

## Esempi

Mostra come ignorare la formattazione della tabella per il contenuto successivo.

```csharp
Document doc = new Document();
DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
builderOptions.ContextTableFormatting = true;
DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

// Aggiunge contenuto prima della tabella.
// La dimensione predefinita del carattere è 12.
builder.Writeln("Font size 12 here.");
builder.StartTable();
builder.InsertCell();
// Modifica la dimensione del carattere all'interno della tabella.
builder.Font.Size = 5;
builder.Write("Font size 5 here");
builder.InsertCell();
builder.Write("Font size 5 here");
builder.EndRow();
builder.EndTable();

// Se ContextTableFormatting è true, la formattazione della tabella non viene applicata al contenuto successivo.
// Se ContextTableFormatting è falso, la formattazione della tabella viene applicata al contenuto successivo.
builder.Writeln("Font size 12 here.");

doc.Save(ArtifactsDir + "Table.ContextTableFormatting.docx");
```

### Guarda anche

* class [Document](../../document/)
* class [DocumentBuilderOptions](../../documentbuilderoptions/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
