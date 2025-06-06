---
title: FieldNoteRef.InsertRelativePosition
linktitle: InsertRelativePosition
articleTitle: InsertRelativePosition
second_title: Aspose.Words pour .NET
description: Découvrez la propriété InsertRelativePosition de FieldNoteRef. Gérez facilement les paragraphes marqués d'un signet en définissant des positions relatives pour une navigation optimisée dans le document.
type: docs
weight: 50
url: /fr/net/aspose.words.fields/fieldnoteref/insertrelativeposition/
---
## FieldNoteRef.InsertRelativePosition property

Obtient ou définit s'il faut insérer une position relative du paragraphe marqué d'un signet.

```csharp
public bool InsertRelativePosition { get; set; }
```

## Exemples

Montre comment insérer des champs NOTEREF et modifier leur apparence.

```csharp
public void FieldNoteRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Créez un signet avec une note de bas de page à laquelle le champ NOTEREF fera référence.
    InsertBookmarkWithFootnote(builder, "MyBookmark1", "Contents of MyBookmark1", "Footnote from MyBookmark1");

    // Ce champ NOTEREF affichera le numéro de la note de bas de page à l'intérieur du signet référencé.
    // La définition de la propriété InsertHyperlink nous permet d'accéder au signet en appuyant sur Ctrl + en cliquant sur le champ dans Microsoft Word.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h",
        InsertFieldNoteRef(builder, "MyBookmark2", true, false, false, "Hyperlink to Bookmark2, with footnote number ").GetFieldCode());

    // Lorsque vous utilisez l'indicateur \p, après le numéro de note de bas de page, le champ affiche également la position du signet par rapport au champ.
    // Bookmark1 est au-dessus de ce champ et contient la note de bas de page numéro 1, donc le résultat sera « 1 au-dessus » lors de la mise à jour.
    Assert.AreEqual(" NOTEREF  MyBookmark1 \\h \\p",
        InsertFieldNoteRef(builder, "MyBookmark1", true, true, false, "Bookmark1, with footnote number ").GetFieldCode());

    // Le signet 2 se trouve sous ce champ et contient la note de bas de page numéro 2, le champ affichera donc « 2 ci-dessous ».
    // L'indicateur \f fait apparaître le numéro 2 dans le même format que l'étiquette du numéro de note de bas de page dans le texte réel.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h \\p \\f",
        InsertFieldNoteRef(builder, "MyBookmark2", true, true, true, "Bookmark2, with footnote number ").GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);
    InsertBookmarkWithFootnote(builder, "MyBookmark2", "Contents of MyBookmark2", "Footnote from MyBookmark2");

    doc.UpdatePageLayout();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.NOTEREF.docx");
}

/// <summary>
/// Utilise un générateur de documents pour insérer un champ NOTEREF avec des propriétés spécifiées.
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
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
