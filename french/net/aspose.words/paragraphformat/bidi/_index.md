---
title: ParagraphFormat.Bidi
second_title: Référence de l'API Aspose.Words pour .NET
description: ParagraphFormat propriété. Obtient ou définit sil sagit dun paragraphe de droite à gauche.
type: docs
weight: 50
url: /fr/net/aspose.words/paragraphformat/bidi/
---
## ParagraphFormat.Bidi property

Obtient ou définit s'il s'agit d'un paragraphe de droite à gauche.

```csharp
public bool Bidi { get; set; }
```

### Remarques

Quand`vrai`, les exécutions et autres objets en ligne dans ce paragraphe sont disposés de droite à gauche.

### Exemples

Montre comment détecter la direction du texte d'un document en texte brut.

```csharp
// Crée un objet "TxtLoadOptions", que l'on peut transmettre au constructeur d'un document
// pour modifier la façon dont nous chargeons un document en texte brut.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Définissez la propriété "DocumentDirection" sur "DocumentDirection.Auto" détecte automatiquement
// la direction de chaque paragraphe de texte chargé par Aspose.Words à partir du texte brut.
// La propriété "Bidi" de chaque paragraphe stockera sa direction.
loadOptions.DocumentDirection = DocumentDirection.Auto;

// Détecte le texte hébreu de droite à gauche.
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// Détecte le texte anglais de droite à gauche.
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

Montre comment créer des listes compatibles avec les langues de droite à gauche avec les champs BIDIOUTLINE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Le champ BIDIOUTLINE numérote les paragraphes comme les champs AUTONUM/LISTNUM,
// mais n'est visible que lorsqu'une langue d'édition de droite à gauche est activée, comme l'hébreu ou l'arabe.
// Le champ suivant affichera ".1", l'équivalent RTL du numéro de liste "1.".
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// Ajoutez deux champs BIDIOUTLINE supplémentaires, qui afficheront ".2" et ".3".
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

// Définissez l'alignement horizontal du texte pour chaque paragraphe du document sur RTL.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
{
    para.ParagraphFormat.Bidi = true;
}

// Si nous activons une langue d'édition de droite à gauche dans Microsoft Word, nos champs afficheront des chiffres.
// Sinon, ils afficheront "###".
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

### Voir également

* class [ParagraphFormat](../)
* espace de noms [Aspose.Words](../../paragraphformat/)
* Assemblée [Aspose.Words](../../../)


