---
title: FieldFileName.IncludeFullPath
linktitle: IncludeFullPath
articleTitle: IncludeFullPath
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FieldFileName IncludeFullPath, gérez facilement les chemins de fichiers avec des paramètres personnalisables pour une gestion et une organisation améliorées des fichiers.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldfilename/includefullpath/
---
## FieldFileName.IncludeFullPath property

Obtient ou définit s'il faut inclure le nom du chemin d'accès complet au fichier.

```csharp
public bool IncludeFullPath { get; set; }
```

## Exemples

Montre comment utiliser FieldOptions pour remplacer la valeur par défaut du champ FILENAME.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToDocumentEnd();
builder.Writeln();

// Ce champ FILENAME affichera le nom du fichier système local du document que nous avons chargé.
FieldFileName field = (FieldFileName)builder.InsertField(FieldType.FieldFileName, true);
field.Update();

Assert.AreEqual(" FILENAME ", field.GetFieldCode());
Assert.AreEqual("Document.docx", field.Result);

builder.Writeln();

// Par défaut, le champ NOM DE FICHIER affiche le nom du fichier, mais pas son chemin d'accès complet au système de fichiers local.
// Nous pouvons définir un indicateur pour afficher le chemin complet du fichier.
field = (FieldFileName)builder.InsertField(FieldType.FieldFileName, true);
field.IncludeFullPath = true;
field.Update();

Assert.AreEqual(MyDir + "Document.docx", field.Result);

// Nous pouvons également définir une valeur pour cette propriété à
// remplace la valeur affichée par le champ FILENAME.
doc.FieldOptions.FileName = "FieldOptions.FILENAME.docx";
field.Update();

Assert.AreEqual(" FILENAME  \\p", field.GetFieldCode());
Assert.AreEqual("FieldOptions.FILENAME.docx", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + doc.FieldOptions.FileName);
```

### Voir également

* class [FieldFileName](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
