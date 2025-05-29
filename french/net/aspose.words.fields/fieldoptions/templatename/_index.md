---
title: FieldOptions.TemplateName
linktitle: TemplateName
articleTitle: TemplateName
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FieldOptions TemplateName pour gérer facilement le nom du fichier modèle de votre document pour une organisation et une efficacité améliorées.
type: docs
weight: 190
url: /fr/net/aspose.words.fields/fieldoptions/templatename/
---
## FieldOptions.TemplateName property

Obtient ou définit le nom de fichier du modèle utilisé par le document.

```csharp
public string TemplateName { get; set; }
```

## Remarques

Cette propriété est utilisée par le[`FieldTemplate`](../../fieldtemplate/) champ si le[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) la propriété est vide.

Si cette propriété est vide, le nom du fichier de modèle par défaut`Normal.dotm` est utilisé.

## Exemples

Montre comment utiliser un champ MODÈLE pour afficher l'emplacement du système de fichiers local du modèle d'un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nous pouvons définir un nom de modèle à l'aide des champs. Cette propriété est utilisée lorsque « doc.AttachedTemplate » est vide.
// Si cette propriété est vide, le nom de fichier de modèle par défaut « Normal.dotm » est utilisé.
doc.FieldOptions.TemplateName = string.Empty;

FieldTemplate field = (FieldTemplate)builder.InsertField(FieldType.FieldTemplate, false);
Assert.AreEqual(" TEMPLATE ", field.GetFieldCode());

builder.Writeln();
field = (FieldTemplate)builder.InsertField(FieldType.FieldTemplate, false);
field.IncludeFullPath = true;

Assert.AreEqual(" TEMPLATE  \\p", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.TEMPLATE.docx");
```

### Voir également

* class [FieldOptions](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
