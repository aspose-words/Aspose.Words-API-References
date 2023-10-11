---
title: WriteProtection.SetPassword
second_title: Référence de l'API Aspose.Words pour .NET
description: WriteProtection méthode. Définit le mot de passe de protection en écriture pour le document.
type: docs
weight: 30
url: /fr/net/aspose.words.settings/writeprotection/setpassword/
---
## WriteProtection.SetPassword method

Définit le mot de passe de protection en écriture pour le document.

```csharp
public void SetPassword(string password)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| password | String | Le mot de passe à définir. C'est pas possible`nul`, mais peut être une chaîne vide. |

### Remarques

Si un mot de passe est défini, Microsoft Word demandera à l'utilisateur de le saisir ou d'ouvrir le document en lecture seule.

### Exemples

Montre comment protéger un document avec un mot de passe.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! This document is protected.");
// Saisissez un mot de passe de 15 caractères maximum, puis vérifiez l'état de protection du document.
doc.WriteProtection.SetPassword("MyPassword");
doc.WriteProtection.ReadOnlyRecommended = true;

Assert.IsTrue(doc.WriteProtection.IsWriteProtected);
Assert.IsTrue(doc.WriteProtection.ValidatePassword("MyPassword"));

// La protection n'empêche pas la modification du document par programme et ne crypte pas non plus son contenu.
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
* espace de noms [Aspose.Words.Settings](../../writeprotection/)
* Assemblée [Aspose.Words](../../../)


