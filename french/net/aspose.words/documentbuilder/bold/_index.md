---
title: DocumentBuilder.Bold
linktitle: Bold
articleTitle: Bold
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Gras de DocumentBuilder. Mettez facilement vos polices en gras pour améliorer la visibilité et l'impact du texte dans vos documents. Optimisez votre design dès aujourd'hui !
type: docs
weight: 20
url: /fr/net/aspose.words/documentbuilder/bold/
---
## DocumentBuilder.Bold property

Vrai si la police est formatée en gras.

```csharp
public bool Bold { get; set; }
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
