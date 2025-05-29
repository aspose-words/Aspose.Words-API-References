---
title: FieldIndexFormat Enum
linktitle: FieldIndexFormat
articleTitle: FieldIndexFormat
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.FieldIndexFormat pour personnaliser le formatage FieldIndex de vos documents. Améliorez la structure de vos documents sans effort !
type: docs
weight: 2480
url: /fr/net/aspose.words.fields/fieldindexformat/
---
## FieldIndexFormat enumeration

Spécifie le formatage du[`FieldIndex`](../fieldindex/) champs dans un document.

```csharp
public enum FieldIndexFormat
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Template | `0` | À partir du modèle. |
| Classic | `1` | Classique. |
| Fancy | `2` | Fantaisie. |
| Modern | `3` | Moderne. |
| Bulleted | `4` | Puces. |
| Formal | `5` | Officiel. |
| Simple | `6` | Simple. |

## Exemples

Montre comment formater les champs FieldIndex.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("A");
builder.InsertBreak(BreakType.LineBreak);
builder.InsertField("XE \"A\"");
builder.Write("B");

builder.InsertField(" INDEX \\e \" · \" \\h \"A\" \\c \"2\" \\z \"1033\"", null);

doc.FieldOptions.FieldIndexFormat = FieldIndexFormat.Fancy;
doc.UpdateFields();

doc.Save(ArtifactsDir + "Field.SetFieldIndexFormat.docx");
```

### Voir également

* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)
