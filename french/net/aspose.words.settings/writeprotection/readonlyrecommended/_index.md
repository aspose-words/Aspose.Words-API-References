---
title: WriteProtection.ReadOnlyRecommended
linktitle: ReadOnlyRecommended
articleTitle: ReadOnlyRecommended
second_title: Aspose.Words pour .NET
description: Découvrez la propriété WriteProtection ReadOnlyRecommended, qui guide les utilisateurs pour ouvrir les documents en mode lecture seule pour une sécurité et une intégrité renforcées.
type: docs
weight: 20
url: /fr/net/aspose.words.settings/writeprotection/readonlyrecommended/
---
## WriteProtection.ReadOnlyRecommended property

Spécifie si l'auteur du document a recommandé que le document soit ouvert en lecture seule.

```csharp
public bool ReadOnlyRecommended { get; set; }
```

## Exemples

Montre comment protéger un document avec un mot de passe.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! This document is protected.");
// Saisissez un mot de passe d'une longueur maximale de 15 caractères, puis vérifiez l'état de protection du document.
doc.WriteProtection.SetPassword("MyPassword");
doc.WriteProtection.ReadOnlyRecommended = true;

Assert.IsTrue(doc.WriteProtection.IsWriteProtected);
Assert.IsTrue(doc.WriteProtection.ValidatePassword("MyPassword"));

// La protection n'empêche pas la modification du document par programmation et ne crypte pas le contenu.
doc.Save(ArtifactsDir + "Document.WriteProtection.docx");
doc = new Document(ArtifactsDir + "Document.WriteProtection.docx");

Assert.IsTrue(doc.WriteProtection.IsWriteProtected);

builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln("Writing text in a protected document.");

Assert.AreEqual("Hello world! This document is protected." +
                "\rWriting text in a protected document.", doc.GetText().Trim());
```

### Voir également

* class [WriteProtection](../)
* espace de noms [Aspose.Words.Settings](../../../aspose.words.settings/)
* Assemblée [Aspose.Words](../../../)
