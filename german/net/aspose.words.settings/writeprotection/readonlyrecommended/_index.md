---
title: WriteProtection.ReadOnlyRecommended
linktitle: ReadOnlyRecommended
articleTitle: ReadOnlyRecommended
second_title: Aspose.Words für .NET
description: Entdecken Sie die WriteProtection ReadOnlyRecommended-Eigenschaft, die Benutzer anweist, Dokumente im schreibgeschützten Modus zu öffnen, um die Sicherheit und Integrität zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words.settings/writeprotection/readonlyrecommended/
---
## WriteProtection.ReadOnlyRecommended property

Gibt an, ob der Autor des Dokuments empfohlen hat, das Dokument schreibgeschützt zu öffnen.

```csharp
public bool ReadOnlyRecommended { get; set; }
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
