---
title: WriteProtection.IsWriteProtected
linktitle: IsWriteProtected
articleTitle: IsWriteProtected
second_title: Aspose.Words für .NET
description: Entdecken Sie die WriteProtection-Eigenschaft „IsWriteProtected“ und überprüfen Sie einfach, ob ein Schreibschutzkennwort aktiv ist, um die Sicherheit und Datenintegrität zu verbessern.
type: docs
weight: 10
url: /de/net/aspose.words.settings/writeprotection/iswriteprotected/
---
## WriteProtection.IsWriteProtected property

Rückgaben`WAHR` wenn ein Schreibschutzkennwort festgelegt ist.

```csharp
public bool IsWriteProtected { get; }
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
