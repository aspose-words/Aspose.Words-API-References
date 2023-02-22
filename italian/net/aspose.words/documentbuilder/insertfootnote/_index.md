---
title: DocumentBuilder.InsertFootnote
second_title: Aspose.Words per .NET API Reference
description: DocumentBuilder metodo. Inserisce una nota a piè di pagina o una nota di chiusura nel documento.
type: docs
weight: 310
url: /it/net/aspose.words/documentbuilder/insertfootnote/
---
## InsertFootnote(FootnoteType, string) {#insertfootnote}

Inserisce una nota a piè di pagina o una nota di chiusura nel documento.

```csharp
public Footnote InsertFootnote(FootnoteType footnoteType, string footnoteText)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| footnoteType | FootnoteType | Specifica se inserire una nota a piè di pagina o una nota di chiusura. |
| footnoteText | String | Specifica il testo della nota a piè di pagina. |

### Valore di ritorno

Restituisce un oggetto nota a piè di pagina che è stato appena creato.

### Esempi

Mostra come fare riferimento al testo con una nota a piè di pagina e una nota di chiusura.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci del testo e contrassegnalo con una nota a piè di pagina con la proprietà IsAuto impostata su "true" per impostazione predefinita,
// quindi il marcatore visto nel corpo del testo sarà numerato automaticamente a "1",
// e la nota a piè di pagina apparirà in fondo alla pagina.
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// Inserisci più testo e contrassegnalo con una nota di chiusura con un segno di riferimento personalizzato,
// che verrà utilizzato al posto del numero "2" e imposterà "IsAuto" su false.
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// Le note a piè di pagina appaiono sempre in fondo al testo di riferimento,
// quindi questa interruzione di pagina non influirà sulla nota a piè di pagina.
// D'altra parte, le note di chiusura sono sempre alla fine del documento
// in modo che questa interruzione di pagina spinga la nota di chiusura alla pagina successiva.
builder.InsertBreak(BreakType.PageBreak);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFootnote.docx");
```

### Guarda anche

* class [Footnote](../../../aspose.words.notes/footnote/)
* enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../documentbuilder/)
* assemblea [Aspose.Words](../../../)

---

## InsertFootnote(FootnoteType, string, string) {#insertfootnote_1}

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

Restituisce un oggetto nota a piè di pagina che è stato appena creato.

### Esempi

Mostra come fare riferimento al testo con una nota a piè di pagina e una nota di chiusura.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci del testo e contrassegnalo con una nota a piè di pagina con la proprietà IsAuto impostata su "true" per impostazione predefinita,
// quindi il marcatore visto nel corpo del testo sarà numerato automaticamente a "1",
// e la nota a piè di pagina apparirà in fondo alla pagina.
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// Inserisci più testo e contrassegnalo con una nota di chiusura con un segno di riferimento personalizzato,
// che verrà utilizzato al posto del numero "2" e imposterà "IsAuto" su false.
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// Le note a piè di pagina appaiono sempre in fondo al testo di riferimento,
// quindi questa interruzione di pagina non influirà sulla nota a piè di pagina.
// D'altra parte, le note di chiusura sono sempre alla fine del documento
// in modo che questa interruzione di pagina spinga la nota di chiusura alla pagina successiva.
builder.InsertBreak(BreakType.PageBreak);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFootnote.docx");
```

### Guarda anche

* class [Footnote](../../../aspose.words.notes/footnote/)
* enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../documentbuilder/)
* assemblea [Aspose.Words](../../../)


