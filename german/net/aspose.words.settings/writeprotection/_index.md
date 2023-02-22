---
title: Class WriteProtection
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Settings.WriteProtection klas. Gibt die Schreibschutzeinstellungen für ein Dokument an.
type: docs
weight: 5670
url: /de/net/aspose.words.settings/writeprotection/
---
## WriteProtection class

Gibt die Schreibschutzeinstellungen für ein Dokument an.

```csharp
public class WriteProtection
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [IsWriteProtected](../../aspose.words.settings/writeprotection/iswriteprotected/) { get; } | Gibt „true“ zurück, wenn ein Schreibschutzkennwort festgelegt ist. |
| [ReadOnlyRecommended](../../aspose.words.settings/writeprotection/readonlyrecommended/) { get; set; } | Gibt an, ob der Autor des Dokuments empfohlen hat, das Dokument schreibgeschützt zu öffnen. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [SetPassword](../../aspose.words.settings/writeprotection/setpassword/)(string) | Legt das Schreibschutzpasswort für das Dokument fest. |
| [ValidatePassword](../../aspose.words.settings/writeprotection/validatepassword/)(string) | Gibt „true“ zurück, wenn das angegebene Passwort mit dem Schreibschutzpasswort übereinstimmt, mit dem das Dokument geschützt wurde. Wenn das Dokument nicht mit einem Passwort schreibgeschützt ist, wird „false“ zurückgegeben. |

### Bemerkungen

Der Schreibschutz gibt an, ob der Autor empfohlen hat, dass das Dokument schreibgeschützt geöffnet werden soll und/oder ein Passwort erforderlich ist, um ein Dokument zu ändern.

Der Schreibschutz unterscheidet sich vom Dokumentenschutz. Der Schreibschutz wird in Microsoft Word in den Optionen des Dialogfelds Speichern unter festgelegt.

Sie erstellen keine Instanzen dieser Klasse direkt. Sie erreichen die Dokumentenschutzeinstellungen über die[`WriteProtection`](../../aspose.words/document/writeprotection/) Eigentum.

### Beispiele

Zeigt, wie Sie ein Dokument mit einem Kennwort schützen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! This document is protected.");

// Geben Sie ein Passwort mit einer Länge von bis zu 15 Zeichen ein und überprüfen Sie dann den Schutzstatus des Dokuments.
doc.WriteProtection.SetPassword("MyPassword");
doc.WriteProtection.ReadOnlyRecommended = true;

Assert.IsTrue(doc.WriteProtection.IsWriteProtected);
Assert.IsTrue(doc.WriteProtection.ValidatePassword("MyPassword"));

// Der Schutz verhindert weder die programmatische Bearbeitung des Dokuments noch verschlüsselt er den Inhalt.
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

* namensraum [Aspose.Words.Settings](../../aspose.words.settings/)
* Montage [Aspose.Words](../../)


