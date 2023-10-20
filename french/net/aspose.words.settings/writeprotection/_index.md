---
title: WriteProtection Class
linktitle: WriteProtection
articleTitle: WriteProtection
second_title: Aspose.Words pour .NET
description: Aspose.Words.Settings.WriteProtection classe. Spécifie les paramètres de protection en écriture pour un document en C#.
type: docs
weight: 5970
url: /fr/net/aspose.words.settings/writeprotection/
---
## WriteProtection class

Spécifie les paramètres de protection en écriture pour un document.

Pour en savoir plus, visitez le[Protéger ou chiffrer un document](https://docs.aspose.com/words/net/protect-or-encrypt-a-document/) article documentaire.

```csharp
public class WriteProtection
```

## Propriétés

| Nom | La description |
| --- | --- |
| [IsWriteProtected](../../aspose.words.settings/writeprotection/iswriteprotected/) { get; } | Retours`vrai` lorsqu'un mot de passe de protection en écriture est défini. |
| [ReadOnlyRecommended](../../aspose.words.settings/writeprotection/readonlyrecommended/) { get; set; } | Spécifie si l'auteur du document a recommandé que le document soit ouvert en lecture seule. |

## Méthodes

| Nom | La description |
| --- | --- |
| [SetPassword](../../aspose.words.settings/writeprotection/setpassword/)(*string*) | Définit le mot de passe de protection en écriture pour le document. |
| [ValidatePassword](../../aspose.words.settings/writeprotection/validatepassword/)(*string*) | Retours`vrai` si le mot de passe spécifié est le même que le mot de passe de protection en écriture avec lequel le document a été protégé. Si le document n'est pas protégé en écriture avec un mot de passe, renvoie`FAUX` . |

## Remarques

La protection en écriture spécifie si l'auteur a recommandé que le document soit ouvert en lecture seule et/ou exige un mot de passe pour modifier un document.

La protection en écriture est différente de la protection des documents. La protection en écriture est spécifiée dans Microsoft Word dans les options de la boîte de dialogue Enregistrer sous.

Vous ne créez pas directement des instances de cette classe. Vous accédez aux paramètres de protection des documents via le[`WriteProtection`](../../aspose.words/document/writeprotection/) propriété.

## Exemples

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

* espace de noms [Aspose.Words.Settings](../../aspose.words.settings/)
* Assemblée [Aspose.Words](../../)
