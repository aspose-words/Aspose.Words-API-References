---
title: DocumentBuilder.InsertFootnote
linktitle: InsertFootnote
articleTitle: InsertFootnote
second_title: Aspose.Words per .NET
description: Migliora i tuoi documenti senza sforzo con il metodo InsertFootnote di DocumentBuilder aggiungi facilmente note a piè di pagina o note di chiusura per maggiore chiarezza e professionalità.
type: docs
weight: 340
url: /it/net/aspose.words/documentbuilder/insertfootnote/
---
## InsertFootnote(*[FootnoteType](../../../aspose.words.notes/footnotetype/), string*) {#insertfootnote}

Inserisce una nota a piè di pagina o una nota di chiusura nel documento.

```csharp
public Footnote InsertFootnote(FootnoteType footnoteType, string footnoteText)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| footnoteType | FootnoteType | Specifica se inserire una nota a piè di pagina o una nota di chiusura. |
| footnoteText | String | Specifica il testo della nota a piè di pagina. |

### Valore di ritorno

Restituisce un oggetto nota a piè di pagina appena creato.

## Esempi

Mostra come fare riferimento al testo con una nota a piè di pagina e una nota di chiusura.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci del testo e contrassegnalo con una nota a piè di pagina con la proprietà IsAuto impostata su "true" per impostazione predefinita,
// quindi il marcatore visualizzato nel corpo del testo verrà numerato automaticamente a "1",
// e la nota a piè di pagina apparirà in fondo alla pagina.
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// Inserisci altro testo e contrassegnalo con una nota di chiusura con un segno di riferimento personalizzato,
// che verrà utilizzato al posto del numero "2" e impostare "IsAuto" su false.
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// Le note a piè di pagina appaiono sempre in fondo al testo a cui si fa riferimento,
// quindi questa interruzione di pagina non influirà sulla nota a piè di pagina.
// D'altra parte, le note di chiusura sono sempre alla fine del documento
// in modo che questa interruzione di pagina sposti la nota di chiusura alla pagina successiva.
builder.InsertBreak(BreakType.PageBreak);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFootnote.docx");
```

### Guarda anche

* class [Footnote](../../../aspose.words.notes/footnote/)
* enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## InsertFootnote(*[FootnoteType](../../../aspose.words.notes/footnotetype/), string, string*) {#insertfootnote_1}

Inserisce una nota a piè di pagina o una nota di chiusura nel documento.

```csharp
public Footnote InsertFootnote(FootnoteType footnoteType, string footnoteText, string referenceMark)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| footnoteType | FootnoteType | Specifica se inserire una nota a piè di pagina o una nota di chiusura. |
| footnoteText | String | Specifica il testo della nota a piè di pagina. |
| referenceMark | String | Specifica il segno di riferimento personalizzato della nota a piè di pagina. |

### Valore di ritorno

Restituisce un oggetto nota a piè di pagina appena creato.

## Esempi

Mostra come fare riferimento al testo con una nota a piè di pagina e una nota di chiusura.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci del testo e contrassegnalo con una nota a piè di pagina con la proprietà IsAuto impostata su "true" per impostazione predefinita,
// quindi il marcatore visualizzato nel corpo del testo verrà numerato automaticamente a "1",
// e la nota a piè di pagina apparirà in fondo alla pagina.
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// Inserisci altro testo e contrassegnalo con una nota di chiusura con un segno di riferimento personalizzato,
// che verrà utilizzato al posto del numero "2" e impostare "IsAuto" su false.
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// Le note a piè di pagina appaiono sempre in fondo al testo a cui si fa riferimento,
// quindi questa interruzione di pagina non influirà sulla nota a piè di pagina.
// D'altra parte, le note di chiusura sono sempre alla fine del documento
// in modo che questa interruzione di pagina sposti la nota di chiusura alla pagina successiva.
builder.InsertBreak(BreakType.PageBreak);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFootnote.docx");
```

### Guarda anche

* class [Footnote](../../../aspose.words.notes/footnote/)
* enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
