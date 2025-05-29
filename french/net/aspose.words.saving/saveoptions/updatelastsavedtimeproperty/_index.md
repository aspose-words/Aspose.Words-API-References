---
title: SaveOptions.UpdateLastSavedTimeProperty
linktitle: UpdateLastSavedTimeProperty
articleTitle: UpdateLastSavedTimeProperty
second_title: Aspose.Words pour .NET
description: Optimisez vos options d'enregistrement avec la propriété UpdateLastSavedTime. Contrôlez les mises à jour LastSavedTime pour une gestion efficace des données et des performances améliorées.
type: docs
weight: 190
url: /fr/net/aspose.words.saving/saveoptions/updatelastsavedtimeproperty/
---
## SaveOptions.UpdateLastSavedTimeProperty property

Obtient ou définit une valeur déterminant si le[`LastSavedTime`](../../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la propriété est mise à jour avant l'enregistrement.

```csharp
public bool UpdateLastSavedTimeProperty { get; set; }
```

## Exemples

Montre comment déterminer s'il faut conserver la propriété « Dernière heure d'enregistrement » du document lors de l'enregistrement.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(new DateTime(2021, 5, 11, 6, 32, 0), 
    doc.BuiltInDocumentProperties.LastSavedTime);

// Lorsque nous enregistrons le document au format OOXML, nous pouvons créer un objet OoxmlSaveOptions
// puis transmettez-le à la méthode d'enregistrement du document pour modifier la façon dont nous enregistrons le document.
// Définissez la propriété « UpdateLastSavedTimeProperty » sur « true » pour
// définir la propriété intégrée « Dernière heure d'enregistrement » du document de sortie sur la date/heure actuelle.
// Définissez la propriété « UpdateLastSavedTimeProperty » sur « false » pour
// conserver la valeur d'origine de la propriété intégrée « Dernière heure d'enregistrement » du document d'entrée.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.UpdateLastSavedTimeProperty = updateLastSavedTimeProperty;

doc.Save(ArtifactsDir + "OoxmlSaveOptions.LastSavedTime.docx", saveOptions);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.LastSavedTime.docx");
DateTime lastSavedTimeNew = doc.BuiltInDocumentProperties.LastSavedTime;

if (updateLastSavedTimeProperty)
    Assert.IsTrue((DateTime.Now - lastSavedTimeNew).Days < 1);
else
    Assert.AreEqual(new DateTime(2021, 5, 11, 6, 32, 0), 
        lastSavedTimeNew);
```

### Voir également

* class [SaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
