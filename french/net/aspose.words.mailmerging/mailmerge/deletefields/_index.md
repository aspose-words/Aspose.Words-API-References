---
title: MailMerge.DeleteFields
second_title: Référence de l'API Aspose.Words pour .NET
description: MailMerge méthode. Supprime les champs liés au publipostage du document.
type: docs
weight: 170
url: /fr/net/aspose.words.mailmerging/mailmerge/deletefields/
---
## MailMerge.DeleteFields method

Supprime les champs liés au publipostage du document.

```csharp
public void DeleteFields()
```

### Remarques

Cette méthode supprime les champs MERGEFIELD et NEXT du document.

Cette méthode peut être utile si votre opération de publipostage n'a pas toujours besoin de pour remplir tous les champs du document. Utilisez cette méthode pour supprimer tous les champs de fusion et publipostage restants .

### Exemples

Montre comment supprimer tous les MERGEFIELD d'un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.Writeln(",");
builder.Writeln("Greetings!");

Assert.AreEqual(
    "Dear \u0013 MERGEFIELD FirstName \u0014«FirstName»\u0015 \u0013 MERGEFIELD LastName \u0014«LastName»\u0015,\rGreetings!", 
    doc.GetText().Trim());

doc.MailMerge.DeleteFields();

Assert.AreEqual("Dear  ,\rGreetings!", doc.GetText().Trim());
```

### Voir également

* class [MailMerge](../)
* espace de noms [Aspose.Words.MailMerging](../../mailmerge/)
* Assemblée [Aspose.Words](../../../)


