---
title: Style.ParagraphFormat
linktitle: ParagraphFormat
articleTitle: ParagraphFormat
second_title: Aspose.Words pour .NET
description: Découvrez comment accéder et personnaliser la mise en forme des paragraphes des styles pour une présentation améliorée des documents et une mise en forme professionnelle.
type: docs
weight: 150
url: /fr/net/aspose.words/style/paragraphformat/
---
## Style.ParagraphFormat property

Obtient la mise en forme du paragraphe du style.

```csharp
public ParagraphFormat ParagraphFormat { get; }
```

## Remarques

Pour les styles de caractères et de listes, cette propriété renvoie`nul`.

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

* class [ParagraphFormat](../../paragraphformat/)
* class [Style](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
