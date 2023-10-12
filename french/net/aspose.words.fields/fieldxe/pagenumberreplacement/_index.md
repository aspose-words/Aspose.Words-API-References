---
title: FieldXE.PageNumberReplacement
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldXE propriété. Obtient ou définit le texte utilisé à la place dun numéro de page.
type: docs
weight: 50
url: /fr/net/aspose.words.fields/fieldxe/pagenumberreplacement/
---
## FieldXE.PageNumberReplacement property

Obtient ou définit le texte utilisé à la place d'un numéro de page.

```csharp
public string PageNumberReplacement { get; set; }
```

### Exemples

Montre comment définir des références croisées dans un champ INDEX.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Créez un champ INDEX qui affichera une entrée pour chaque champ XE trouvé dans le document.
// Chaque entrée affichera la valeur de la propriété Text du champ XE sur le côté gauche,
// et le numéro de la page qui contient le champ XE à droite.
// L'entrée INDEX collectera tous les champs XE avec des valeurs correspondantes dans la propriété "Texte"
// en une seule entrée au lieu de créer une entrée pour chaque champ XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Nous pouvons configurer un champ XE pour que son entrée INDEX affiche une chaîne au lieu d'un numéro de page.
// Premièrement, pour les entrées qui remplacent un numéro de page par une chaîne,
// spécifie un séparateur personnalisé entre la valeur de la propriété Text du champ XE et la chaîne.
index.CrossReferenceSeparator = ", see: ";

Assert.AreEqual(" INDEX  \\k \", see: \"", index.GetFieldCode());

// Insère un champ XE, qui crée une entrée INDEX régulière qui affiche le numéro de page de ce champ,
// et n'appelle pas la valeur CrossReferenceSeparator.
// L'entrée de ce champ XE affichera "Apple, 2".
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";

Assert.AreEqual(" XE  Apple", indexEntry.GetFieldCode());

// Insérez un autre champ XE à la page 3 et définissez une valeur pour la propriété PageNumberReplacement.
// Cette valeur s'affichera à la place du numéro de la page sur laquelle se trouve ce champ,
// et la valeur CrossReferenceSeparator du champ INDEX apparaîtra devant lui.
// L'entrée de ce champ XE affichera "Banane, voir : Fruits tropicaux".
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";
indexEntry.PageNumberReplacement = "Tropical fruit";

Assert.AreEqual(" XE  Banana \\t \"Tropical fruit\"", indexEntry.GetFieldCode());

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.CrossReferenceSeparator.docx");
```

### Voir également

* class [FieldXE](../)
* espace de noms [Aspose.Words.Fields](../../fieldxe/)
* Assemblée [Aspose.Words](../../../)


