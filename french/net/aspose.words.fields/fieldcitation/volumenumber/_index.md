---
title: FieldCitation.VolumeNumber
linktitle: VolumeNumber
articleTitle: VolumeNumber
second_title: Aspose.Words pour .NET
description: Gérez vos citations sans effort avec la propriété FieldCitation VolumeNumber, vous permettant de définir ou de récupérer facilement les numéros de volume associés.
type: docs
weight: 110
url: /fr/net/aspose.words.fields/fieldcitation/volumenumber/
---
## FieldCitation.VolumeNumber property

Obtient ou définit un numéro de volume associé à la citation.

```csharp
public string VolumeNumber { get; set; }
```

## Exemples

Montre comment travailler avec les champs CITATION et BIBLIOGRAPHIE.

```csharp
// Ouvrir un document contenant des sources bibliographiques que nous pouvons trouver dans
// Microsoft Word via Références -> Citations et bibliographie -> Gérer les sources.
Document doc = new Document(MyDir + "Bibliography.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Text to be cited with one source.");

// Créez une citation avec uniquement le numéro de page et l'auteur du livre référencé.
FieldCitation fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);

// Nous faisons référence aux sources en utilisant leurs noms de balises.
fieldCitation.SourceTag = "Book1";
fieldCitation.PageNumber = "85";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = true;
fieldCitation.SuppressYear = true;

Assert.AreEqual(" CITATION  Book1 \\p 85 \\t \\y", fieldCitation.GetFieldCode());

// Créez une citation plus détaillée qui cite deux sources.
builder.InsertParagraph();
builder.Write("Text to be cited with two sources.");
fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);
fieldCitation.SourceTag = "Book1";
fieldCitation.AnotherSourceTag = "Book2";
fieldCitation.FormatLanguageId = "en-US";
fieldCitation.PageNumber = "19";
fieldCitation.Prefix = "Prefix ";
fieldCitation.Suffix = " Suffix";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = false;
fieldCitation.SuppressYear = false;
fieldCitation.VolumeNumber = "VII";

Assert.AreEqual(" CITATION  Book1 \\m Book2 \\l en-US \\p 19 \\f \"Prefix \" \\s \" Suffix\" \\v VII", fieldCitation.GetFieldCode());

// Nous pouvons utiliser un champ BIBLIOGRAPHIE pour afficher toutes les sources du document.
builder.InsertBreak(BreakType.PageBreak);
FieldBibliography fieldBibliography = (FieldBibliography)builder.InsertField(FieldType.FieldBibliography, true);
fieldBibliography.FormatLanguageId = "5129";
fieldBibliography.FilterLanguageId = "5129";
fieldBibliography.SourceTag = "Book2";

Assert.AreEqual(" BIBLIOGRAPHY  \\l 5129 \\f 5129 \\m Book2", fieldBibliography.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CITATION.docx");
```

### Voir également

* class [FieldCitation](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
