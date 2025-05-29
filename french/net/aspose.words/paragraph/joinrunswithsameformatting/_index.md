---
title: Paragraph.JoinRunsWithSameFormatting
linktitle: JoinRunsWithSameFormatting
articleTitle: JoinRunsWithSameFormatting
second_title: Aspose.Words pour .NET
description: Reliez facilement des passages avec une mise en forme cohérente dans vos paragraphes grâce à la méthode JoinRunsWithSameFormatting. Améliorez le style de votre document dès aujourd'hui !
type: docs
weight: 300
url: /fr/net/aspose.words/paragraph/joinrunswithsameformatting/
---
## Paragraph.JoinRunsWithSameFormatting method

Les jointures s'exécutent avec le même formatage dans le paragraphe.

```csharp
public int JoinRunsWithSameFormatting()
```

### Return_Value

Nombre de jointures effectuées. Quand**N** les pistes adjacentes sont jointes, elles comptent comme**N - 1** rejoint.

## Exemples

Montre comment simplifier les paragraphes en fusionnant les passages superflus.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer quatre séquences de texte dans le paragraphe.
builder.Write("Run 1. ");
builder.Write("Run 2. ");
builder.Write("Run 3. ");
builder.Write("Run 4. ");

// Si nous ouvrons ce document dans Microsoft Word, le paragraphe ressemblera à un corps de texte homogène.
// Cependant, il sera composé de quatre passages distincts avec la même mise en forme. Des paragraphes fragmentés comme celui-ci
// peut se produire lorsque nous modifions manuellement plusieurs fois des parties d'un paragraphe dans Microsoft Word.
Paragraph para = builder.CurrentParagraph;

Assert.AreEqual(4, para.Runs.Count);

// Modifiez le style de la dernière exécution pour la distinguer des trois premières.
para.Runs[3].Font.StyleIdentifier = StyleIdentifier.Emphasis;

// Nous pouvons exécuter la méthode « JoinRunsWithSameFormatting » pour optimiser le contenu du document
// en fusionnant des exécutions similaires en une seule, réduisant ainsi leur nombre total.
// Cette méthode renvoie également le nombre d'exécutions que cette méthode a fusionnées.
// Ces deux fusions ont eu lieu pour combiner les exécutions n°1, n°2 et n°3,
// tout en laissant de côté Run #4 car il a un style incompatible.
Assert.AreEqual(2, para.JoinRunsWithSameFormatting());

// Le nombre de courses restantes sera égal au nombre initial
// moins le nombre de fusions exécutées par la méthode « JoinRunsWithSameFormatting ».
Assert.AreEqual(2, para.Runs.Count);
Assert.AreEqual("Run 1. Run 2. Run 3. ", para.Runs[0].Text);
Assert.AreEqual("Run 4. ", para.Runs[1].Text);
```

### Voir également

* class [Paragraph](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
