---
title: FieldNoteRef.InsertReferenceMark
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldNoteRef propriété. Insère la marque de référence avec le même format de caractères que le style Footnote Reference ou Endnote Reference.
type: docs
weight: 40
url: /fr/net/aspose.words.fields/fieldnoteref/insertreferencemark/
---
## FieldNoteRef.InsertReferenceMark property

Insère la marque de référence avec le même format de caractères que le style Footnote Reference ou Endnote Reference.

```csharp
public bool InsertReferenceMark { get; set; }
```

### Exemples

Montre pour insérer des champs NOTEREF et modifier leur apparence.

```csharp
public void FieldNoteRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Créez un signet avec une note de bas de page que le champ NOTEREF référencera.
    InsertBookmarkWithFootnote(builder, "MyBookmark1", "Contents of MyBookmark1", "Footnote from MyBookmark1");

    // Ce champ NOTEREF affichera le numéro de la note de bas de page à l'intérieur du signet référencé.
    // La définition de la propriété InsertHyperlink nous permet d'accéder au signet en Ctrl + cliquant sur le champ dans Microsoft Word.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h",
        InsertFieldNoteRef(builder, "MyBookmark2", true, false, false, "Hyperlink to Bookmark2, with footnote number ").GetFieldCode());

    // Lors de l'utilisation de l'indicateur \p, après le numéro de note de bas de page, le champ affiche également la position du signet par rapport au champ.
    // Bookmark1 est au-dessus de ce champ et contient la note de bas de page numéro 1, le résultat sera donc "1 au-dessus" lors de la mise à jour.
    Assert.AreEqual(" NOTEREF  MyBookmark1 \\h \\p",
        InsertFieldNoteRef(builder, "MyBookmark1", true, true, false, "Bookmark1, with footnote number ").GetFieldCode());

    // Bookmark2 se trouve en dessous de ce champ et contient la note de bas de page numéro 2, le champ affichera donc "2 ci-dessous".
    // L'indicateur \f fait apparaître le chiffre 2 dans le même format que l'étiquette du numéro de note de bas de page dans le texte réel.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h \\p \\f",
        InsertFieldNoteRef(builder, "MyBookmark2", true, true, true, "Bookmark2, with footnote number ").GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);
    InsertBookmarkWithFootnote(builder, "MyBookmark2", "Contents of MyBookmark2", "Footnote from MyBookmark2");

    doc.UpdatePageLayout();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.NOTEREF.docx");
}

/// <summary>
/// Utilise un générateur de documents pour insérer un champ NOTEREF avec les propriétés spécifiées.
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
/// Utilise un générateur de documents pour insérer un signet nommé avec une note de bas de page à la fin.
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

### Voir également

* class [FieldNoteRef](../)
* espace de noms [Aspose.Words.Fields](../../fieldnoteref/)
* Assemblée [Aspose.Words](../../../)


