---
title: WriteProtection.ValidatePassword
second_title: Aspose.Words für .NET-API-Referenz
description: WriteProtection methode. Gibt zurückWAHR Wenn das angegebene Passwort mit dem Schreibschutzpasswort übereinstimmt mit dem das Dokument geschützt wurde. Wenn das Dokument nicht mit einem Passwort schreibgeschützt ist wird zurückgegebenFALSCH .
type: docs
weight: 40
url: /de/net/aspose.words.settings/writeprotection/validatepassword/
---
## WriteProtection.ValidatePassword method

Gibt zurück`WAHR` Wenn das angegebene Passwort mit dem Schreibschutzpasswort übereinstimmt, mit dem das Dokument geschützt wurde. Wenn das Dokument nicht mit einem Passwort schreibgeschützt ist, wird zurückgegeben`FALSCH` .

```csharp
public bool ValidatePassword(string password)
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

* class [WriteProtection](../)
* namensraum [Aspose.Words.Settings](../../writeprotection/)
* Montage [Aspose.Words](../../../)


