---
title: LockFields
second_title: Référence de l'API Aspose.Words pour .NET
description: Obtient ou définit sil faut empêcher la mise à jour des champs du document inclus.
type: docs
weight: 30
url: /fr/net/aspose.words.fields/fieldinclude/lockfields/
---
## FieldInclude.LockFields property

Obtient ou définit s'il faut empêcher la mise à jour des champs du document inclus.

```csharp
public bool LockFields { get; set; }
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

* class [FieldInclude](../../fieldinclude)
* espace de noms [Aspose.Words.Fields](../../fieldinclude)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
