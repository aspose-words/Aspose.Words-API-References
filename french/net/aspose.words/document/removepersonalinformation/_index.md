---
title: Document.RemovePersonalInformation
second_title: Référence de l'API Aspose.Words pour .NET
description: Document propriété. Obtient ou définit un indicateur indiquant que Microsoft Word supprimera toutes les informations utilisateur des commentaires des révisions et des propriétés du document lors de lenregistrement du document.
type: docs
weight: 340
url: /fr/net/aspose.words/document/removepersonalinformation/
---
## Document.RemovePersonalInformation property

Obtient ou définit un indicateur indiquant que Microsoft Word supprimera toutes les informations utilisateur des commentaires, des révisions et des propriétés du document lors de l'enregistrement du document.

```csharp
public bool RemovePersonalInformation { get; set; }
```

### Exemples

Montre comment activer la suppression des informations personnelles lors d’une sauvegarde manuelle.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère du contenu avec des informations personnelles.
doc.BuiltInDocumentProperties.Author = "John Doe";
doc.BuiltInDocumentProperties.Company = "Placeholder Inc.";

doc.StartTrackRevisions(doc.BuiltInDocumentProperties.Author, DateTime.Now);
builder.Write("Hello world!");
doc.StopTrackRevisions();

// Cet indicateur est équivalent à Fichier -> Options -> Centre de confiance -> Paramètres du Centre de confidentialité... ->
// Options de confidentialité -> "Supprimer les informations personnelles des propriétés du fichier lors de l'enregistrement" dans Microsoft Word.
doc.RemovePersonalInformation = saveWithoutPersonalInfo;

// Cette option ne prendra pas effet lors d'une opération de sauvegarde effectuée à l'aide d'Aspose.Words.
// Les données personnelles seront supprimées de notre document avec l'indicateur défini lorsque nous les enregistrerons manuellement à l'aide de Microsoft Word.
doc.Save(ArtifactsDir + "Document.RemovePersonalInformation.docx");
doc = new Document(ArtifactsDir + "Document.RemovePersonalInformation.docx");

Assert.AreEqual(saveWithoutPersonalInfo, doc.RemovePersonalInformation);
Assert.AreEqual("John Doe", doc.BuiltInDocumentProperties.Author);
Assert.AreEqual("Placeholder Inc.", doc.BuiltInDocumentProperties.Company);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../document/)
* Assemblée [Aspose.Words](../../../)


