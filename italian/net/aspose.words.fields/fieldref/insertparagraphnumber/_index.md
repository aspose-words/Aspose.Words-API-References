---
title: FieldRef.InsertParagraphNumber
linktitle: InsertParagraphNumber
articleTitle: InsertParagraphNumber
second_title: Aspose.Words per .NET
description: Scopri come la proprietà FieldRef InsertParagraphNumber ti consente di inserire facilmente numeri di paragrafo precisi dal tuo documento per una migliore gestione dei riferimenti.
type: docs
weight: 50
url: /it/net/aspose.words.fields/fieldref/insertparagraphnumber/
---
## FieldRef.InsertParagraphNumber property

Ottiene o imposta se inserire il numero del paragrafo a cui si fa riferimento esattamente come appare nel documento.

```csharp
public bool InsertParagraphNumber { get; set; }
```

## Esempi

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
