---
title: WriteProtection.IsWriteProtected
second_title: Référence de l'API Aspose.Words pour .NET
description: WriteProtection propriété. Retoursvrai lorsquun mot de passe de protection en écriture est défini.
type: docs
weight: 10
url: /fr/net/aspose.words.settings/writeprotection/iswriteprotected/
---
## WriteProtection.IsWriteProtected property

Retours`vrai` lorsqu'un mot de passe de protection en écriture est défini.

```csharp
public bool IsWriteProtected { get; }
```

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


