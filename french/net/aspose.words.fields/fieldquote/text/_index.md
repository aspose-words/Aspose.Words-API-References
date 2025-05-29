---
title: FieldQuote.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words pour .NET
description: Propriété Texte FieldQuote. Récupérez ou définissez facilement du texte pour une gestion optimisée des données. Simplifiez votre flux de travail grâce à cette fonctionnalité puissante !
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldquote/text/
---
## FieldQuote.Text property

Obtient ou définit le texte à récupérer.

```csharp
public string Text { get; set; }
```

## Exemples

Montre comment utiliser le champ CITATION.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérez un champ QUOTE, qui affichera la valeur de sa propriété Texte.
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.AreEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.GetFieldCode());

// Insérez un champ QUOTE et imbriquez un champ DATE à l'intérieur.
// Les champs DATE mettent à jour leur valeur à la date actuelle chaque fois que nous ouvrons le document à l'aide de Microsoft Word.
// L'imbrication du champ DATE dans le champ QUOTE comme ceci gèlera sa valeur
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
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
