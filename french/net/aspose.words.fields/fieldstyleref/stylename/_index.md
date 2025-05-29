---
title: FieldStyleRef.StyleName
linktitle: StyleName
articleTitle: StyleName
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FieldStyleRef StyleName pour personnaliser et formater facilement votre texte de recherche. Améliorez le style de votre projet avec flexibilité et précision.
type: docs
weight: 70
url: /fr/net/aspose.words.fields/fieldstyleref/stylename/
---
## FieldStyleRef.StyleName property

Obtient ou définit le nom du style par lequel le texte à rechercher est formaté.

```csharp
public string StyleName { get; set; }
```

## Exemples

Montre comment utiliser les champs STYLEREF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Créez une liste à l'aide d'un modèle de liste Microsoft Word.
Aspose.Words.Lists.List list = doc.Lists.Add(Aspose.Words.Lists.ListTemplate.NumberDefault);

// Cette liste générée affichera « 1.a ) ».
 // L'espace avant le crochet est un caractère non délimiteur, que nous pouvons supprimer.
list.ListLevels[0].NumberFormat = "\x0000.";
list.ListLevels[1].NumberFormat = "\x0001 )";

// Ajoutez du texte et appliquez des styles de paragraphe auxquels les champs STYLEREF feront référence.
builder.ListFormat.List = list;
builder.ListFormat.ListIndent();
builder.ParagraphFormat.Style = doc.Styles["List Paragraph"];
builder.Writeln("Item 1");
builder.ParagraphFormat.Style = doc.Styles["Quote"];
builder.Writeln("Item 2");
builder.ParagraphFormat.Style = doc.Styles["List Paragraph"];
builder.Writeln("Item 3");
builder.ListFormat.RemoveNumbers();
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// Placez un champ STYLEREF dans l'en-tête et affichez le premier texte de style « Paragraphe de liste » dans le document.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
FieldStyleRef field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";

// Placez un champ STYLEREF dans le pied de page et affichez le dernier texte.
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";
field.SearchFromBottom = true;

builder.MoveToDocumentEnd();

// Nous pouvons également utiliser les champs STYLEREF pour référencer les numéros de liste des listes.
builder.Write("\nParagraph number: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumber = true;

builder.Write("\nParagraph number, relative context: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInRelativeContext = true;

builder.Write("\nParagraph number, full context: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInFullContext = true;

builder.Write("\nParagraph number, full context, non-delimiter chars suppressed: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInFullContext = true;
field.SuppressNonDelimiters = true;

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.STYLEREF.docx");
```

### Voir également

* class [FieldStyleRef](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
