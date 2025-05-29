---
title: DocumentBuilder.Italic
linktitle: Italic
articleTitle: Italic
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Italique de DocumentBuilder. Formatez facilement votre texte en italique pour une meilleure lisibilité et un meilleur style dans vos documents.
type: docs
weight: 140
url: /fr/net/aspose.words/documentbuilder/italic/
---
## DocumentBuilder.Italic property

Vrai si la police est formatée en italique.

```csharp
public bool Italic { get; set; }
```

## Exemples

Montre comment remplir les MERGEFIELD avec des données avec un générateur de documents au lieu d'un publipostage.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer des MERGEFIELDS, qui acceptent les données des colonnes du même nom dans une source de données lors d'un publipostage,
// puis remplissez-les manuellement.
builder.InsertField(" MERGEFIELD Chairman ");
builder.InsertField(" MERGEFIELD ChiefFinancialOfficer ");
builder.InsertField(" MERGEFIELD ChiefTechnologyOfficer ");

builder.MoveToMergeField("Chairman");
builder.Bold = true;
builder.Writeln("John Doe");

builder.MoveToMergeField("ChiefFinancialOfficer");
builder.Italic = true;
builder.Writeln("Jane Doe");

builder.MoveToMergeField("ChiefTechnologyOfficer");
builder.Italic = true;
builder.Writeln("John Bloggs");

doc.Save(ArtifactsDir + "DocumentBuilder.FillMergeFields.docx");
```

### Voir également

* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
