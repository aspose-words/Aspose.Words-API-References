---
title: ListLevelCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words pour .NET
description: ListLevelCollection GetEnumerator méthode. Obtient lobjet énumérateur qui énumérera les niveaux dans cette liste en C#.
type: docs
weight: 30
url: /fr/net/aspose.words.lists/listlevelcollection/getenumerator/
---
## ListLevelCollection.GetEnumerator method

Obtient l'objet énumérateur qui énumérera les niveaux dans cette liste.

```csharp
public IEnumerator<ListLevel> GetEnumerator()
```

## Exemples

Présente des méthodes avancées de personnalisation des étiquettes de liste.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles de préfixe et des retraits.
 // Nous pouvons créer des listes imbriquées en augmentant le niveau d'indentation.
 // Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un générateur de documents.
// Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

// Les étiquettes de niveau 1 seront formatées selon le style de paragraphe "Titre 1" et auront un préfixe.
// Ceux-ci ressembleront à "Annexe A", "Annexe B"...
list.ListLevels[0].NumberFormat = "Appendix \x0000";
list.ListLevels[0].NumberStyle = NumberStyle.UppercaseLetter;
list.ListLevels[0].LinkedStyle = doc.Styles["Heading 1"];

// Les étiquettes de niveau 2 afficheront les numéros actuels des premier et deuxième niveaux de liste et auront des zéros non significatifs.
// Si le premier niveau de liste est à 1, alors les étiquettes de liste de ceux-ci ressembleront à "Section (1.01)", "Section (1.02)"...
list.ListLevels[1].NumberFormat = "Section (\x0000.\x0001)";
list.ListLevels[1].NumberStyle = NumberStyle.LeadingZero;

// Notez que le niveau supérieur utilise la numérotation UppercaseLetter.
// Nous pouvons définir la propriété "IsLegal" pour qu'elle utilise des nombres arabes pour les niveaux de liste supérieurs.
list.ListLevels[1].IsLegal = true;
list.ListLevels[1].RestartAfterLevel = 0;

// Les étiquettes de niveau 3 seront des chiffres romains majuscules avec un préfixe et un suffixe et redémarreront à chaque élément de niveau 1 de la liste.
// Ces étiquettes de liste ressembleront à "-I-", "-II-"...
list.ListLevels[2].NumberFormat = "-\x0002-";
list.ListLevels[2].NumberStyle = NumberStyle.UppercaseRoman;
list.ListLevels[2].RestartAfterLevel = 1;

// Mettez les étiquettes de tous les niveaux de liste en gras.
foreach (ListLevel level in list.ListLevels)
    level.Font.Bold = true;

// Applique le formatage de la liste au paragraphe actuel.
builder.ListFormat.List = list;

// Créez des éléments de liste qui afficheront nos trois niveaux de liste.
for (int n = 0; n < 2; n++)
{
    for (int i = 0; i < 3; i++)
    {
        builder.ListFormat.ListLevelNumber = i;
        builder.Writeln("Level " + i);
    }
}

builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.CreateListRestartAfterHigher.docx");
```

### Voir également

* class [ListLevel](../../listlevel/)
* class [ListLevelCollection](../)
* espace de noms [Aspose.Words.Lists](../../../aspose.words.lists/)
* Assemblée [Aspose.Words](../../../)
