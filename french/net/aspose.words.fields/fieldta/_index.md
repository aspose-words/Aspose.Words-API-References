---
title: Class FieldTA
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Fields.FieldTA classe. Implémente le champ TA.
type: docs
weight: 2470
url: /fr/net/aspose.words.fields/fieldta/
---
## FieldTA class

Implémente le champ TA.

Pour en savoir plus, visitez le[Travailler avec des champs](https://docs.aspose.com/words/net/working-with-fields/) article documentaire.

```csharp
public class FieldTA : Field
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FieldTA](fieldta/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtient le texte qui représente le résultat du champ affiché. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtient le nœud qui représente la fin du champ. |
| [EntryCategory](../../aspose.words.fields/fieldta/entrycategory/) { get; set; } | Obtient ou définit la catégorie d'entrée intégrale, qui est un nombre qui correspond à l'ordre des catégories . |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtient un[`FieldFormat`](../fieldformat/) objet qui fournit un accès typé au formatage du champ. |
| [IsBold](../../aspose.words.fields/fieldta/isbold/) { get; set; } | Obtient ou définit s'il faut appliquer une mise en forme en gras au numéro de page de l'entrée. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtient ou définit si le résultat actuel du champ n'est plus correct (périmé) en raison d'autres modifications apportées au document. |
| [IsItalic](../../aspose.words.fields/fieldta/isitalic/) { get; set; } | Obtient ou définit s'il faut appliquer la mise en forme en italique au numéro de page de l'entrée. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtient ou définit le LCID du champ. |
| [LongCitation](../../aspose.words.fields/fieldta/longcitation/) { get; set; } | Obtient ou définit la citation longue de l'entrée. |
| [PageRangeBookmarkName](../../aspose.words.fields/fieldta/pagerangebookmarkname/) { get; set; } | Obtient ou définit le nom du signet qui marque une plage de pages insérée comme numéro de page de l'entrée. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtient ou définit le texte situé entre le séparateur de champ et la fin du champ. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtient le nœud qui représente le séparateur de champ. Peut être`nul` . |
| [ShortCitation](../../aspose.words.fields/fieldta/shortcitation/) { get; set; } | Obtient ou définit la courte citation de l'entrée. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtient le nœud qui représente le début du champ. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtient le type de champ Microsoft Word. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). Le code de champ et le résultat du champ des champs enfants sont inclus. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [Remove](../../aspose.words.fields/field/remove/)() | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier child de son nœud parent, renvoie son paragraphe parent. Si le champ est déjà supprimé, renvoie`nul` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Effectue la dissociation du champ. |
| [Update](../../aspose.words.fields/field/update/)() | Effectue la mise à jour du champ. Lance si le champ est déjà mis à jour. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Effectue une mise à jour du champ. Lance si le champ est déjà mis à jour. |

### Remarques

Définit le texte et le numéro de page d'une entrée de table de références, qui est utilisée par un champ TOA.

### Exemples

Montre comment créer et personnaliser une table de autorités à l’aide des champs TOA et TA.

```csharp
public void FieldTOA()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Insère un champ TOA, qui créera une entrée pour chaque champ TA du document,
    // affichant de longues citations et des numéros de page pour chaque entrée.
    FieldToa fieldToa = (FieldToa)builder.InsertField(FieldType.FieldTOA, false);

    // Définit la catégorie d'entrée pour notre table. Ce TOA n'inclura désormais que les champs TA
    // qui ont une valeur correspondante dans leur propriété EntryCategory.
    fieldToa.EntryCategory = "1";

    // De plus, la catégorie Table of Authorities à l'index 1 est "Cas",
    // qui apparaîtra comme titre de notre table si nous définissons cette variable sur true.
    fieldToa.UseHeading = true;

    // Nous pouvons filtrer davantage les champs TA en nommant un signet dont ils devront se trouver dans les limites du TOA.
    fieldToa.BookmarkName = "MyBookmark";

    // Par défaut, un onglet en pointillé sur toute la page apparaît entre la citation du champ TA
    // et son numéro de page. Nous pouvons le remplacer par n'importe quel texte que nous mettons sur cette propriété.
    // L'insertion d'un caractère de tabulation conservera la tabulation d'origine.
    fieldToa.EntrySeparator = " \t p.";

    // Si nous avons plusieurs entrées TA partageant la même longue citation,
    // tous leurs numéros de page respectifs apparaîtront sur une seule ligne.
    // Nous pouvons utiliser cette propriété pour spécifier une chaîne qui séparera leurs numéros de page.
    fieldToa.PageNumberListSeparator = " & p. ";

    // Nous pouvons définir cela sur true pour que notre table affiche le mot "passim"
    // s'il y a cinq numéros de page ou plus sur une ligne.
    fieldToa.UsePassim = true;

    // Un champ TA peut faire référence à une plage de pages.
    // Nous pouvons spécifier ici une chaîne qui apparaîtra entre les numéros de page de début et de fin pour ces plages.
    fieldToa.PageRangeSeparator = " to ";

    // Le format des champs TA sera reporté dans notre table.
    // Nous pouvons désactiver cela en définissant l'indicateur RemoveEntryFormatting.
    fieldToa.RemoveEntryFormatting = true;
    builder.Font.Color = Color.Green;
    builder.Font.Name = "Arial Black";

    Assert.AreEqual(" TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f", fieldToa.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // Ce champ TA n'apparaîtra pas comme une entrée dans le TOA puisqu'il est en dehors
    // les limites du signet spécifiées par la propriété BookmarkName du TOA.
    FieldTA fieldTA = InsertToaEntry(builder, "1", "Source 1");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 1\"", fieldTA.GetFieldCode());

    // Ce champ TA est à l'intérieur du signet,
    // mais la catégorie de l'entrée ne correspond pas à celle de la table, donc le champ TA ne l'inclura pas.
    builder.StartBookmark("MyBookmark");
    fieldTA = InsertToaEntry(builder, "2", "Source 2");

    // Cette entrée apparaîtra dans le tableau.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");

    // Un tableau TOA n'affiche pas les citations courtes,
    // mais nous pouvons les utiliser comme raccourci pour faire référence à des noms de sources volumineux référencés par plusieurs champs TA.
    fieldTA.ShortCitation = "S.3";

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\s S.3", fieldTA.GetFieldCode());

    // Nous pouvons formater le numéro de page pour le mettre en gras/italique en utilisant les propriétés suivantes.
    // Nous verrons toujours ces effets si nous configurons notre table pour qu'elle ignore le formatage.
    fieldTA = InsertToaEntry(builder, "1", "Source 2");
    fieldTA.IsBold = true;
    fieldTA.IsItalic = true;

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 2\" \\b \\i", fieldTA.GetFieldCode());

    // Nous pouvons configurer les champs TA pour que leurs entrées TOA fassent référence à une plage de pages traversées par un signet.
    // Notez que cette entrée fait référence à la même source que celle ci-dessus pour partager une ligne de notre tableau.
    // Cette ligne aura le numéro de page de l'entrée ci-dessus et la plage de pages de cette entrée,
    // avec la liste des pages du tableau et les séparateurs de plage de numéros de page entre les numéros de page.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");
    fieldTA.PageRangeBookmarkName = "MyMultiPageBookmark";

    builder.StartBookmark("MyMultiPageBookmark");
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.EndBookmark("MyMultiPageBookmark");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark", fieldTA.GetFieldCode());

    // Si nous avons activé la fonctionnalité "Passim" de notre table, avoir 5 entrées TA ou plus avec la même source l'invoquera.
    for (int i = 0; i < 5; i++)
    {
        InsertToaEntry(builder, "1", "Source 4");
    }

    builder.EndBookmark("MyBookmark");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOA.TA.docx");
}

private static FieldTA InsertToaEntry(DocumentBuilder builder, string entryCategory, string longCitation)
{
    FieldTA field = (FieldTA)builder.InsertField(FieldType.FieldTOAEntry, false);
    field.EntryCategory = entryCategory;
    field.LongCitation = longCitation;

    builder.InsertBreak(BreakType.PageBreak);

    return field;
}
```

### Voir également

* class [Field](../field/)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)


