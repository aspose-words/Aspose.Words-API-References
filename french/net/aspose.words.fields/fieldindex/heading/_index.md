---
title: FieldIndex.Heading
linktitle: Heading
articleTitle: Heading
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FieldIndex Heading pour personnaliser les en-têtes d'entrée par lettre, améliorant ainsi l'organisation et l'expérience utilisateur dans votre application.
type: docs
weight: 70
url: /fr/net/aspose.words.fields/fieldindex/heading/
---
## FieldIndex.Heading property

Obtient ou définit un en-tête qui apparaît au début de chaque ensemble d'entrées pour une lettre donnée.

```csharp
public string Heading { get; set; }
```

## Exemples

Montre comment remplir un champ INDEX avec des entrées à l'aide de champs XE et également modifier son apparence.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Créez un champ INDEX qui affichera une entrée pour chaque champ XE trouvé dans le document.
// Chaque entrée affichera la valeur de la propriété Texte du champ XE sur le côté gauche,
// et le numéro de la page qui contient le champ XE à droite.
// Si les champs XE ont la même valeur dans leur propriété « Texte »,
// le champ INDEX les regroupera en une seule entrée.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.LanguageId = "1033";

// Définir la valeur de cette propriété sur « A » regroupera toutes les entrées par leur première lettre,
// et placez cette lettre en majuscule au-dessus de chaque groupe.
index.Heading = "A";

// Définissez la table créée par le champ INDEX pour qu'elle s'étende sur 2 colonnes.
index.NumberOfColumns = "2";

// Définissez toutes les entrées avec des lettres de départ en dehors de la plage de caractères « ac » à omettre.
index.LetterRange = "a-c";

Assert.AreEqual(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.GetFieldCode());

// Ces deux prochains champs XE apparaîtront sous le titre « A »,
// avec leurs styles de texte respectifs également appliqués à leurs numéros de page.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";
indexEntry.IsItalic = true;

Assert.AreEqual(" XE  Apple \\i", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apricot";
indexEntry.IsBold = true;

Assert.AreEqual(" XE  Apricot \\b", indexEntry.GetFieldCode());

// Les deux champs XE suivants seront sous un en-tête « B » et « C » dans la table des matières des champs INDEX.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cherry";

// Les champs INDEX trient toutes les entrées par ordre alphabétique, donc cette entrée apparaîtra sous « A » avec les deux autres.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Avocado";

// Cette entrée n'apparaîtra pas car elle commence par la lettre « D »,
// qui est en dehors de la plage de caractères « ac » définie par la propriété LetterRange du champ INDEX.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Durian";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Formatting.docx");
```

### Voir également

* class [FieldIndex](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
