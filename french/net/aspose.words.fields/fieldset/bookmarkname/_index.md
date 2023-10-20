---
title: FieldSet.BookmarkName
linktitle: BookmarkName
articleTitle: BookmarkName
second_title: Aspose.Words pour .NET
description: FieldSet BookmarkName propriété. Obtient ou définit le nom du signet en C#.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldset/bookmarkname/
---
## FieldSet.BookmarkName property

Obtient ou définit le nom du signet.

```csharp
public string BookmarkName { get; set; }
```

## Exemples

Montre comment créer un texte mis en signet avec un champ SET, puis l'afficher dans le document à l'aide d'un champ REF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // Nommez le texte mis en signet avec un champ SET.
// Ce champ fait référence au "signet" non pas à une structure de signet qui apparaît dans le texte, mais à une variable nommée.
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
