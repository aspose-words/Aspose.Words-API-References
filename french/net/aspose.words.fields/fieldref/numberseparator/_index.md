---
title: FieldRef.NumberSeparator
linktitle: NumberSeparator
articleTitle: NumberSeparator
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FieldRef NumberSeparator pour personnaliser facilement la mise en forme des numéros de séquence et de page avec votre séquence de caractères préférée.
type: docs
weight: 90
url: /fr/net/aspose.words.fields/fieldref/numberseparator/
---
## FieldRef.NumberSeparator property

Obtient ou définit la séquence de caractères utilisée pour séparer les numéros de séquence et les numéros de page.

```csharp
public string NumberSeparator { get; set; }
```

## Exemples

Montre comment insérer des champs REF pour référencer des signets.

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

    // Nous appliquerons un format de liste personnalisé, où le nombre de crochets angulaires indique le niveau de liste auquel nous nous trouvons actuellement.
    builder.ListFormat.ApplyNumberDefault();
    builder.ListFormat.ListLevel.NumberFormat = "> \x0000";

    // Insérez un champ REF qui contiendra le texte dans notre signet, agira comme un lien hypertexte et clonera les notes de bas de page du signet.
    FieldRef field = InsertFieldRef(builder, "MyBookmark", "", "\n");
    field.IncludeNoteOrComment = true;
    field.InsertHyperlink = true;

    Assert.AreEqual(" REF  MyBookmark \\f \\h", field.GetFieldCode());

    // Insérer un champ REF et afficher si le signet référencé est au-dessus ou en dessous.
    field = InsertFieldRef(builder, "MyBookmark", "The referenced paragraph is ", " this field.\n");
    field.InsertRelativePosition = true;

    Assert.AreEqual(" REF  MyBookmark \\p", field.GetFieldCode());

    // Affiche le numéro de liste du signet tel qu'il apparaît dans le document.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number is ", "\n");
    field.InsertParagraphNumber = true;

    Assert.AreEqual(" REF  MyBookmark \\n", field.GetFieldCode());

    // Affiche le numéro de liste du signet, mais avec les caractères non délimiteurs, tels que les chevrons, omis.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number, non-delimiters suppressed, is ", "\n");
    field.InsertParagraphNumber = true;
    field.SuppressNonDelimiters = true;

    Assert.AreEqual(" REF  MyBookmark \\n \\t", field.GetFieldCode());

    // Descendre d'un niveau de liste.
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">> \x0001";

    // Affiche le numéro de liste du signet et les numéros de tous les niveaux de liste au-dessus.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's full context paragraph number is ", "\n");
    field.InsertParagraphNumberInFullContext = true;

    Assert.AreEqual(" REF  MyBookmark \\w", field.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // Affiche les numéros de niveau de liste entre ce champ REF et le signet auquel il fait référence.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's relative paragraph number is ", "\n");
    field.InsertParagraphNumberInRelativeContext = true;

    Assert.AreEqual(" REF  MyBookmark \\r", field.GetFieldCode());

    // À la fin du document, le signet apparaîtra comme un élément de liste ici.
    builder.Writeln("List level above bookmark");
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">>> \x0002";

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.REF.docx");
}

/// <summary>
/// Demandez au générateur de documents d'insérer un champ REF, de référencer un signet avec celui-ci et d'ajouter du texte avant et après celui-ci.
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

### Voir également

* class [FieldRef](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
