---
title: Style.ParagraphFormat
second_title: Référence de l'API Aspose.Words pour .NET
description: Style propriété. Obtient la mise en forme du paragraphe du style.
type: docs
weight: 130
url: /fr/net/aspose.words/style/paragraphformat/
---
## Style.ParagraphFormat property

Obtient la mise en forme du paragraphe du style.

```csharp
public ParagraphFormat ParagraphFormat { get; }
```

### Remarques

Pour les styles de caractère et de liste, cette propriété renvoie null.

### Exemples

Montre comment créer et utiliser un style de paragraphe avec une mise en forme de liste.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crée un style de paragraphe personnalisé.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// Créez une liste et assurez-vous que les paragraphes qui utilisent ce style utiliseront cette liste.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// Appliquez le style de paragraphe au paragraphe actuel du générateur de document, puis ajoutez du texte.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// Modifiez le style du générateur de document en un style qui n'a pas de formatage de liste et écrivez un autre paragraphe.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

### Voir également

* class [ParagraphFormat](../../paragraphformat/)
* class [Style](../)
* espace de noms [Aspose.Words](../../style/)
* Assemblée [Aspose.Words](../../../)


