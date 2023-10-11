---
title: Document.WriteProtection
second_title: Aspose.Words für .NET-API-Referenz
description: Document eigendom. Bietet Zugriff auf die Schreibschutzoptionen für Dokumente.
type: docs
weight: 500
url: /de/net/aspose.words/document/writeprotection/
---
## Document.WriteProtection property

Bietet Zugriff auf die Schreibschutzoptionen für Dokumente.

```csharp
public WriteProtection WriteProtection { get; }
```

### Beispiele

Zeigt, wie man ein Dokument mit einem Passwort schützt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! This document is protected.");
// Geben Sie ein bis zu 15 Zeichen langes Passwort ein und überprüfen Sie dann den Schutzstatus des Dokuments.
doc.WriteProtection.SetPassword("MyPassword");
doc.WriteProtection.ReadOnlyRecommended = true;

Assert.IsTrue(doc.WriteProtection.IsWriteProtected);
Assert.IsTrue(doc.WriteProtection.ValidatePassword("MyPassword"));

// Der Schutz verhindert nicht, dass das Dokument programmgesteuert bearbeitet wird, und verschlüsselt auch nicht den Inhalt.
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

* class [WriteProtection](../../../aspose.words.settings/writeprotection/)
* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)


