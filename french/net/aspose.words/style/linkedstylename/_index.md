---
title: Style.LinkedStyleName
linktitle: LinkedStyleName
articleTitle: LinkedStyleName
second_title: Aspose.Words pour .NET
description: Découvrez comment styliser la propriété LinkedStyleName, gérer facilement les styles liés et améliorer votre flux de travail de conception avec une intégration transparente.
type: docs
weight: 90
url: /fr/net/aspose.words/style/linkedstylename/
---
## Style.LinkedStyleName property

Obtient/définit le nom du[`Style`](../) Lié à celui-ci. Renvoie une chaîne vide si aucun style n'est lié.

```csharp
public string LinkedStyleName { get; set; }
```

## Remarques

Il est uniquement permis de lier le style de paragraphe au style de caractère et vice versa.

La définition de LinkedStyleName pour le style actuel entraîne automatiquement la définition de LinkedStyleName pour le style lié.

L'attribution de la chaîne vide équivaut à dissocier le style précédemment lié.

## Exemples

Montre comment lier les styles entre eux.

```csharp
Document doc = new Document();

Style styleHeading1 = doc.Styles[StyleIdentifier.Heading1];

Style styleHeading1Char = doc.Styles.Add(StyleType.Character, "Heading 1 Char");
styleHeading1Char.Font.Name = "Verdana";
styleHeading1Char.Font.Bold = true;
styleHeading1Char.Font.Border.LineStyle = LineStyle.Dot;
styleHeading1Char.Font.Border.LineWidth = 15;

styleHeading1.LinkedStyleName = "Heading 1 Char";

Assert.AreEqual("Heading 1 Char", styleHeading1.LinkedStyleName);
Assert.AreEqual("Heading 1", styleHeading1Char.LinkedStyleName);
```

Montre comment utiliser les alias de style.

```csharp
Document doc = new Document(MyDir + "Style with alias.docx");

// Ce document contient un style nommé « MyStyle,MyStyle Alias 1,MyStyle Alias 2 ».
// Si le nom d'un style comporte plusieurs valeurs séparées par des virgules, chaque clause est un alias distinct.
Style style = doc.Styles["MyStyle"];
Assert.AreEqual(new [] { "MyStyle Alias 1", "MyStyle Alias 2" }, style.Aliases);
Assert.AreEqual("Title", style.BaseStyleName);
Assert.AreEqual("MyStyle Char", style.LinkedStyleName);

// Nous pouvons référencer un style en utilisant son alias, ainsi que son nom.
Assert.AreEqual(doc.Styles["MyStyle Alias 1"], doc.Styles["MyStyle Alias 2"]);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.ParagraphFormat.Style = doc.Styles["MyStyle Alias 1"];
builder.Writeln("Hello world!");
builder.ParagraphFormat.Style = doc.Styles["MyStyle Alias 2"];
builder.Write("Hello again!");

Assert.AreEqual(doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.Style, 
    doc.FirstSection.Body.Paragraphs[1].ParagraphFormat.Style);
```

### Voir également

* class [Style](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
