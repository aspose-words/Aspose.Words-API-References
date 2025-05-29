---
title: FieldToa.SequenceSeparator
linktitle: SequenceSeparator
articleTitle: SequenceSeparator
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FieldToa SequenceSeparator : personnalisez facilement la séquence de caractères pour séparer les numéros de séquence et de page pour une clarté accrue.
type: docs
weight: 90
url: /fr/net/aspose.words.fields/fieldtoa/sequenceseparator/
---
## FieldToa.SequenceSeparator property

Obtient ou définit la séquence de caractères utilisée pour séparer les numéros de séquence et les numéros de page.

```csharp
public string SequenceSeparator { get; set; }
```

## Exemples

Montre comment créer et personnaliser une table d'autorités à l'aide des champs TOA et TA.

```csharp
public void FieldTOA()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Insérer un champ TOA, qui créera une entrée pour chaque champ TA dans le document,
    // affichage des citations longues et des numéros de page pour chaque entrée.
    FieldToa fieldToa = (FieldToa)builder.InsertField(FieldType.FieldTOA, false);

    // Définissez la catégorie d'entrée de notre table. Ce TOA n'inclura désormais que les champs TA.
    // qui ont une valeur correspondante dans leur propriété EntryCategory.
    fieldToa.EntryCategory = "1";

    // De plus, la catégorie du Tableau des autorités à l'index 1 est « Cas »,
    // qui apparaîtra comme titre de notre table si nous définissons cette variable sur true.
    fieldToa.UseHeading = true;

    // Nous pouvons filtrer davantage les champs TA en nommant un signet indiquant qu'ils devront se trouver dans les limites TOA.
    fieldToa.BookmarkName = "MyBookmark";

    // Par défaut, une tabulation en pointillé sur toute la page apparaît entre la citation du champ TA
    // et son numéro de page. Nous pouvons le remplacer par n'importe quel texte ajouté à cette propriété.
    // L'insertion d'un caractère de tabulation conservera la tabulation d'origine.
    fieldToa.EntrySeparator = " \t p.";

    // Si nous avons plusieurs entrées TA qui partagent la même longue citation,
    // tous leurs numéros de page respectifs apparaîtront sur une seule ligne.
    // Nous pouvons utiliser cette propriété pour spécifier une chaîne qui séparera leurs numéros de page.
    fieldToa.PageNumberListSeparator = " & p. ";

    // Nous pouvons définir ceci sur true pour que notre table affiche le mot « passim »
    // s'il y a cinq numéros de page ou plus dans une ligne.
    fieldToa.UsePassim = true;

    // Un champ TA peut faire référence à une plage de pages.
    // Nous pouvons spécifier ici une chaîne qui apparaîtra entre les numéros de page de début et de fin pour de telles plages.
    fieldToa.PageRangeSeparator = " to ";

    // Le format des champs TA sera reporté dans notre table.
    // Nous pouvons désactiver cela en définissant l'indicateur RemoveEntryFormatting.
    fieldToa.RemoveEntryFormatting = true;
    builder.Font.Color = Color.Green;
    builder.Font.Name = "Arial Black";

    Assert.AreEqual(" TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f", fieldToa.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // Ce champ TA n'apparaîtra pas comme une entrée dans le TOA car il est en dehors
    // les limites du signet que la propriété BookmarkName du TOA spécifie.
    FieldTA fieldTA = InsertToaEntry(builder, "1", "Source 1");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 1\"", fieldTA.GetFieldCode());

    // Ce champ TA est à l'intérieur du signet,
    // mais la catégorie d'entrée ne correspond pas à celle de la table, donc le champ TA ne l'inclura pas.
    builder.StartBookmark("MyBookmark");
    fieldTA = InsertToaEntry(builder, "2", "Source 2");

    // Cette entrée apparaîtra dans le tableau.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");

    // Une table TOA n'affiche pas les citations courtes,
    // mais nous pouvons les utiliser comme raccourci pour faire référence à des noms de sources volumineux auxquels plusieurs champs TA font référence.
    fieldTA.ShortCitation = "S.3";

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\s S.3", fieldTA.GetFieldCode());

    // Nous pouvons formater le numéro de page pour le rendre en gras/italique en utilisant les propriétés suivantes.
    // Nous verrons toujours ces effets si nous configurons notre tableau pour ignorer le formatage.
    fieldTA = InsertToaEntry(builder, "1", "Source 2");
    fieldTA.IsBold = true;
    fieldTA.IsItalic = true;

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 2\" \\b \\i", fieldTA.GetFieldCode());

    // Nous pouvons configurer les champs TA pour que leurs entrées TOA fassent référence à une plage de pages sur lesquelles s'étend un signet.
    // Notez que cette entrée fait référence à la même source que celle ci-dessus pour partager une ligne dans notre tableau.
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

    // Si nous avons activé la fonctionnalité « Passim » de notre table, le fait d'avoir 5 entrées TA ou plus avec la même source l'invoquera.
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

* class [FieldToa](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
