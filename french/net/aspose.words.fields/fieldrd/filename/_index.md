---
title: FieldRD.FileName
linktitle: FileName
articleTitle: FileName
second_title: Aspose.Words pour .NET
description: FieldRD FileName propriété. Obtient ou définit le nom du fichier à inclure lors de la génération dune table des matières dune table de références ou dun index en C#.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldrd/filename/
---
## FieldRD.FileName property

Obtient ou définit le nom du fichier à inclure lors de la génération d'une table des matières, d'une table de références ou d'un index.

```csharp
public string FileName { get; set; }
```

## Exemples

Montre comment utiliser le champ RD pour créer une table des matières à partir des titres d'autres documents.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Utiliser un générateur de documents pour insérer une table des matières,
// puis ajoutez une entrée pour la table des matières de la page suivante.
builder.InsertField(FieldType.FieldTOC, true);
builder.InsertBreak(BreakType.PageBreak);
builder.CurrentParagraph.ParagraphFormat.StyleName = "Heading 1";
builder.Writeln("TOC entry from within this document");

// Insère un champ RD, qui fait référence à un autre document du système de fichiers local dans sa propriété FileName.
// La table des matières acceptera également désormais tous les titres du document référencé comme entrées pour sa table.
FieldRD field = (FieldRD)builder.InsertField(FieldType.FieldRefDoc, true);
field.FileName = ArtifactsDir + "ReferencedDocument.docx";

Assert.AreEqual($" RD  {ArtifactsDir.Replace(@"\",@"\\")}ReferencedDocument.docx", field.GetFieldCode());

 // Créez le document auquel le champ RD fait référence et insérez un en-tête.
// Cet en-tête apparaîtra comme une entrée dans le champ TOC de notre premier document.
Document referencedDoc = new Document();
DocumentBuilder refDocBuilder = new DocumentBuilder(referencedDoc);
refDocBuilder.CurrentParagraph.ParagraphFormat.StyleName = "Heading 1";
refDocBuilder.Writeln("TOC entry from referenced document");
referencedDoc.Save(ArtifactsDir + "ReferencedDocument.docx");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.RD.docx");
```

### Voir également

* class [FieldRD](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
