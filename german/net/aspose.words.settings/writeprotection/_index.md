---
title: WriteProtection Class
linktitle: WriteProtection
articleTitle: WriteProtection
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Settings.WriteProtection, um die Schreibschutzeinstellungen für Dokumente einfach zu verwalten und die Sicherheit Ihrer Dokumente zu verbessern.
type: docs
weight: 6800
url: /de/net/aspose.words.settings/writeprotection/
---
## WriteProtection class

Gibt die Schreibschutzeinstellungen für ein Dokument an.

Um mehr zu erfahren, besuchen Sie die[Schützen oder Verschlüsseln eines Dokuments](https://docs.aspose.com/words/net/protect-or-encrypt-a-document/) Dokumentationsartikel.

```csharp
public class WriteProtection
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [IsWriteProtected](../../aspose.words.settings/writeprotection/iswriteprotected/) { get; } | Rückgaben`WAHR` wenn ein Schreibschutzkennwort festgelegt ist. |
| [ReadOnlyRecommended](../../aspose.words.settings/writeprotection/readonlyrecommended/) { get; set; } | Gibt an, ob der Autor des Dokuments empfohlen hat, das Dokument schreibgeschützt zu öffnen. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [SetPassword](../../aspose.words.settings/writeprotection/setpassword/)(*string*) | Legt das Schreibschutzkennwort für das Dokument fest. |
| [ValidatePassword](../../aspose.words.settings/writeprotection/validatepassword/)(*string*) | Rückgaben`WAHR` wenn das angegebene Passwort mit dem Schreibschutzpasswort übereinstimmt, mit dem das Dokument geschützt wurde. Wenn das Dokument nicht mit einem Passwort schreibgeschützt ist, wird Folgendes zurückgegeben:`FALSCH` . |

## Bemerkungen

Der Schreibschutz gibt an, ob der Autor empfohlen hat, das Dokument nur lesbar zu öffnen und/oder zum Ändern eines Dokuments ein Kennwort anzufordern.

Schreibschutz ist nicht mit Dokumentschutz identisch. Schreibschutz wird in Microsoft Word in den Optionen des Dialogfelds „Speichern unter“ festgelegt.

Sie erstellen keine Instanzen dieser Klasse direkt. Sie greifen auf die Dokumentschutzeinstellungen über die[`WriteProtection`](../../aspose.words/document/writeprotection/) Eigentum.

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

* namensraum [Aspose.Words.Settings](../../aspose.words.settings/)
* Montage [Aspose.Words](../../)
