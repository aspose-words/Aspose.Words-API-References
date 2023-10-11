---
title: SaveOptions.UpdateLastSavedTimeProperty
second_title: Référence de l'API Aspose.Words pour .NET
description: SaveOptions propriété. Obtient ou définit une valeur déterminant si leLastSavedTime la propriété est mise à jour avant lenregistrement.
type: docs
weight: 180
url: /fr/net/aspose.words.saving/saveoptions/updatelastsavedtimeproperty/
---
## SaveOptions.UpdateLastSavedTimeProperty property

Obtient ou définit une valeur déterminant si le[`LastSavedTime`](../../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la propriété est mise à jour avant l'enregistrement.

```csharp
public bool UpdateLastSavedTimeProperty { get; set; }
```

### Exemples

Montre comment déterminer s’il faut conserver la propriété « Dernière heure enregistrée » du document lors de l’enregistrement.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(new DateTime(2021, 5, 11, 6, 32, 0), 
    doc.BuiltInDocumentProperties.LastSavedTime);

// Lorsque nous enregistrons le document au format OOXML, nous pouvons créer un objet OoxmlSaveOptions
// puis transmettez-le à la méthode de sauvegarde du document pour modifier la façon dont nous enregistrons le document.
// Définit la propriété "UpdateLastSavedTimeProperty" sur "true" pour
// définit la propriété intégrée "Dernière heure enregistrée" du document de sortie sur la date/heure actuelle.
// Définit la propriété "UpdateLastSavedTimeProperty" sur "false" pour
// préserve la valeur originale de la propriété intégrée "Dernière heure enregistrée" du document d'entrée.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.UpdateLastSavedTimeProperty = updateLastSavedTimeProperty;

doc.Save(ArtifactsDir + "OoxmlSaveOptions.LastSavedTime.docx", saveOptions);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.LastSavedTime.docx");
DateTime lastSavedTimeNew = doc.BuiltInDocumentProperties.LastSavedTime;

if (updateLastSavedTimeProperty)
    Assert.That(DateTime.Now, Is.EqualTo(lastSavedTimeNew).Within(1).Days);
else
    Assert.AreEqual(new DateTime(2021, 5, 11, 6, 32, 0), 
        lastSavedTimeNew);
```

### Voir également

* class [SaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../saveoptions/)
* Assemblée [Aspose.Words](../../../)


