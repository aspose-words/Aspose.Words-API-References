---
title: WriteProtection.ValidatePassword
linktitle: ValidatePassword
articleTitle: ValidatePassword
second_title: Aspose.Words für .NET
description: Sichern Sie Ihre Dokumente mit der WriteProtection ValidatePassword-Methode. Überprüfen Sie einfach, ob das Kennwort mit dem Schutz des Dokuments übereinstimmt, und erhöhen Sie so die Sicherheit.
type: docs
weight: 40
url: /de/net/aspose.words.settings/writeprotection/validatepassword/
---
## WriteProtection.ValidatePassword method

Rückgaben`WAHR` wenn das angegebene Passwort mit dem Schreibschutzpasswort übereinstimmt, mit dem das Dokument geschützt wurde. Wenn das Dokument nicht mit einem Passwort schreibgeschützt ist, wird Folgendes zurückgegeben:`FALSCH` .

```csharp
public bool ValidatePassword(string password)
```

## Beispiele

Zeigt, wie Sie ein Dokument mit einem Kennwort schützen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! This document is protected.");
// Geben Sie ein bis zu 15 Zeichen langes Passwort ein und überprüfen Sie anschließend den Schutzstatus des Dokuments.
doc.WriteProtection.SetPassword("MyPassword");
doc.WriteProtection.ReadOnlyRecommended = true;

Assert.IsTrue(doc.WriteProtection.IsWriteProtected);
Assert.IsTrue(doc.WriteProtection.ValidatePassword("MyPassword"));

// Der Schutz verhindert weder die programmgesteuerte Bearbeitung des Dokuments noch verschlüsselt er den Inhalt.
doc.Save(ArtifactsDir + "Document.WriteProtection.docx");
doc = new Document(ArtifactsDir + "Document.WriteProtection.docx");

Assert.IsTrue(doc.WriteProtection.IsWriteProtected);

builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln("Writing text in a protected document.");

Assert.AreEqual("Hello world! This document is protected." +
                "\rWriting text in a protected document.", doc.GetText().Trim());
```

### Siehe auch

* class [WriteProtection](../)
* namensraum [Aspose.Words.Settings](../../../aspose.words.settings/)
* Montage [Aspose.Words](../../../)
