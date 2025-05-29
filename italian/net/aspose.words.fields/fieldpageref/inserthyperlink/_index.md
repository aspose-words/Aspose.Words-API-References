---
title: FieldPageRef.InsertHyperlink
linktitle: InsertHyperlink
articleTitle: InsertHyperlink
second_title: Aspose.Words per .NET
description: Scopri come la proprietà FieldPageRef InsertHyperlink migliora i tuoi documenti collegandoli facilmente ai paragrafi con segnalibro per una navigazione fluida.
type: docs
weight: 30
url: /it/net/aspose.words.fields/fieldpageref/inserthyperlink/
---
## FieldPageRef.InsertHyperlink property

Ottiene o imposta se inserire un collegamento ipertestuale al paragrafo aggiunto ai segnalibri.

```csharp
public bool InsertHyperlink { get; set; }
```

## Esempi

Mostra come inserire campi PAGEREF per visualizzare la posizione relativa dei segnalibri.

```csharp
public void FieldPageRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    InsertAndNameBookmark(builder, "MyBookmark1");

    // Inserire un campo PAGEREF che visualizza la pagina in cui si trova un segnalibro.
    // Imposta il flag InsertHyperlink per fare in modo che il campo funzioni anche come collegamento cliccabile al segnalibro.
    Assert.AreEqual(" PAGEREF  MyBookmark3 \\h", 
        InsertFieldPageRef(builder, "MyBookmark3", true, false, "Hyperlink to Bookmark3, on page: ").GetFieldCode());

    // Possiamo usare il flag \p per visualizzare il campo PAGEREF
    // la posizione del segnalibro rispetto alla posizione del campo.
    // Bookmark1 si trova sulla stessa pagina e sopra questo campo, quindi il risultato visualizzato per questo campo sarà "sopra".
    Assert.AreEqual(" PAGEREF  MyBookmark1 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark1", true, true, "Bookmark1 is ").GetFieldCode());

    // Bookmark2 sarà sulla stessa pagina e sotto questo campo, quindi il risultato visualizzato di questo campo sarà "sotto".
    Assert.AreEqual(" PAGEREF  MyBookmark2 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark2", true, true, "Bookmark2 is ").GetFieldCode());

    // Bookmark3 sarà su una pagina diversa, quindi il campo visualizzerà "a pagina 2".
    Assert.AreEqual(" PAGEREF  MyBookmark3 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark3", true, true, "Bookmark3 is ").GetFieldCode());

    InsertAndNameBookmark(builder, "MyBookmark2");
    builder.InsertBreak(BreakType.PageBreak);
    InsertAndNameBookmark(builder, "MyBookmark3");

    doc.UpdatePageLayout();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.PAGEREF.docx");
}

/// <summary>
/// Utilizza un generatore di documenti per inserire un campo PAGEREF e impostarne le proprietà.
/// </summary>
private static FieldPageRef InsertFieldPageRef(DocumentBuilder builder, string bookmarkName, bool insertHyperlink, bool insertRelativePosition, string textBefore)
{
    builder.Write(textBefore);

    FieldPageRef field = (FieldPageRef)builder.InsertField(FieldType.FieldPageRef, true);
    field.BookmarkName = bookmarkName;
    field.InsertHyperlink = insertHyperlink;
    field.InsertRelativePosition = insertRelativePosition;
    builder.Writeln();

    return field;
}

/// <summary>
/// Utilizza un generatore di documenti per inserire un segnalibro denominato.
/// </summary>
private static void InsertAndNameBookmark(DocumentBuilder builder, string bookmarkName)
{
    builder.StartBookmark(bookmarkName);
    builder.Writeln($"Contents of bookmark \"{bookmarkName}\".");
    builder.EndBookmark(bookmarkName);
}
```

### Guarda anche

* class [FieldPageRef](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
