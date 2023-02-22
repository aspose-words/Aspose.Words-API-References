---
title: ParagraphFormat.Bidi
second_title: Aspose.Words per .NET API Reference
description: ParagraphFormat proprietà. Ottiene o imposta se si tratta di un paragrafo da destra a sinistra.
type: docs
weight: 40
url: /it/net/aspose.words/paragraphformat/bidi/
---
## ParagraphFormat.Bidi property

Ottiene o imposta se si tratta di un paragrafo da destra a sinistra.

```csharp
public bool Bidi { get; set; }
```

### Osservazioni

Se true, le corse e altri oggetti inline in questo paragrafo sono disposti da destra a sinistra.

### Esempi

Mostra come rilevare la direzione del testo del documento in testo normale.

```csharp
// Crea un oggetto "TxtLoadOptions", che possiamo passare al costruttore di un documento
// per modificare il modo in cui carichiamo un documento di testo normale.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Imposta la proprietà "DocumentDirection" su "DocumentDirection.Auto" rileva automaticamente
// la direzione di ogni paragrafo di testo che Aspose.Words carica dal testo in chiaro.
// La proprietà "Bidi" di ogni paragrafo memorizzerà la sua direzione.
loadOptions.DocumentDirection = DocumentDirection.Auto;

// Rileva il testo ebraico da destra a sinistra.
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// Rileva il testo inglese come da destra a sinistra.
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

Mostra come creare elenchi compatibili con la lingua da destra a sinistra con i campi BIDIOUTLINE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Il campo BIDIOUTLINE numera i paragrafi come i campi AUTONUM/LISTNUM,
// ma è visibile solo quando è abilitata una lingua di modifica da destra a sinistra, come l'ebraico o l'arabo.
// Il campo seguente visualizzerà ".1", l'equivalente RTL del numero di elenco "1.".
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// Aggiungi altri due campi BIDIOUTLINE, che visualizzeranno ".2" e ".3".
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

// Imposta l'allineamento orizzontale del testo per ogni paragrafo del documento su RTL.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
{
    para.ParagraphFormat.Bidi = true;
}

// Se abilitiamo una lingua di modifica da destra a sinistra in Microsoft Word, i nostri campi visualizzeranno dei numeri.
// Altrimenti visualizzeranno "###".
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

### Guarda anche

* class [ParagraphFormat](../)
* spazio dei nomi [Aspose.Words](../../paragraphformat/)
* assemblea [Aspose.Words](../../../)


