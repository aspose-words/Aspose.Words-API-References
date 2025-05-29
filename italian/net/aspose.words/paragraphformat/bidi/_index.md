---
title: ParagraphFormat.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words per .NET
description: Scopri la proprietà Bidi ParagraphFormat per controllare facilmente la formattazione del testo da destra a sinistra, migliorando così la leggibilità e il layout del documento.
type: docs
weight: 50
url: /it/net/aspose.words/paragraphformat/bidi/
---
## ParagraphFormat.Bidi property

Ottiene o imposta se questo è un paragrafo da destra a sinistra.

```csharp
public bool Bidi { get; set; }
```

## Osservazioni

Quando`VERO`, le esecuzioni e gli altri oggetti in linea in questo paragrafo sono disposti da destra a sinistra.

## Esempi

Mostra come rilevare la direzione del testo in un documento di testo normale.

```csharp
// Creiamo un oggetto "TxtLoadOptions", che possiamo passare al costruttore di un documento
// per modificare il modo in cui carichiamo un documento di testo normale.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Imposta la proprietà "DocumentDirection" su "DocumentDirection.Auto" rileva automaticamente
// la direzione di ogni paragrafo di testo che Aspose.Words carica dal testo normale.
// La proprietà "Bidi" di ogni paragrafo memorizzerà la sua direzione.
loadOptions.DocumentDirection = DocumentDirection.Auto;

// Rileva il testo ebraico come scritto da destra a sinistra.
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// Rileva il testo inglese come scritto da destra a sinistra.
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

Mostra come creare elenchi compatibili con le lingue con scrittura da destra a sinistra con campi BIDIOUTLINE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Il campo BIDIOUTLINE numera i paragrafi come i campi AUTONUM/LISTNUM,
// ma è visibile solo quando è abilitata una lingua di modifica da destra a sinistra, come l'ebraico o l'arabo.
// Il campo seguente visualizzerà ".1", l'equivalente RTL del numero di elenco "1.".
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// Aggiungere altri due campi BIDIOUTLINE, che visualizzeranno ".2" e ".3".
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

// Imposta l'allineamento orizzontale del testo per ogni paragrafo del documento su RTL.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
{
    para.ParagraphFormat.Bidi = true;
}

// Se abilitiamo una lingua di modifica da destra a sinistra in Microsoft Word, i nostri campi visualizzeranno numeri.
// Altrimenti verrà visualizzato "###".
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

### Guarda anche

* class [ParagraphFormat](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
