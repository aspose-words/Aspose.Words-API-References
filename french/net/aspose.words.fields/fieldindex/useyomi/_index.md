---
title: FieldIndex.UseYomi
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldIndex propriété. Obtient ou définit sil faut activer lutilisation du texte yomi pour les entrées dindex.
type: docs
weight: 170
url: /fr/net/aspose.words.fields/fieldindex/useyomi/
---
## FieldIndex.UseYomi property

Obtient ou définit s'il faut activer l'utilisation du texte yomi pour les entrées d'index.

```csharp
public bool UseYomi { get; set; }
```

### Exemples

Montre comment trier phonétiquement les entrées du champ INDEX.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Créez un champ INDEX qui affichera une entrée pour chaque champ XE trouvé dans le document.
// Chaque entrée affichera la valeur de la propriété Text du champ XE sur le côté gauche,
// et le numéro de la page qui contient le champ XE à droite.
// L'entrée INDEX collectera tous les champs XE avec des valeurs correspondantes dans la propriété "Texte"
// en une seule entrée au lieu de créer une entrée pour chaque champ XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// La table INDEX trie automatiquement ses entrées selon les valeurs de leurs propriétés Text par ordre alphabétique.
// Définit la table INDEX pour trier les entrées phonétiquement en utilisant Hiragana à la place.
index.UseYomi = sortEntriesUsingYomi;

if (sortEntriesUsingYomi)
    Assert.AreEqual(" INDEX  \\y", index.GetFieldCode());
else
    Assert.AreEqual(" INDEX ", index.GetFieldCode());

// Insère 4 champs XE, qui apparaîtront sous forme d'entrées dans la table des matières du champ INDEX.
// La propriété "Texte" peut contenir l'orthographe d'un mot en Kanji, dont la prononciation peut être ambiguë,
// tandis que la version "Yomi" du mot épellera exactement comment il est prononcé en utilisant Hiragana.
// Si nous définissons notre champ INDEX pour utiliser Yomi, il triera ces entrées
// par la valeur de leurs propriétés Yomi, au lieu de leurs valeurs Text.
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
* espace de noms [Aspose.Words.Fields](../../fieldindex/)
* Assemblée [Aspose.Words](../../../)


