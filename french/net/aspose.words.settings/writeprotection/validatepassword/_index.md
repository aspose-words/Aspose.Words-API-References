---
title: WriteProtection.ValidatePassword
linktitle: ValidatePassword
articleTitle: ValidatePassword
second_title: Aspose.Words pour .NET
description: Sécurisez vos documents avec la méthode WriteProtection ValidatePassword. Vérifiez facilement si le mot de passe correspond à la protection du document pour une sécurité renforcée.
type: docs
weight: 40
url: /fr/net/aspose.words.settings/writeprotection/validatepassword/
---
## WriteProtection.ValidatePassword method

Retours`vrai` si le mot de passe spécifié est le même que le mot de passe de protection en écriture avec lequel le document a été protégé. Si le document n'est pas protégé en écriture avec un mot de passe, renvoie`FAUX` .

```csharp
public bool ValidatePassword(string password)
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
