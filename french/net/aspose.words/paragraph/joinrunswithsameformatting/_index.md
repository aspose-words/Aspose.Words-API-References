---
title: Paragraph.JoinRunsWithSameFormatting
second_title: Référence de l'API Aspose.Words pour .NET
description: Paragraph méthode. Les jointures sexécutent avec le même formatage dans le paragraphe.
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

Nombre de jointures effectuées. Quand **N** les pistes adjacentes sont rejointes, elles comptent comme **N-1** rejoint.

### Exemples

Montre comment simplifier les paragraphes en fusionnant les passages superflus.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère quatre séquences de texte dans le paragraphe.
builder.Write("Run 1. ");
builder.Write("Run 2. ");
builder.Write("Run 3. ");
builder.Write("Run 4. ");

// Si nous ouvrons ce document dans Microsoft Word, le paragraphe ressemblera à un corps de texte homogène.
// Cependant, il s'agira de quatre exécutions distinctes avec le même formatage. Des paragraphes fragmentés comme celui-ci
// peut se produire lorsque nous modifions manuellement des parties d'un paragraphe plusieurs fois dans Microsoft Word.
Paragraph para = builder.CurrentParagraph;

Assert.AreEqual(4, para.Runs.Count);

// Change le style de la dernière exécution pour la distinguer des trois premières.
para.Runs[3].Font.StyleIdentifier = StyleIdentifier.Emphasis;

// On peut exécuter la méthode "JoinRunsWithSameFormatting" pour optimiser le contenu du document
// en fusionnant les exécutions similaires en une seule, réduisant ainsi leur nombre global.
// Cette méthode renvoie également le nombre d'exécutions fusionnées par cette méthode.
// Ces deux fusions ont eu lieu pour combiner les exécutions n°1, n°2 et n°3,
// tout en laissant de côté l'exécution n°4 car son style est incompatible.
Assert.AreEqual(2, para.JoinRunsWithSameFormatting());

// Le nombre de courses restantes sera égal au nombre d'origine
// moins le nombre de fusions d'exécutions effectuées par la méthode "JoinRunsWithSameFormatting".
Assert.AreEqual(2, para.Runs.Count);
Assert.AreEqual("Run 1. Run 2. Run 3. ", para.Runs[0].Text);
Assert.AreEqual("Run 4. ", para.Runs[1].Text);
```

### Voir également

* class [Paragraph](../)
* espace de noms [Aspose.Words](../../paragraph/)
* Assemblée [Aspose.Words](../../../)


