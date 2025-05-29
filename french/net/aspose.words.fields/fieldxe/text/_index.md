---
title: FieldXE.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words pour .NET
description: Gérez facilement vos propriétés de texte FieldXE. Saisissez ou définissez facilement le texte de votre entrée pour une gestion fluide des données et une expérience utilisateur améliorée.
type: docs
weight: 70
url: /fr/net/aspose.words.fields/fieldxe/text/
---
## FieldXE.Text property

Obtient ou définit le texte de l'entrée.

```csharp
public string Text { get; set; }
```

## Exemples

Montre comment créer un champ INDEX, puis utiliser des champs XE pour le remplir avec des entrées.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Créez un champ INDEX qui affichera une entrée pour chaque champ XE trouvé dans le document.
// Chaque entrée affichera la valeur de la propriété Texte du champ XE sur le côté gauche
// et la page contenant le champ XE à droite.
// Si les champs XE ont la même valeur dans leur propriété « Texte »,
// le champ INDEX les regroupera en une seule entrée.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Configurez le champ INDEX uniquement pour afficher les champs XE qui se trouvent dans les limites
// d'un signet nommé "MainBookmark", et dont les propriétés "EntryType" ont une valeur de "A".
// Pour les champs INDEX et XE, la propriété « EntryType » utilise uniquement le premier caractère de sa valeur de chaîne.
index.BookmarkName = "MainBookmark";
index.EntryType = "A";

Assert.AreEqual(" INDEX  \\b MainBookmark \\f A", index.GetFieldCode());

// Sur une nouvelle page, démarrez le signet avec un nom qui correspond à la valeur
// de la propriété « BookmarkName » du champ INDEX.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MainBookmark");

// Le champ INDEX récupérera cette entrée car elle se trouve à l'intérieur du signet,
// et son type d'entrée correspond également au type d'entrée du champ INDEX.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 1";
indexEntry.EntryType = "A";

Assert.AreEqual(" XE  \"Index entry 1\" \\f A", indexEntry.GetFieldCode());

// Insérer un champ XE qui n'apparaîtra pas dans l'INDEX car les types d'entrée ne correspondent pas.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 2";
indexEntry.EntryType = "B";

// Terminez le signet et insérez ensuite un champ XE.
// Il est du même type que le champ INDEX, mais n'apparaîtra pas
// car il est en dehors des limites du signet.
builder.EndBookmark("MainBookmark");
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 3";
indexEntry.EntryType = "A";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Filtering.docx");
```

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

* class [FieldXE](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
