---
title: Class WriteProtection
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Settings.WriteProtection klas. Gibt Schreibschutzeinstellungen für ein Dokument an.
type: docs
weight: 5970
url: /de/net/aspose.words.settings/writeprotection/
---
## WriteProtection class

Gibt Schreibschutzeinstellungen für ein Dokument an.

Um mehr zu erfahren, besuchen Sie die[Schützen oder verschlüsseln Sie ein Dokument](https://docs.aspose.com/words/net/protect-or-encrypt-a-document/) Dokumentationsartikel.

```csharp
public class WriteProtection
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [IsWriteProtected](../../aspose.words.settings/writeprotection/iswriteprotected/) { get; } | Gibt zurück`WAHR` wenn ein Schreibschutzpasswort gesetzt ist. |
| [ReadOnlyRecommended](../../aspose.words.settings/writeprotection/readonlyrecommended/) { get; set; } | Gibt an, ob der Dokumentautor empfohlen hat, das Dokument schreibgeschützt zu öffnen. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [SetPassword](../../aspose.words.settings/writeprotection/setpassword/)(string) | Legt das Schreibschutzkennwort für das Dokument fest. |
| [ValidatePassword](../../aspose.words.settings/writeprotection/validatepassword/)(string) | Gibt zurück`WAHR` Wenn das angegebene Passwort mit dem Schreibschutzpasswort übereinstimmt, mit dem das Dokument geschützt wurde. Wenn das Dokument nicht mit einem Passwort schreibgeschützt ist, wird zurückgegeben`FALSCH` . |

### Bemerkungen

Der Schreibschutz gibt an, ob der Autor empfohlen hat, das Dokument schreibgeschützt zu öffnen und/oder ein Kennwort zum Ändern eines Dokuments zu erfordern.

Der Schreibschutz unterscheidet sich vom Dokumentenschutz. Der Schreibschutz wird in Microsoft Word in den Optionen des Dialogfelds „Speichern unter“ angegeben.

Sie erstellen keine Instanzen dieser Klasse direkt. Den Zugriff auf die Dokumentenschutzeinstellungen erreichen Sie über[`WriteProtection`](../../aspose.words/document/writeprotection/) Eigentum.

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

* namensraum [Aspose.Words.Settings](../../aspose.words.settings/)
* Montage [Aspose.Words](../../)


