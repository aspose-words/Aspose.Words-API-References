---
title: Style.Equals
linktitle: Equals
articleTitle: Equals
second_title: Aspose.Words pour .NET
description: Découvrez la méthode « Style Equals » pour comparer les styles intégrés. Comprendre les styles de paragraphes liés et suivants pour une mise en forme et une conception optimisées.
type: docs
weight: 220
url: /fr/net/aspose.words/style/equals/
---
## Style.Equals method

Compare avec le style spécifié. Les styles Istds sont comparés uniquement pour les styles intégrés. Les valeurs par défaut des styles ne sont pas incluses dans la comparaison. Le style de base, le style lié et le style du paragraphe suivant sont comparés de manière récursive.

```csharp
public bool Equals(Style style)
```

## Exemples

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
