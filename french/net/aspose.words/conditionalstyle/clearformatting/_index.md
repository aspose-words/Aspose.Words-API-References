---
title: ConditionalStyle.ClearFormatting
second_title: Référence de l'API Aspose.Words pour .NET
description: ConditionalStyle méthode. Efface la mise en forme de ce style conditionnel.
type: docs
weight: 100
url: /fr/net/aspose.words/conditionalstyle/clearformatting/
---
## ConditionalStyle.ClearFormatting method

Efface la mise en forme de ce style conditionnel.

```csharp
public void ClearFormatting()
```

### Exemples

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

// Définit le style de tableau pour colorer les bordures de la première ligne du tableau en rouge.
tableStyle.ConditionalStyles.FirstRow.Borders.Color = Color.Red;

// Définit le style de tableau pour colorer les bordures de la dernière ligne du tableau en bleu.
tableStyle.ConditionalStyles.LastRow.Borders.Color = Color.Blue;

// Vous trouverez ci-dessous deux manières d'utiliser la méthode "ClearFormatting" pour effacer les styles conditionnels.
// 1 - Efface les styles conditionnels pour une partie spécifique d'un tableau :
tableStyle.ConditionalStyles[0].ClearFormatting();

Assert.AreEqual(Color.Empty, tableStyle.ConditionalStyles.FirstRow.Borders.Color);

// 2 - Efface les styles conditionnels pour tout le tableau :
tableStyle.ConditionalStyles.ClearFormatting();

Assert.True(tableStyle.ConditionalStyles.All(s => s.Borders.Color == Color.Empty));
```

### Voir également

* class [ConditionalStyle](../)
* espace de noms [Aspose.Words](../../conditionalstyle/)
* Assemblée [Aspose.Words](../../../)


