---
title: FieldRD.IsPathRelative
linktitle: IsPathRelative
articleTitle: IsPathRelative
second_title: Aspose.Words pour .NET
description: Découvrez la propriété IsPathRelative de FieldRD pour gérer facilement les chemins d'accès aux documents. Simplifiez votre codage grâce à des paramètres de chemin flexibles pour une efficacité accrue !
type: docs
weight: 30
url: /fr/net/aspose.words.fields/fieldrd/ispathrelative/
---
## FieldRD.IsPathRelative property

Obtient ou définit si le chemin est relatif au document actuel.

```csharp
public bool IsPathRelative { get; set; }
```

## Exemples

Montre comment utiliser le champ RD pour créer des entrées de table des matières à partir de titres dans d'autres documents.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Utilisez un générateur de documents pour insérer une table des matières,
// puis ajoutez une entrée pour la table des matières sur la page suivante.
builder.InsertField(FieldType.FieldTOC, true);
builder.InsertBreak(BreakType.PageBreak);
builder.CurrentParagraph.ParagraphFormat.StyleName = "Heading 1";
builder.Writeln("TOC entry from within this document");

// Insérer un champ RD, qui fait référence à un autre document du système de fichiers local dans sa propriété FileName.
// La table des matières acceptera désormais également tous les titres du document référencé comme entrées pour sa table.
FieldRD field = (FieldRD)builder.InsertField(FieldType.FieldRefDoc, true);
field.FileName = ArtifactsDir + "ReferencedDocument.docx";

Assert.AreEqual($" RD  {ArtifactsDir.Replace(@"\",@"\\")}ReferencedDocument.docx", field.GetFieldCode());

 // Créez le document auquel le champ RD fait référence et insérez un en-tête.
// Ce titre apparaîtra comme une entrée dans le champ TOC de notre premier document.
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
