---
title: Document.RemovePersonalInformation
linktitle: RemovePersonalInformation
articleTitle: RemovePersonalInformation
second_title: Aspose.Words pour .NET
description: Assurez la confidentialité avec la fonctionnalité Document RemovePersonalInformation dans Word, qui supprime automatiquement les données utilisateur des commentaires et des propriétés lors de l'enregistrement.
type: docs
weight: 360
url: /fr/net/aspose.words/document/removepersonalinformation/
---
## Document.RemovePersonalInformation property

Obtient ou définit un indicateur indiquant que Microsoft Word supprimera toutes les informations utilisateur des commentaires, des révisions et des propriétés du document lors de l'enregistrement du document.

```csharp
public bool RemovePersonalInformation { get; set; }
```

## Exemples

Montre comment activer la suppression des informations personnelles lors d'une sauvegarde manuelle.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer du contenu avec des informations personnelles.
doc.BuiltInDocumentProperties.Author = "John Doe";
doc.BuiltInDocumentProperties.Company = "Placeholder Inc.";

doc.StartTrackRevisions(doc.BuiltInDocumentProperties.Author, DateTime.Now);
builder.Write("Hello world!");
doc.StopTrackRevisions();

// Cet indicateur est équivalent à Fichier -> Options -> Centre de gestion de la confidentialité -> Paramètres du Centre de gestion de la confidentialité... ->
// Options de confidentialité -> « Supprimer les informations personnelles des propriétés du fichier lors de l'enregistrement » dans Microsoft Word.
doc.RemovePersonalInformation = saveWithoutPersonalInfo;

// Cette option ne prendra pas effet lors d'une opération de sauvegarde effectuée à l'aide d'Aspose.Words.
// Les données personnelles seront supprimées de notre document avec l'indicateur défini lorsque nous l'enregistrerons manuellement à l'aide de Microsoft Word.
doc.Save(ArtifactsDir + "Document.RemovePersonalInformation.docx");
doc = new Document(ArtifactsDir + "Document.RemovePersonalInformation.docx");

Assert.AreEqual(saveWithoutPersonalInfo, doc.RemovePersonalInformation);
Assert.AreEqual("John Doe", doc.BuiltInDocumentProperties.Author);
Assert.AreEqual("Placeholder Inc.", doc.BuiltInDocumentProperties.Company);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
