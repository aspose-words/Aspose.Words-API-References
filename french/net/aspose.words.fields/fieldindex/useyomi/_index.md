---
title: FieldIndex.UseYomi
linktitle: UseYomi
articleTitle: UseYomi
second_title: Aspose.Words pour .NET
description: Améliorez votre indexation avec la propriété UseYomi de FieldIndex. Activez facilement le texte Yomi pour une meilleure visibilité dans les recherches et une meilleure expérience utilisateur.
type: docs
weight: 170
url: /fr/net/aspose.words.fields/fieldindex/useyomi/
---
## FieldIndex.UseYomi property

Obtient ou définit s'il faut activer l'utilisation du texte Yomi pour les entrées d'index.

```csharp
public bool UseYomi { get; set; }
```

## Exemples

Montre comment trier les entrées du champ INDEX de manière phonétique.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Créez un champ INDEX qui affichera une entrée pour chaque champ XE trouvé dans le document.
// Chaque entrée affichera la valeur de la propriété Texte du champ XE sur le côté gauche,
// et le numéro de la page qui contient le champ XE à droite.
// L'entrée INDEX collectera tous les champs XE avec des valeurs correspondantes dans la propriété « Texte »
// dans une seule entrée au lieu de créer une entrée pour chaque champ XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// La table INDEX trie automatiquement ses entrées par les valeurs de leurs propriétés Text par ordre alphabétique.
// Définissez la table INDEX pour trier les entrées phonétiquement en utilisant Hiragana à la place.
index.UseYomi = sortEntriesUsingYomi;

if (sortEntriesUsingYomi)
    Assert.AreEqual(" INDEX  \\y", index.GetFieldCode());
else
    Assert.AreEqual(" INDEX ", index.GetFieldCode());

// Insérez 4 champs XE, qui apparaîtront comme des entrées dans la table des matières du champ INDEX.
// La propriété "Texte" peut contenir l'orthographe d'un mot en Kanji, dont la prononciation peut être ambiguë,
// tandis que la version « Yomi » du mot s'écrira exactement comme il est prononcé en utilisant Hiragana.
// Si nous définissons notre champ INDEX pour utiliser Yomi, il triera ces entrées
// par la valeur de leurs propriétés Yomi, au lieu de leurs valeurs de texte.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "愛子";
indexEntry.Yomi = "あ";

Assert.AreEqual(" XE  愛子 \\y あ", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "明美";
indexEntry.Yomi = "あ";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "恵美";
indexEntry.Yomi = "え";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "愛美";
indexEntry.Yomi = "え";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Yomi.docx");
```

### Voir également

* class [FieldIndex](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
