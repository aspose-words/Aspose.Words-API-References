---
title: Document.UpdateFields
linktitle: UpdateFields
articleTitle: UpdateFields
second_title: Aspose.Words per .NET
description: Aggiorna il tuo documento con il metodo UpdateFields: aggiorna in modo efficiente tutti i valori dei campi per una maggiore precisione e una modifica fluida.
type: docs
weight: 810
url: /it/net/aspose.words/document/updatefields/
---
## Document.UpdateFields method

Aggiorna i valori dei campi nell'intero documento.

```csharp
public void UpdateFields()
```

## Osservazioni

Quando si apre, si modifica e si salva un documento, Aspose.Words non aggiorna automaticamente i campi, ma li mantiene intatti. Pertanto, in genere si desidera chiamare questo metodo prima di salvare se si è modificato il documento a livello di codice e si desidera assicurarsi che i valori dei campi corretti (calcolati) vengano visualizzati nel documento salvato.

Non è necessario aggiornare i campi dopo aver eseguito una stampa unione, perché la stampa unione è un tipo di aggiornamento di campo e aggiorna automaticamente tutti i campi nel documento.

Questo metodo non aggiorna tutti i tipi di campo. Per un elenco dettagliato dei tipi di campo supportati, consultare la Guida per i programmatori.

Questo metodo non aggiorna i campi correlati agli algoritmi di layout di pagina (ad esempio PAGE, PAGES, PAGEREF). I campi correlati al layout di pagina vengono aggiornati quando si esegue il rendering di un documento o si chiama[`UpdatePageLayout`](../updatepagelayout/).

Utilizzare il[`NormalizeFieldTypes`](../normalizefieldtypes/) metodo prima dell'aggiornamento dei campi se sono state apportate modifiche al documento che hanno interessato i tipi di campo.

Per aggiornare i campi in una parte specifica del documento utilizzare[`UpdateFields`](../../range/updatefields/).

## Esempi

Mostra come utilizzare il campo CITAZIONE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserire un campo QUOTE, che visualizzerà il valore della sua proprietà Text.
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.AreEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.GetFieldCode());

// Inserire un campo QUOTE e annidare al suo interno un campo DATE.
// I campi DATA aggiornano il loro valore alla data corrente ogni volta che apriamo il documento utilizzando Microsoft Word.
// Annidare il campo DATA all'interno del campo QUOTE in questo modo ne bloccherà il valore
// alla data in cui abbiamo creato il documento.
builder.Write("\nDocument creation date: ");
field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
builder.MoveTo(field.Separator);
builder.InsertField(FieldType.FieldDate, true);

Assert.AreEqual(" QUOTE \u0013 DATE \u0014" + DateTime.Now.Date.ToShortDateString() + "\u0015", field.GetFieldCode());

// Aggiorna tutti i campi per visualizzare i risultati corretti.
doc.UpdateFields();

Assert.AreEqual("\"Quoted text\"", doc.Range.Fields[0].Result);

doc.Save(ArtifactsDir + "Field.QUOTE.docx");
```

Mostra come impostare i dettagli dell'utente e visualizzarli utilizzando i campi.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un oggetto UserInformation e impostalo come origine dati per i campi che visualizzano le informazioni utente.
UserInformation userInformation = new UserInformation
{
    Name = "John Doe",
    Initials = "J. D.",
    Address = "123 Main Street"
};
doc.FieldOptions.CurrentUser = userInformation;

// Inserire i campi USERNAME, USERINITIALS e USERADDRESS, che visualizzano i valori di
 // le rispettive proprietà dell'oggetto UserInformation che abbiamo creato sopra.
Assert.AreEqual(userInformation.Name, builder.InsertField(" USERNAME ").Result);
Assert.AreEqual(userInformation.Initials, builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual(userInformation.Address, builder.InsertField(" USERADDRESS ").Result);

// L'oggetto opzioni campo ha anche un utente predefinito statico a cui possono fare riferimento i campi di tutti i documenti.
UserInformation.DefaultUser.Name = "Default User";
UserInformation.DefaultUser.Initials = "D. U.";
UserInformation.DefaultUser.Address = "One Microsoft Way";
doc.FieldOptions.CurrentUser = UserInformation.DefaultUser;

Assert.AreEqual("Default User", builder.InsertField(" USERNAME ").Result);
Assert.AreEqual("D. U.", builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual("One Microsoft Way", builder.InsertField(" USERADDRESS ").Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.CurrentUser.docx");
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

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
