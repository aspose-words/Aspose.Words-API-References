---
title: FieldSet.BookmarkText
linktitle: BookmarkText
articleTitle: BookmarkText
second_title: Aspose.Words pour .NET
description: Découvrez comment gérer facilement la propriété FieldSet BookmarkText pour personnaliser et améliorer vos signets pour une meilleure organisation et accessibilité.
type: docs
weight: 30
url: /fr/net/aspose.words.fields/fieldset/bookmarktext/
---
## FieldSet.BookmarkText property

Obtient ou définit le nouveau texte du signet.

```csharp
public string BookmarkText { get; set; }
```

## Exemples

Montre comment créer du texte marqué d'un signet avec un champ SET, puis l'afficher dans le document à l'aide d'un champ REF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // Nommez le texte marqué avec un champ SET.
// Ce champ fait référence au « signet », non pas à une structure de signet qui apparaît dans le texte, mais à une variable nommée.
FieldSet fieldSet = (FieldSet)builder.InsertField(FieldType.FieldSet, false);
fieldSet.BookmarkName = "MyBookmark";
fieldSet.BookmarkText = "Hello world!";
fieldSet.Update();

Assert.AreEqual(" SET  MyBookmark \"Hello world!\"", fieldSet.GetFieldCode());

// Faites référence au signet par son nom dans un champ REF et affichez son contenu.
FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
fieldRef.BookmarkName = "MyBookmark";
fieldRef.Update();

Assert.AreEqual(" REF  MyBookmark", fieldRef.GetFieldCode());
Assert.AreEqual("Hello world!", fieldRef.Result);

doc.Save(ArtifactsDir + "Field.SET.REF.docx");
```

### Voir également

* class [FieldSet](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
