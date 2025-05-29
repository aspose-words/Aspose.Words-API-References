---
title: Field.IsDirty
linktitle: IsDirty
articleTitle: IsDirty
second_title: Aspose.Words pour .NET
description: Gérez la propriété IsDirty pour garantir que vos données de champ restent exactes et à jour, améliorant ainsi l'intégrité et les performances des documents.
type: docs
weight: 40
url: /fr/net/aspose.words.fields/field/isdirty/
---
## Field.IsDirty property

Obtient ou définit si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document.

```csharp
public bool IsDirty { get; set; }
```

## Exemples

Montre comment utiliser une propriété spéciale pour mettre à jour le résultat du champ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Donnez la valeur de la propriété « Auteur » intégrée du document, puis affichez-la avec un champ.
doc.BuiltInDocumentProperties.Author = "John Doe";
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);

Assert.False(field.IsDirty);
Assert.AreEqual("John Doe", field.Result);

// Mettre à jour la propriété. Le champ affiche toujours l'ancienne valeur.
doc.BuiltInDocumentProperties.Author = "John & Jane Doe";

Assert.AreEqual("John Doe", field.Result);

// Étant donné que la valeur du champ est obsolète, nous pouvons la marquer comme « sale ».
// Cette valeur restera obsolète jusqu'à ce que nous mettions à jour le champ manuellement avec la méthode Field.Update().
field.IsDirty = true;

using (MemoryStream docStream = new MemoryStream())
{
    // Si nous sauvegardons sans appeler une méthode de mise à jour,
    // le champ continuera d'afficher la valeur obsolète dans le document de sortie.
    doc.Save(docStream, SaveFormat.Docx);

    // L'objet LoadOptions a une option pour mettre à jour tous les champs
    // marqué comme « sale » lors du chargement du document.
    LoadOptions options = new LoadOptions();
    options.UpdateDirtyFields = updateDirtyFields;
    doc = new Document(docStream, options);

    Assert.AreEqual("John & Jane Doe", doc.BuiltInDocumentProperties.Author);

    field = (FieldAuthor)doc.Range.Fields[0];

    // La mise à jour des champs sales comme celui-ci définit automatiquement leur indicateur « IsDirty » sur false.
    if (updateDirtyFields)
    {
        Assert.AreEqual("John & Jane Doe", field.Result);
        Assert.False(field.IsDirty);
    }
    else
    {
        Assert.AreEqual("John Doe", field.Result);
        Assert.True(field.IsDirty);
    }
}
```

### Voir également

* class [Field](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
