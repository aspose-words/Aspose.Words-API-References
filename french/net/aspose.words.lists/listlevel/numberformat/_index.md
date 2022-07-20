---
title: NumberFormat
second_title: Référence de l'API Aspose.Words pour .NET
description: Renvoie ou définit le format numérique pour le niveau de liste.
type: docs
weight: 70
url: /fr/net/aspose.words.lists/listlevel/numberformat/
---
## ListLevel.NumberFormat property

Renvoie ou définit le format numérique pour le niveau de liste.

```csharp
public string NumberFormat { get; set; }
```

### Remarques

Parmi les caractères de texte normaux, la chaîne peut contenir des caractères d'espace réservé \x0000 à \x0008 représentant les numéros des niveaux de liste correspondants.

Par exemple, la chaîne "\x0000.\x0001)" générera une liste label qui ressemble à quelque chose comme "1.5)". Le nombre "1" est le nombre actuel de le 1er niveau de liste, le nombre "5" est le nombre actuel du 2ème niveau de liste.

Null n'est pas autorisé, mais une chaîne vide signifiant qu'aucun nombre n'est valide.

### Exemples

Montre comment appliquer une mise en forme de liste personnalisée aux paragraphes lors de l'utilisation de DocumentBuilder.

```csharp
Document doc = new Document();

// Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles de préfixe et des retraits.
// Nous pouvons créer des listes imbriquées en augmentant le niveau d'indentation. 
// Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un générateur de document. 
// Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
// Crée une liste à partir d'un modèle Microsoft Word et personnalise les deux premiers de ses niveaux de liste.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

ListLevel listLevel = list.ListLevels[0];
listLevel.Font.Color = Color.Red;
listLevel.Font.Size = 24;
listLevel.NumberStyle = NumberStyle.OrdinalText;
listLevel.StartAt = 21;
listLevel.NumberFormat = "\x0000";

listLevel.NumberPosition = -36;
listLevel.TextPosition = 144;
listLevel.TabPosition = 144;

listLevel = list.ListLevels[1];
listLevel.Alignment = ListLevelAlignment.Right;
listLevel.NumberStyle = NumberStyle.Bullet;
listLevel.Font.Name = "Wingdings";
listLevel.Font.Color = Color.Blue;
listLevel.Font.Size = 24;

// Cette valeur NumberFormat créera des symboles de liste à puces en forme d'étoile.
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// Créez des paragraphes et appliquez-leur les deux niveaux de liste de notre formatage de liste personnalisé.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = list;
builder.Writeln("The quick brown fox...");
builder.Writeln("The quick brown fox...");

builder.ListFormat.ListIndent();
builder.Writeln("jumped over the lazy dog.");
builder.Writeln("jumped over the lazy dog.");

builder.ListFormat.ListOutdent();
builder.Writeln("The quick brown fox...");

builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateCustomList.docx");
```

Affiche des méthodes avancées de personnalisation des étiquettes de liste.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles de préfixe et des retraits.
// Nous pouvons créer des listes imbriquées en augmentant le niveau d'indentation. 
// Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un générateur de document. 
// Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

// Les étiquettes de niveau 1 seront formatées selon le style de paragraphe "Titre 1" et auront un préfixe.
// Celles-ci ressembleront à "Appendix A", "Appendix B"...
list.ListLevels[0].NumberFormat = "Appendix \x0000";
list.ListLevels[0].NumberStyle = NumberStyle.UppercaseLetter;
list.ListLevels[0].LinkedStyle = doc.Styles["Heading 1"];

// Les étiquettes de niveau 2 afficheront les numéros actuels des premier et deuxième niveaux de liste et auront des zéros non significatifs.
// Si le premier niveau de liste est à 1, alors les étiquettes de liste de celles-ci ressembleront à "Section (1.01)", "Section (1.02)"...
list.ListLevels[1].NumberFormat = "Section (\x0000.\x0001)";
list.ListLevels[1].NumberStyle = NumberStyle.LeadingZero;

// Notez que le niveau supérieur utilise la numérotation en lettres majuscules.
// Nous pouvons définir la propriété "IsLegal" pour utiliser des chiffres arabes pour les niveaux de liste supérieurs.
list.ListLevels[1].IsLegal = true;
list.ListLevels[1].RestartAfterLevel = 0;

// Les étiquettes de niveau 3 seront des chiffres romains majuscules avec un préfixe et un suffixe et recommenceront à chaque élément de niveau 1 de la liste.
// Ces étiquettes de liste ressembleront à "-I-", "-II-"...
list.ListLevels[2].NumberFormat = "-\x0002-";
list.ListLevels[2].NumberStyle = NumberStyle.UppercaseRoman;
list.ListLevels[2].RestartAfterLevel = 1;

// Met les étiquettes de tous les niveaux de liste en gras.
foreach (ListLevel level in list.ListLevels)
    level.Font.Bold = true;

// Applique le formatage de la liste au paragraphe courant.
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

* class [ListLevel](../../listlevel)
* espace de noms [Aspose.Words.Lists](../../listlevel)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
