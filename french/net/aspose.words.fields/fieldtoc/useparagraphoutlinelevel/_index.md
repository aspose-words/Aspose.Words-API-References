---
title: FieldToc.UseParagraphOutlineLevel
linktitle: UseParagraphOutlineLevel
articleTitle: UseParagraphOutlineLevel
second_title: Aspose.Words pour .NET
description: Découvrez comment utiliser la propriété FieldToc UseParagraphOutlineLevel pour améliorer l'organisation des documents en définissant efficacement les niveaux de plan de paragraphe.
type: docs
weight: 170
url: /fr/net/aspose.words.fields/fieldtoc/useparagraphoutlinelevel/
---
## FieldToc.UseParagraphOutlineLevel property

Obtient ou définit s'il faut utiliser le niveau de plan de paragraphe appliqué.

```csharp
public bool UseParagraphOutlineLevel { get; set; }
```

## Exemples

Montre comment insérer une table des matières et la remplir avec des entrées basées sur des styles de titre.

```csharp
public void FieldToc()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");

    // Insérez un champ TOC, qui compilera tous les titres dans une table des matières.
    // Pour chaque titre, ce champ créera une ligne avec le texte dans ce style de titre à gauche,
    // et la page sur laquelle le titre apparaît à droite.
    FieldToc field = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Utilisez la propriété BookmarkName pour répertorier uniquement les titres
    // qui apparaissent dans les limites d'un signet portant le nom « MyBookmark ».
    field.BookmarkName = "MyBookmark";

    // Le texte avec un style de titre intégré, tel que « Titre 1 », qui lui est appliqué sera considéré comme un titre.
    // Nous pouvons nommer des styles supplémentaires à récupérer comme titres par la table des matières dans cette propriété et leurs niveaux de table des matières.
    field.CustomStyles = "Quote; 6; Intense Quote; 7";

    // Par défaut, les niveaux Styles/TOC sont séparés dans la propriété CustomStyles par une virgule,
    // mais nous pouvons définir un délimiteur personnalisé dans cette propriété.
    doc.FieldOptions.CustomTocStyleSeparator = ";";

    // Configurez le champ pour exclure tous les titres dont les niveaux de table des matières sont en dehors de cette plage.
    field.HeadingLevelRange = "1-3";

    // La table des matières n'affichera pas les numéros de page des titres dont les niveaux de table des matières se situent dans cette plage.
    field.PageNumberOmittingLevelRange = "2-5";

     // Définissez une chaîne personnalisée qui séparera chaque titre de son numéro de page.
    field.EntrySeparator = "-";
    field.InsertHyperlinks = true;
    field.HideInWebLayout = false;
    field.PreserveLineBreaks = true;
    field.PreserveTabs = true;
    field.UseParagraphOutlineLevel = false;

    InsertNewPageWithHeading(builder, "First entry", "Heading 1");
    builder.Writeln("Paragraph text.");
    InsertNewPageWithHeading(builder, "Second entry", "Heading 1");
    InsertNewPageWithHeading(builder, "Third entry", "Quote");
    InsertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

    // Ces deux titres auront les numéros de page omis car ils sont compris dans la plage « 2-5 ».
    InsertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
    InsertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

    // Cette entrée n'apparaît pas car « Titre 4 » est en dehors de la plage « 1-3 » que nous avons définie précédemment.
    InsertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

    builder.EndBookmark("MyBookmark");
    builder.Writeln("Paragraph text.");

    // Cette entrée n'apparaît pas car elle se trouve en dehors du signet spécifié par la table des matières.
    InsertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

    Assert.AreEqual(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.GetFieldCode());

    field.UpdatePageNumbers();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOC.docx");
}

/// <summary>
/// Démarrez une nouvelle page et insérez un paragraphe d'un style spécifié.
/// </summary>
public void InsertNewPageWithHeading(DocumentBuilder builder, string captionText, string styleName)
{
    builder.InsertBreak(BreakType.PageBreak);
    string originalStyle = builder.ParagraphFormat.StyleName;
    builder.ParagraphFormat.Style = builder.Document.Styles[styleName];
    builder.Writeln(captionText);
    builder.ParagraphFormat.Style = builder.Document.Styles[originalStyle];
}
```

### Voir également

* class [FieldToc](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
