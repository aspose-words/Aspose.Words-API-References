---
title: FieldAutoNumLgl Class
linktitle: FieldAutoNumLgl
articleTitle: FieldAutoNumLgl
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Fields.FieldAutoNumLgl pour une implémentation transparente des champs AUTONUMLGL, améliorant l'automatisation et le formatage des documents.
type: docs
weight: 2000
url: /fr/net/aspose.words.fields/fieldautonumlgl/
---
## FieldAutoNumLgl class

Implémente le champ AUTONUMLGL.

Pour en savoir plus, visitez le[Travailler avec les champs](https://docs.aspose.com/words/net/working-with-fields/) article de documentation.

```csharp
public class FieldAutoNumLgl : Field
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FieldAutoNumLgl](fieldautonumlgl/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtient le texte qui représente le résultat du champ affiché. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtient le nœud qui représente la fin du champ. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtient un[`FieldFormat`](../fieldformat/)objet qui fournit un accès typé au formatage du champ. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtient ou définit si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtient ou définit le LCID du champ. |
| [RemoveTrailingPeriod](../../aspose.words.fields/fieldautonumlgl/removetrailingperiod/) { get; set; } | Obtient ou définit s'il faut afficher le nombre sans point de fin. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtient ou définit le texte qui se trouve entre le séparateur de champ et la fin du champ. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Récupère le nœud représentant le séparateur de champ. Peut être`nul` . |
| [SeparatorCharacter](../../aspose.words.fields/fieldautonumlgl/separatorcharacter/) { get; set; } | Obtient ou définit le caractère séparateur à utiliser. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtient le nœud qui représente le début du champ. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtient le type de champ Microsoft Word. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). Le code du champ et le résultat du champ des champs enfants sont inclus. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [Remove](../../aspose.words.fields/field/remove/)() | Supprime le champ du document. Renvoie un nœud immédiatement après le champ. Si la fin du champ est le dernier child de son nœud parent, renvoie son paragraphe parent. Si le champ est déjà supprimé, renvoie`nul` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Effectue la dissociation du champ. |
| [Update](../../aspose.words.fields/field/update/)() | Effectue la mise à jour du champ. Lève une requête si le champ est déjà en cours de mise à jour. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Effectue une mise à jour du champ. L'erreur est générée si le champ est déjà en cours de mise à jour. |

## Remarques

Insère un numéro automatique au format légal.

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

* class [Field](../field/)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)
