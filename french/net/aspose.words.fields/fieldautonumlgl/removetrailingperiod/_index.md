---
title: FieldAutoNumLgl.RemoveTrailingPeriod
linktitle: RemoveTrailingPeriod
articleTitle: RemoveTrailingPeriod
second_title: Aspose.Words pour .NET
description: Gérez la propriété RemoveTrailingPeriod de FieldAutoNumLgl pour personnaliser l'affichage des nombres  éliminez les points de fin pour un formatage plus propre et professionnel.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldautonumlgl/removetrailingperiod/
---
## FieldAutoNumLgl.RemoveTrailingPeriod property

Obtient ou définit s'il faut afficher le nombre sans point de fin.

```csharp
public bool RemoveTrailingPeriod { get; set; }
```

## Exemples

Montre comment organiser un document à l'aide des champs AUTONUMLGL.

```csharp
public void FieldAutoNumLgl()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    const string fillerText = "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
                              "\nUt enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. ";

    // Les champs AUTONUMLGL affichent un numéro qui s'incrémente à chaque champ AUTONUMLGL dans son niveau d'en-tête actuel.
    // Ces champs conservent un décompte distinct pour chaque niveau de titre,
     // et chaque champ affiche également le nombre de champs AUTONUMLGL pour tous les niveaux de titre inférieurs au sien.
    // La modification du nombre pour n'importe quel niveau de titre réinitialise les nombres pour tous les niveaux au-dessus de ce niveau à 1.
    // Cela nous permet d'organiser notre document sous la forme d'une liste schématique.
    // Il s'agit du premier champ AUTONUMLGL à un niveau de titre de 1, affichant « 1. » dans le document.
    InsertNumberedClause(builder, "\tHeading 1", fillerText, StyleIdentifier.Heading1);

    // Il s'agit du deuxième champ AUTONUMLGL au niveau d'en-tête 1, il affichera donc « 2 ».
    InsertNumberedClause(builder, "\tHeading 2", fillerText, StyleIdentifier.Heading1);

    // Il s'agit du premier champ AUTONUMLGL à un niveau d'en-tête de 2,
    // et le nombre AUTONUMLGL pour le niveau de titre en dessous est « 2 », il affichera donc « 2.1 ».
    InsertNumberedClause(builder, "\tHeading 3", fillerText, StyleIdentifier.Heading2);

     // Il s'agit du premier champ AUTONUMLGL à un niveau d'en-tête de 3.
    // Fonctionnant de la même manière que le champ ci-dessus, il affichera « 2.1.1. ».
    InsertNumberedClause(builder, "\tHeading 4", fillerText, StyleIdentifier.Heading3);

    // Ce champ est à un niveau d'en-tête de 2, et son nombre AUTONUMLGL respectif est à 2, donc le champ affichera « 2.2. ».
    InsertNumberedClause(builder, "\tHeading 5", fillerText, StyleIdentifier.Heading2);

    // Incrémentation du nombre AUTONUMLGL pour un niveau de titre inférieur à celui-ci
    // a réinitialisé le compteur pour ce niveau afin que ce champ affiche « 2.2.1 ».
    InsertNumberedClause(builder, "\tHeading 6", fillerText, StyleIdentifier.Heading3);

    foreach (FieldAutoNumLgl field in doc.Range.Fields.Where(f => f.Type == FieldType.FieldAutoNumLegal).ToList())
    {
        // Le caractère séparateur, qui apparaît dans le champ résultat immédiatement après le nombre,
        // est un point par défaut. Si nous laissons cette propriété nulle,
        // notre dernier champ AUTONUMLGL affichera « 2.2.1. » dans le document.
        Assert.IsNull(field.SeparatorCharacter);

        // Définition d'un caractère séparateur personnalisé et suppression du point de fin
        // changera l'apparence de ce champ de « 2.2.1. » à « 2:2:1 ».
        // Nous appliquerons ceci à tous les champs que nous avons créés.
        field.SeparatorCharacter = ":";
        field.RemoveTrailingPeriod = true;
        Assert.AreEqual(" AUTONUMLGL  \\s : \\e", field.GetFieldCode());
    }

    doc.Save(ArtifactsDir + "Field.AUTONUMLGL.docx");
}

/// <summary>
/// Utilise un générateur de documents pour insérer une clause numérotée par un champ AUTONUMLGL.
/// </summary>
private static void InsertNumberedClause(DocumentBuilder builder, string heading, string contents, StyleIdentifier headingStyle)
{
    builder.InsertField(FieldType.FieldAutoNumLegal, true);
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = headingStyle;
    builder.Writeln(heading);

    // Ce texte appartiendra au champ légal auto num au-dessus de lui.
    // Il s'effondrera lorsque nous cliquerons sur la flèche à côté du champ AUTONUMLGL correspondant dans Microsoft Word.
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = StyleIdentifier.BodyText;
    builder.Writeln(contents);
}
```

### Voir également

* class [FieldAutoNumLgl](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
