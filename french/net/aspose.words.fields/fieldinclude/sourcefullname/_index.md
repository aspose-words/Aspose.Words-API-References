---
title: FieldInclude.SourceFullName
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldInclude propriété. Obtient ou définit lemplacement du document.
type: docs
weight: 40
url: /fr/net/aspose.words.fields/fieldinclude/sourcefullname/
---
## FieldInclude.SourceFullName property

Obtient ou définit l'emplacement du document.

```csharp
public string SourceFullName { get; set; }
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


