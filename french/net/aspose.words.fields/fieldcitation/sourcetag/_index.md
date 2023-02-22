---
title: FieldCitation.SourceTag
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldCitation propriété. Obtient ou définit une valeur qui calcule le Étiquettevaleur de lélément de la source à insérer.
type: docs
weight: 60
url: /fr/net/aspose.words.fields/fieldcitation/sourcetag/
---
## FieldCitation.SourceTag property

Obtient ou définit une valeur qui calcule le **Étiquette**valeur de l'élément de la source à insérer.

```csharp
public string SourceTag { get; set; }
```

### Exemples

Montre comment travailler avec les champs CITATION et BIBLIOGRAPHIE.

```csharp
// Ouvre un document contenant des sources bibliographiques que l'on peut trouver dans
// Microsoft Word via Références -> Citations & Bibliographie -> Gérer les sources.
Document doc = new Document(MyDir + "Bibliography.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Text to be cited with one source.");

// Crée une citation avec juste le numéro de page et l'auteur du livre référencé.
FieldCitation fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);

// Nous nous référons aux sources en utilisant leurs noms de balises.
fieldCitation.SourceTag = "Book1";
fieldCitation.PageNumber = "85";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = true;
fieldCitation.SuppressYear = true;

Assert.AreEqual(" CITATION  Book1 \\p 85 \\t \\y", fieldCitation.GetFieldCode());

// Crée une citation plus détaillée qui cite deux sources.
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

// Nous pouvons utiliser un champ BIBLIOGRAPHIE pour afficher toutes les sources dans le document.
builder.InsertBreak(BreakType.PageBreak);
FieldBibliography fieldBibliography = (FieldBibliography)builder.InsertField(FieldType.FieldBibliography, true);
fieldBibliography.FormatLanguageId = "1124";

Assert.AreEqual(" BIBLIOGRAPHY  \\l 1124", fieldBibliography.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CITATION.docx");
```

### Voir également

* class [FieldCitation](../)
* espace de noms [Aspose.Words.Fields](../../fieldcitation/)
* Assemblée [Aspose.Words](../../../)


