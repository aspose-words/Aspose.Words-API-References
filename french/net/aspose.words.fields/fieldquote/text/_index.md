---
title: FieldQuote.Text
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldQuote propriété. Obtient ou définit le texte à récupérer.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldquote/text/
---
## FieldQuote.Text property

Obtient ou définit le texte à récupérer.

```csharp
public string Text { get; set; }
```

### Exemples

Indique comment utiliser le champ QUOTE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère un champ QUOTE, qui affichera la valeur de sa propriété Text.
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.AreEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.GetFieldCode());

// Insère un champ QUOTE et imbrique un champ DATE à l'intérieur.
// Les champs DATE mettent à jour leur valeur avec la date actuelle chaque fois que nous ouvrons le document à l'aide de Microsoft Word.
// Imbriquer le champ DATE dans le champ QUOTE comme ceci figera sa valeur
// à la date à laquelle nous avons créé le document.
builder.Write("\nDocument creation date: ");
field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
builder.MoveTo(field.Separator);
builder.InsertField(FieldType.FieldDate, true);

Assert.AreEqual(" QUOTE \u0013 DATE \u0014" + DateTime.Now.Date.ToShortDateString() + "\u0015", field.GetFieldCode());

// Mettez à jour tous les champs pour afficher leurs résultats corrects.
doc.UpdateFields();

Assert.AreEqual("\"Quoted text\"", doc.Range.Fields[0].Result);

doc.Save(ArtifactsDir + "Field.QUOTE.docx");
```

### Voir également

* class [FieldQuote](../)
* espace de noms [Aspose.Words.Fields](../../fieldquote/)
* Assemblée [Aspose.Words](../../../)


