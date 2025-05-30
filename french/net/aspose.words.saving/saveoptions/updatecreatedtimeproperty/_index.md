---
title: SaveOptions.UpdateCreatedTimeProperty
linktitle: UpdateCreatedTimeProperty
articleTitle: UpdateCreatedTimeProperty
second_title: Aspose.Words pour .NET
description: Optimisez vos options d'enregistrement avec la propriété UpdateCreatedTime. Contrôlez les mises à jour de CreatedTime avant l'enregistrement, améliorant ainsi la précision des données. Valeur par défaut  false.
type: docs
weight: 160
url: /fr/net/aspose.words.saving/saveoptions/updatecreatedtimeproperty/
---
## SaveOptions.UpdateCreatedTimeProperty property

Obtient ou définit une valeur déterminant si le[`CreatedTime`](../../../aspose.words.properties/builtindocumentproperties/createdtime/) la propriété est mise à jour avant l'enregistrement. La valeur par défaut est`FAUX` ;

```csharp
public bool UpdateCreatedTimeProperty { get; set; }
```

## Exemples

Montre comment mettre à jour la propriété « CreatedTime » d'un document lors de l'enregistrement.

```csharp
Document doc = new Document();

DateTime createdTime = new DateTime(2019, 12, 20);
doc.BuiltInDocumentProperties.CreatedTime = createdTime;

// Cet indicateur détermine si l'heure de création, qui est une propriété intégrée, est mise à jour.
// Si tel est le cas, alors la date de la dernière opération de sauvegarde du document
// avec cet objet SaveOptions passé en paramètre est utilisé comme heure de création.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.UpdateCreatedTimeProperty = isUpdateCreatedTimeProperty;

doc.Save(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);

// Ouvrez le document enregistré, puis vérifiez la valeur de la propriété.
doc = new Document(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx");

if (isUpdateCreatedTimeProperty)
    Assert.AreNotEqual(createdTime, doc.BuiltInDocumentProperties.CreatedTime);
else
    Assert.AreEqual(createdTime, doc.BuiltInDocumentProperties.CreatedTime);
```

### Voir également

* class [SaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
