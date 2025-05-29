---
title: FieldPageRef.InsertHyperlink
linktitle: InsertHyperlink
articleTitle: InsertHyperlink
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété FieldPageRef InsertHyperlink améliore vos documents en créant facilement des liens vers des paragraphes marqués d'un signet pour une navigation fluide.
type: docs
weight: 30
url: /fr/net/aspose.words.fields/fieldpageref/inserthyperlink/
---
## FieldPageRef.InsertHyperlink property

Obtient ou définit s'il faut insérer un lien hypertexte vers le paragraphe marqué d'un signet.

```csharp
public bool InsertHyperlink { get; set; }
```

## Exemples

Affiche l'insertion de champs PAGEREF pour afficher l'emplacement relatif des signets.

```csharp
public void FieldPageRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    InsertAndNameBookmark(builder, "MyBookmark1");

    // Insérer un champ PAGEREF qui affiche sur quelle page se trouve un signet.
    // Définissez l'indicateur InsertHyperlink pour que le champ fonctionne également comme un lien cliquable vers le signet.
    Assert.AreEqual(" PAGEREF  MyBookmark3 \\h", 
        InsertFieldPageRef(builder, "MyBookmark3", true, false, "Hyperlink to Bookmark3, on page: ").GetFieldCode());

    // Nous pouvons utiliser l'indicateur \p pour obtenir le champ PAGEREF à afficher
    // la position du signet par rapport à la position du champ.
    // Le signet 1 est sur la même page et au-dessus de ce champ, donc le résultat affiché de ce champ sera « au-dessus ».
    Assert.AreEqual(" PAGEREF  MyBookmark1 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark1", true, true, "Bookmark1 is ").GetFieldCode());

    // Le signet 2 sera sur la même page et en dessous de ce champ, donc le résultat affiché de ce champ sera « en dessous ».
    Assert.AreEqual(" PAGEREF  MyBookmark2 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark2", true, true, "Bookmark2 is ").GetFieldCode());

    // Le signet 3 sera sur une page différente, le champ affichera donc « sur la page 2 ».
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
/// Utilise un générateur de documents pour insérer un champ PAGEREF et définit ses propriétés.
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
/// Utilise un générateur de documents pour insérer un signet nommé.
/// </summary>
private static void InsertAndNameBookmark(DocumentBuilder builder, string bookmarkName)
{
    builder.StartBookmark(bookmarkName);
    builder.Writeln($"Contents of bookmark \"{bookmarkName}\".");
    builder.EndBookmark(bookmarkName);
}
```

### Voir également

* class [FieldPageRef](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
