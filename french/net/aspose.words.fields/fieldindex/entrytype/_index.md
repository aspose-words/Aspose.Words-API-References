---
title: FieldIndex.EntryType
linktitle: EntryType
articleTitle: EntryType
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FieldIndex EntryType pour gérer efficacement les types d'entrées d'index pour une indexation optimisée et des performances de recherche améliorées.
type: docs
weight: 40
url: /fr/net/aspose.words.fields/fieldindex/entrytype/
---
## FieldIndex.EntryType property

Obtient ou définit un type d'entrée d'index utilisé pour créer l'index.

```csharp
public string EntryType { get; set; }
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

### Voir également

* class [FieldIndex](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
