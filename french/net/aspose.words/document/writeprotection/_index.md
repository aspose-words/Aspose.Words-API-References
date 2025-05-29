---
title: Document.WriteProtection
linktitle: WriteProtection
articleTitle: WriteProtection
second_title: Aspose.Words pour .NET
description: Explorez la propriété Document WriteProtection pour gérer sans effort les paramètres de protection en écriture de votre document et améliorer la sécurité.
type: docs
weight: 520
url: /fr/net/aspose.words/document/writeprotection/
---
## Document.WriteProtection property

Donne accès aux options de protection en écriture du document.

```csharp
public WriteProtection WriteProtection { get; }
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

* class [WriteProtection](../../../aspose.words.settings/writeprotection/)
* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
