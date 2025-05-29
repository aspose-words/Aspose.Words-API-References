---
title: WriteProtection.SetPassword
linktitle: SetPassword
articleTitle: SetPassword
second_title: Aspose.Words pour .NET
description: Sécurisez vos documents avec la méthode WriteProtection SetPassword. Définissez facilement un mot de passe pour renforcer la sécurité de vos documents et empêcher tout accès non autorisé.
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
| password | String | Le mot de passe à définir. Impossible`nul`, mais peut être une chaîne vide. |

## Remarques

Si un mot de passe est défini, Microsoft Word demandera à l'utilisateur de le saisir ou d'ouvrir le document en lecture seule.

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
