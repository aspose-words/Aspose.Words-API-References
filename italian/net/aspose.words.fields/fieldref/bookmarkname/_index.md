---
title: FieldRef.BookmarkName
linktitle: BookmarkName
articleTitle: BookmarkName
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldRef BookmarkName per gestire e personalizzare facilmente i tuoi segnalibri. Migliora la navigazione dei tuoi documenti senza sforzo!
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldref/bookmarkname/
---
## FieldRef.BookmarkName property

Ottiene o imposta il nome del segnalibro a cui si fa riferimento.

```csharp
public string BookmarkName { get; set; }
```

## Esempi

Mostra come creare testo con segnalibro con un campo SET e poi visualizzarlo nel documento utilizzando un campo REF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // Assegna un nome al testo aggiunto ai preferiti con un campo SET.
// Questo campo si riferisce al "segnalibro", non a una struttura di segnalibro che appare all'interno del testo, ma a una variabile denominata.
FieldSet fieldSet = (FieldSet)builder.InsertField(FieldType.FieldSet, false);
fieldSet.BookmarkName = "MyBookmark";
fieldSet.BookmarkText = "Hello world!";
fieldSet.Update();

Assert.AreEqual(" SET  MyBookmark \"Hello world!\"", fieldSet.GetFieldCode());

// Fare riferimento al segnalibro tramite il nome in un campo REF e visualizzarne il contenuto.
FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
fieldRef.BookmarkName = "MyBookmark";
fieldRef.Update();

Assert.AreEqual(" REF  MyBookmark", fieldRef.GetFieldCode());
Assert.AreEqual("Hello world!", fieldRef.Result);

doc.Save(ArtifactsDir + "Field.SET.REF.docx");
```

Mostra come inserire campi REF per fare riferimento ai segnalibri.

```csharp
public void FieldRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");
    builder.InsertFootnote(FootnoteType.Footnote, "MyBookmark footnote #1");
    builder.Write("Text that will appear in REF field");
    builder.InsertFootnote(FootnoteType.Footnote, "MyBookmark footnote #2");
    builder.EndBookmark("MyBookmark");
    builder.MoveToDocumentStart();

    // Applicheremo un formato di elenco personalizzato, in cui la quantità di parentesi angolari indica il livello di elenco in cui ci troviamo attualmente.
    builder.ListFormat.ApplyNumberDefault();
    builder.ListFormat.ListLevel.NumberFormat = "> \x0000";

    // Inserire un campo REF che conterrà il testo all'interno del nostro segnalibro, fungerà da collegamento ipertestuale e clonerà le note a piè di pagina del segnalibro.
    FieldRef field = InsertFieldRef(builder, "MyBookmark", "", "\n");
    field.IncludeNoteOrComment = true;
    field.InsertHyperlink = true;

    Assert.AreEqual(" REF  MyBookmark \\f \\h", field.GetFieldCode());

    // Inserisce un campo RIF. e visualizza se il segnalibro a cui si fa riferimento si trova sopra o sotto di esso.
    field = InsertFieldRef(builder, "MyBookmark", "The referenced paragraph is ", " this field.\n");
    field.InsertRelativePosition = true;

    Assert.AreEqual(" REF  MyBookmark \\p", field.GetFieldCode());

    // Visualizza il numero dell'elenco del segnalibro così come appare nel documento.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number is ", "\n");
    field.InsertParagraphNumber = true;

    Assert.AreEqual(" REF  MyBookmark \\n", field.GetFieldCode());

    // Visualizza il numero dell'elenco dei segnalibri, omettendo però i caratteri non delimitatori, come le parentesi angolari.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number, non-delimiters suppressed, is ", "\n");
    field.InsertParagraphNumber = true;
    field.SuppressNonDelimiters = true;

    Assert.AreEqual(" REF  MyBookmark \\n \\t", field.GetFieldCode());

    // Spostarsi di un livello nell'elenco.
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">> \x0001";

    // Visualizza il numero dell'elenco del segnalibro e i numeri di tutti i livelli di elenco superiori.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's full context paragraph number is ", "\n");
    field.InsertParagraphNumberInFullContext = true;

    Assert.AreEqual(" REF  MyBookmark \\w", field.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // Visualizza i numeri del livello di elenco tra questo campo REF e il segnalibro a cui fa riferimento.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's relative paragraph number is ", "\n");
    field.InsertParagraphNumberInRelativeContext = true;

    Assert.AreEqual(" REF  MyBookmark \\r", field.GetFieldCode());

    // Alla fine del documento, il segnalibro verrà visualizzato come elemento dell'elenco.
    builder.Writeln("List level above bookmark");
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">>> \x0002";

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.REF.docx");
}

/// <summary>
/// Fai in modo che il generatore di documenti inserisca un campo REF, faccia riferimento a un segnalibro con esso e aggiunga del testo prima e dopo.
/// </summary>
private static FieldRef InsertFieldRef(DocumentBuilder builder, string bookmarkName, string textBefore, string textAfter)
{
    builder.Write(textBefore);
    FieldRef field = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
    field.BookmarkName = bookmarkName;
    builder.Write(textAfter);
    return field;
}
```

### Guarda anche

* class [FieldRef](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
