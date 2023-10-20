---
title: FieldAutoNumLgl.SeparatorCharacter
linktitle: SeparatorCharacter
articleTitle: SeparatorCharacter
second_title: Aspose.Words pour .NET
description: FieldAutoNumLgl SeparatorCharacter propriété. Obtient ou définit le caractère séparateur à utiliser en C#.
type: docs
weight: 30
url: /fr/net/aspose.words.fields/fieldautonumlgl/separatorcharacter/
---
## FieldAutoNumLgl.SeparatorCharacter property

Obtient ou définit le caractère séparateur à utiliser.

```csharp
public string SeparatorCharacter { get; set; }
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

    // Les champs AUTONUMLGL affichent un nombre qui s'incrémente à chaque champ AUTONUMLGL dans son niveau d'en-tête actuel.
    // Ces champs maintiennent un décompte distinct pour chaque niveau de titre,
     // et chaque champ affiche également le nombre de champs AUTONUMLGL pour tous les niveaux de titre inférieurs au sien.
    // La modification du décompte pour n'importe quel niveau de titre réinitialise les décomptes de tous les niveaux supérieurs à ce niveau à 1.
    // Cela nous permet d'organiser notre document sous la forme d'une liste hiérarchique.
    // Il s'agit du premier champ AUTONUMLGL à un niveau d'en-tête de 1, affichant "1". dans le document.
    InsertNumberedClause(builder, "\tHeading 1", fillerText, StyleIdentifier.Heading1);

    // Il s'agit du deuxième champ AUTONUMLGL avec un niveau d'en-tête de 1, il affichera donc "2".
    InsertNumberedClause(builder, "\tHeading 2", fillerText, StyleIdentifier.Heading1);

    // Il s'agit du premier champ AUTONUMLGL au niveau de rubrique 2,
    // et le nombre AUTONUMLGL pour le niveau de titre en dessous est "2", il affichera donc "2.1.".
    InsertNumberedClause(builder, "\tHeading 3", fillerText, StyleIdentifier.Heading2);

     // Il s'agit du premier champ AUTONUMLGL à un niveau d'en-tête de 3.
    // Fonctionnant de la même manière que le champ ci-dessus, il affichera "2.1.1.".
    InsertNumberedClause(builder, "\tHeading 4", fillerText, StyleIdentifier.Heading3);

    // Ce champ est au niveau d'en-tête de 2, et son compte AUTONUMLGL respectif est à 2, donc le champ affichera "2.2.".
    InsertNumberedClause(builder, "\tHeading 5", fillerText, StyleIdentifier.Heading2);

    // Incrémentation du compte AUTONUMLGL pour un niveau de titre inférieur à celui-ci
    // a réinitialisé le décompte pour ce niveau afin que ce champ affiche "2.2.1.".
    InsertNumberedClause(builder, "\tHeading 6", fillerText, StyleIdentifier.Heading3);

    foreach (FieldAutoNumLgl field in doc.Range.Fields.Where(f => f.Type == FieldType.FieldAutoNumLegal))
    {
        // Le caractère séparateur, qui apparaît dans le champ résultat immédiatement après le nombre,
        // est un point par défaut. Si nous laissons cette propriété nulle,
        // notre dernier champ AUTONUMLGL affichera "2.2.1." dans le document.
        Assert.IsNull(field.SeparatorCharacter);

        // Définition d'un caractère séparateur personnalisé et suppression du point final
        // changera l'apparence de ce champ de "2.2.1." à "2:2:1".
        // Nous appliquerons cela à tous les champs que nous avons créés.
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

    // Ce texte appartiendra au champ légal auto num au-dessus.
    // Il s'effondrera lorsque nous cliquons sur la flèche à côté du champ AUTONUMLGL correspondant dans Microsoft Word.
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = StyleIdentifier.BodyText;
    builder.Writeln(contents);
}
```

### Voir également

* class [FieldAutoNumLgl](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
