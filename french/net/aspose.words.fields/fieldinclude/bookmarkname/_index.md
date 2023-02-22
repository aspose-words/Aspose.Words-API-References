---
title: FieldInclude.BookmarkName
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldInclude propriété. Obtient ou définit le nom du signet dans le document à inclure.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldinclude/bookmarkname/
---
## FieldInclude.BookmarkName property

Obtient ou définit le nom du signet dans le document à inclure.

```csharp
public string BookmarkName { get; set; }
```

### Exemples

Montre comment créer un champ INCLUDE et définir ses propriétés.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nous pouvons utiliser un champ INCLUDE pour importer une partie d'un autre document dans le système de fichiers local.
// Le signet de l'autre document auquel nous faisons référence avec ce champ contient cette partie importée.
FieldInclude field = (FieldInclude)builder.InsertField(FieldType.FieldInclude, true);
field.SourceFullName = MyDir + "Bookmarks.docx";
field.BookmarkName = "MyBookmark1";
field.LockFields = false;
field.TextConverter = "Microsoft Word";

Assert.True(Regex.Match(field.GetFieldCode(), " INCLUDE .* MyBookmark1 \\\\c \"Microsoft Word\"").Success);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INCLUDE.docx");
```

### Voir également

* class [FieldInclude](../)
* espace de noms [Aspose.Words.Fields](../../fieldinclude/)
* Assemblée [Aspose.Words](../../../)


