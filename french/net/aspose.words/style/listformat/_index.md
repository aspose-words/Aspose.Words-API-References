---
title: Style.ListFormat
linktitle: ListFormat
articleTitle: ListFormat
second_title: Aspose.Words pour .NET
description: Découvrez comment personnaliser la propriété ListFormat pour les styles de paragraphe, améliorant ainsi l'organisation et l'attrait visuel de votre document.
type: docs
weight: 110
url: /fr/net/aspose.words/style/listformat/
---
## Style.ListFormat property

Donne accès aux propriétés de formatage de liste d'un style de paragraphe.

```csharp
public ListFormat ListFormat { get; }
```

## Remarques

Cette propriété n'est valable que pour les styles de paragraphe. Pour les autres types de styles, cette propriété renvoie`nul`.

## Exemples

Montre comment créer et utiliser un style de paragraphe avec formatage de liste.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Créez un style de paragraphe personnalisé.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// Créez une liste et assurez-vous que les paragraphes qui utilisent ce style utiliseront cette liste.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// Appliquez le style de paragraphe au paragraphe actuel du générateur de documents, puis ajoutez du texte.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// Modifiez le style du générateur de documents en un style sans formatage de liste et écrivez un autre paragraphe.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

### Voir également

* class [ListFormat](../../../aspose.words.lists/listformat/)
* class [Style](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
