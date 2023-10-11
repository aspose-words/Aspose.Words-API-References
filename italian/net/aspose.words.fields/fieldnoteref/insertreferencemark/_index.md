---
title: FieldNoteRef.InsertReferenceMark
second_title: Aspose.Words per .NET API Reference
description: FieldNoteRef proprietà. Inserisce il segno di riferimento con la stessa formattazione dei caratteri dello stile Riferimento nota a piè di pagina o Riferimento nota finale.
type: docs
weight: 40
url: /it/net/aspose.words.fields/fieldnoteref/insertreferencemark/
---
## FieldNoteRef.InsertReferenceMark property

Inserisce il segno di riferimento con la stessa formattazione dei caratteri dello stile Riferimento nota a piè di pagina o Riferimento nota finale.

```csharp
public bool InsertReferenceMark { get; set; }
```

### Esempi

Mostra per inserire campi NOTEREF e modificarne l'aspetto.

```csharp
public void FieldNoteRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Crea un segnalibro con una nota a piè di pagina a cui farà riferimento il campo NOTEREF.
    InsertBookmarkWithFootnote(builder, "MyBookmark1", "Contents of MyBookmark1", "Footnote from MyBookmark1");

    // Questo campo NOTEREF visualizzerà il numero della nota a piè di pagina all'interno del segnalibro di riferimento.
    // L'impostazione della proprietà InsertHyperlink ci consente di passare al segnalibro facendo Ctrl + facendo clic sul campo in Microsoft Word.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h",
        InsertFieldNoteRef(builder, "MyBookmark2", true, false, false, "Hyperlink to Bookmark2, with footnote number ").GetFieldCode());

    // Quando si utilizza il flag \p, dopo il numero della nota a piè di pagina, il campo visualizza anche la posizione del segnalibro rispetto al campo.
    // Bookmark1 si trova sopra questo campo e contiene la nota a piè di pagina numero 1, quindi il risultato sarà "1 sopra" durante l'aggiornamento.
    Assert.AreEqual(" NOTEREF  MyBookmark1 \\h \\p",
        InsertFieldNoteRef(builder, "MyBookmark1", true, true, false, "Bookmark1, with footnote number ").GetFieldCode());

    // Bookmark2 si trova sotto questo campo e contiene la nota a piè di pagina numero 2, quindi il campo visualizzerà "2 sotto".
    // Il flag \f fa apparire il numero 2 nello stesso formato dell'etichetta del numero della nota a piè di pagina nel testo effettivo.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h \\p \\f",
        InsertFieldNoteRef(builder, "MyBookmark2", true, true, true, "Bookmark2, with footnote number ").GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);
    InsertBookmarkWithFootnote(builder, "MyBookmark2", "Contents of MyBookmark2", "Footnote from MyBookmark2");

    doc.UpdatePageLayout();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.NOTEREF.docx");
}

/// <summary>
/// Utilizza un generatore di documenti per inserire un campo NOTEREF con le proprietà specificate.
/// </summary>
private static FieldNoteRef InsertFieldNoteRef(DocumentBuilder builder, string bookmarkName, bool insertHyperlink, bool insertRelativePosition, bool insertReferenceMark, string textBefore)
{
    builder.Write(textBefore);

    FieldNoteRef field = (FieldNoteRef)builder.InsertField(FieldType.FieldNoteRef, true);
    field.BookmarkName = bookmarkName;
    field.InsertHyperlink = insertHyperlink;
    field.InsertRelativePosition = insertRelativePosition;
    field.InsertReferenceMark = insertReferenceMark;
    builder.Writeln();

    return field;
}

/// <summary>
/// Utilizza un generatore di documenti per inserire un segnalibro denominato con una nota a piè di pagina alla fine.
/// </summary>
private static void InsertBookmarkWithFootnote(DocumentBuilder builder, string bookmarkName, string bookmarkText, string footnoteText)
{
    builder.StartBookmark(bookmarkName);
    builder.Write(bookmarkText);
    builder.InsertFootnote(FootnoteType.Footnote, footnoteText);
    builder.EndBookmark(bookmarkName);
    builder.Writeln();
}
```

### Guarda anche

* class [FieldNoteRef](../)
* spazio dei nomi [Aspose.Words.Fields](../../fieldnoteref/)
* assemblea [Aspose.Words](../../../)


