---
title: ConditionalStyle.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words pour .NET
description: Une mise en forme claire et sans effort grâce à la méthode ConditionalStyle ClearFormatting. Simplifiez votre processus de conception et améliorez la clarté de vos documents dès aujourd'hui !
type: docs
weight: 100
url: /fr/net/aspose.words/conditionalstyle/clearformatting/
---
## ConditionalStyle.ClearFormatting method

Efface la mise en forme de ce style conditionnel.

```csharp
public void ClearFormatting()
```

## Exemples

Montre comment réinitialiser les styles de tableau conditionnels.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("First row");
builder.EndRow();
builder.InsertCell();
builder.Write("Last row");
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
table.Style = tableStyle;

// Définissez le style du tableau pour colorer les bordures de la première ligne du tableau en rouge.
tableStyle.ConditionalStyles.FirstRow.Borders.Color = Color.Red;

// Définissez le style du tableau pour colorer les bordures de la dernière ligne du tableau en bleu.
tableStyle.ConditionalStyles.LastRow.Borders.Color = Color.Blue;

// Vous trouverez ci-dessous deux manières d'utiliser la méthode « ClearFormatting » pour effacer les styles conditionnels.
// 1 - Effacer les styles conditionnels pour une partie spécifique d'un tableau :
tableStyle.ConditionalStyles[0].ClearFormatting();

Assert.AreEqual(Color.Empty, tableStyle.ConditionalStyles.FirstRow.Borders.Color);

// 2 - Effacer les styles conditionnels pour l'ensemble du tableau :
tableStyle.ConditionalStyles.ClearFormatting();

Assert.True(tableStyle.ConditionalStyles.All(s => s.Borders.Color == Color.Empty));
```

### Voir également

* class [ConditionalStyle](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
