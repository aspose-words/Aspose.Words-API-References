---
title: FieldXE.PageRangeBookmarkName
linktitle: PageRangeBookmarkName
articleTitle: PageRangeBookmarkName
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FieldXE PageRangeBookmarkName  gérez efficacement les noms de signets pour un suivi précis de la plage de pages dans vos documents.
type: docs
weight: 60
url: /fr/net/aspose.words.fields/fieldxe/pagerangebookmarkname/
---
## FieldXE.PageRangeBookmarkName property

Obtient ou définit le nom du signet qui marque une plage de pages qui est insérée comme numéro de page de l'entrée.

```csharp
public string PageRangeBookmarkName { get; set; }
```

## Exemples

Montre comment spécifier les pages étendues d'un signet comme plage de pages pour une entrée de champ INDEX.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Créez un champ INDEX qui affichera une entrée pour chaque champ XE trouvé dans le document.
// Chaque entrée affichera la valeur de la propriété Texte du champ XE sur le côté gauche,
// et le numéro de la page qui contient le champ XE à droite.
// L'entrée INDEX collectera tous les champs XE avec des valeurs correspondantes dans la propriété « Texte »
// dans une seule entrée au lieu de créer une entrée pour chaque champ XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Pour les entrées INDEX qui affichent des plages de pages, nous pouvons spécifier une chaîne de séparation
// qui apparaîtra entre le numéro de la première page, et le numéro de la dernière.
index.PageNumberSeparator = ", on page(s) ";
index.PageRangeSeparator = " to ";

Assert.AreEqual(" INDEX  \\e \", on page(s) \" \\g \" to \"", index.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "My entry";

// Si un champ XE nomme un signet à l'aide de la propriété PageRangeBookmarkName,
// son entrée INDEX affichera la plage de pages couverte par le signet
// au lieu du numéro de la page qui contient le champ XE.
indexEntry.PageRangeBookmarkName = "MyBookmark";

Assert.AreEqual(" XE  \"My entry\" \\r MyBookmark", indexEntry.GetFieldCode());
Assert.AreEqual("MyBookmark", indexEntry.PageRangeBookmarkName);

// Insérer un signet qui commence à la page 3 et se termine à la page 5.
// L'entrée INDEX pour le champ XE qui fait référence à ce signet affichera cette plage de pages.
// Dans notre tableau, l'entrée INDEX affichera « Mon entrée, sur les pages 3 à 5 ».
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MyBookmark");
builder.Write("Start of MyBookmark");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);
builder.Write("End of MyBookmark");
builder.EndBookmark("MyBookmark");

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.PageRangeBookmark.docx");
```

### Voir également

* class [FieldXE](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
