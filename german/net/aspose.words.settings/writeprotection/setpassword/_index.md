---
title: WriteProtection.SetPassword
linktitle: SetPassword
articleTitle: SetPassword
second_title: Aspose.Words für .NET
description: Schützen Sie Ihre Dokumente mit der WriteProtection SetPassword-Methode. Legen Sie einfach ein Kennwort fest, um die Dokumentensicherheit zu erhöhen und unbefugten Zugriff zu verhindern.
type: docs
weight: 30
url: /de/net/aspose.words.settings/writeprotection/setpassword/
---
## WriteProtection.SetPassword method

Legt das Schreibschutzkennwort für das Dokument fest.

```csharp
public void SetPassword(string password)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| password | String | Das festzulegende Passwort. Kann nicht`null`, kann aber eine leere Zeichenfolge sein. |

## Bemerkungen

Wenn ein Kennwort festgelegt ist, fordert Microsoft Word den Benutzer auf, es einzugeben oder das Dokument schreibgeschützt zu öffnen.

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
