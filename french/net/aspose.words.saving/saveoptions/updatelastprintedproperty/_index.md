---
title: SaveOptions.UpdateLastPrintedProperty
linktitle: UpdateLastPrintedProperty
articleTitle: UpdateLastPrintedProperty
second_title: Aspose.Words pour .NET
description: Optimisez la gestion de vos documents avec SaveOptions UpdateLastPrintedProperty. Contrôlez les mises à jour de LastPrinted pour une sauvegarde efficace et un flux de travail optimisé.
type: docs
weight: 180
url: /fr/net/aspose.words.saving/saveoptions/updatelastprintedproperty/
---
## SaveOptions.UpdateLastPrintedProperty property

Obtient ou définit une valeur déterminant si le[`LastPrinted`](../../../aspose.words.properties/builtindocumentproperties/lastprinted/) la propriété est mise à jour avant l'enregistrement.

```csharp
public bool UpdateLastPrintedProperty { get; set; }
```

## Exemples

Montre comment mettre à jour la propriété « Dernière impression » d'un document lors de l'enregistrement.

```csharp
Document doc = new Document();

DateTime lastPrinted = new DateTime(2019, 12, 20);
doc.BuiltInDocumentProperties.LastPrinted = lastPrinted;

// Cet indicateur détermine si la dernière date imprimée, qui est une propriété intégrée, est mise à jour.
// Si tel est le cas, alors la date de la dernière opération de sauvegarde du document
// avec cet objet SaveOptions passé en paramètre est utilisé comme date d'impression.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.UpdateLastPrintedProperty = isUpdateLastPrintedProperty;

// Dans Microsoft Word 2003, cette propriété peut être trouvée via Fichier -> Propriétés -> Statistiques -> Imprimé.
// Il peut également être affiché dans le corps du document en utilisant un champ PRINTDATE.
doc.Save(ArtifactsDir + "DocSaveOptions.UpdateLastPrintedProperty.doc", saveOptions);

// Ouvrez le document enregistré, puis vérifiez la valeur de la propriété.
doc = new Document(ArtifactsDir + "DocSaveOptions.UpdateLastPrintedProperty.doc");

if (isUpdateLastPrintedProperty)
    Assert.AreNotEqual(lastPrinted, doc.BuiltInDocumentProperties.LastPrinted);
else
    Assert.AreEqual(lastPrinted, doc.BuiltInDocumentProperties.LastPrinted);
```

### Voir également

* class [SaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
