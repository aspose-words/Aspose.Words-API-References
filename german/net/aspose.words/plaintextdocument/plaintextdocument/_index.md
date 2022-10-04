---
title: PlainTextDocument
second_title: Aspose.Words für .NET-API-Referenz
description: Erstellt aus einer Datei ein NurTextDokument. Erkennt automatisch das Dateiformat.
type: docs
weight: 10
url: /de/net/aspose.words/plaintextdocument/plaintextdocument/
---
## PlainTextDocument(string) {#constructor_2}

Erstellt aus einer Datei ein Nur-Text-Dokument. Erkennt automatisch das Dateiformat.

```csharp
public PlainTextDocument(string fileName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Name der Datei, aus der der Text extrahiert werden soll. |

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Das Dokumentformat wird nicht erkannt oder nicht unterstützt. |
| [FileCorruptedException](../../filecorruptedexception/) | Das Dokument scheint beschädigt zu sein und kann nicht geladen werden. |
| Exception | Es gibt ein Problem mit dem Dokument und es sollte den Aspose.Words-Entwicklern gemeldet werden. |
| IOException | Es liegt eine Ein-/Ausgabeausnahme vor. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Das Dokument ist verschlüsselt und zum Öffnen ist ein Kennwort erforderlich, aber Sie haben ein falsches Kennwort angegeben. |
| ArgumentException | Der Name der Datei darf nicht null oder eine leere Zeichenfolge sein. |

### Beispiele

Zeigt, wie der Inhalt eines Microsoft Word-Dokuments im Klartext geladen wird.

```csharp
Document doc = new Document(); 
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PlainTextDocument.Load.docx");

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.Load.docx");

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
```

### Siehe auch

* class [PlainTextDocument](../)
* namensraum [Aspose.Words](../../plaintextdocument/)
* Montage [Aspose.Words](../../../)

---

## PlainTextDocument(string, LoadOptions) {#constructor_3}

Erstellt aus einer Datei ein Nur-Text-Dokument. Ermöglicht die Angabe zusätzlicher Optionen wie z. B. eines Verschlüsselungskennworts.

```csharp
public PlainTextDocument(string fileName, LoadOptions loadOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Name der Datei, aus der der Text extrahiert werden soll. |
| loadOptions | LoadOptions | Zusätzliche Optionen zum Laden eines Dokuments. Kann null sein. |

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Das Dokumentformat wird nicht erkannt oder nicht unterstützt. |
| [FileCorruptedException](../../filecorruptedexception/) | Das Dokument scheint beschädigt zu sein und kann nicht geladen werden. |
| Exception | Es gibt ein Problem mit dem Dokument und es sollte den Aspose.Words-Entwicklern gemeldet werden. |
| IOException | Es liegt eine Ein-/Ausgabeausnahme vor. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Das Dokument ist verschlüsselt und zum Öffnen ist ein Kennwort erforderlich, aber Sie haben ein falsches Kennwort angegeben. |
| ArgumentException | Der Name der Datei darf nicht null oder eine leere Zeichenfolge sein. |

### Beispiele

Zeigt, wie der Inhalt eines verschlüsselten Microsoft Word-Dokuments im Klartext geladen wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "PlainTextDocument.LoadEncrypted.docx", saveOptions);

LoadOptions loadOptions = new LoadOptions();
loadOptions.Password = "MyPassword";

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.LoadEncrypted.docx", loadOptions);

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
```

### Siehe auch

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [PlainTextDocument](../)
* namensraum [Aspose.Words](../../plaintextdocument/)
* Montage [Aspose.Words](../../../)

---

## PlainTextDocument(Stream) {#constructor}

Erstellt ein Nur-Text-Dokument aus einem Stream. Erkennt automatisch das Dateiformat.

```csharp
public PlainTextDocument(Stream stream)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | Stream | Der Stream, aus dem der Text extrahiert werden soll. |

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Das Dokumentformat wird nicht erkannt oder nicht unterstützt. |
| [FileCorruptedException](../../filecorruptedexception/) | Das Dokument scheint beschädigt zu sein und kann nicht geladen werden. |
| Exception | Es gibt ein Problem mit dem Dokument und es sollte den Aspose.Words-Entwicklern gemeldet werden. |
| IOException | Es liegt eine Ein-/Ausgabeausnahme vor. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Das Dokument ist verschlüsselt und zum Öffnen ist ein Kennwort erforderlich, aber Sie haben ein falsches Kennwort angegeben. |
| ArgumentNullException | Der Stream darf nicht null sein. |
| NotSupportedException | Der Stream unterstützt kein Lesen oder Suchen. |
| ObjectDisposedException | Der Stream ist ein verworfenes Objekt. |

### Bemerkungen

Das Dokument muss am Anfang des Streams gespeichert werden. Der Stream muss eine zufällige Positionierung unterstützen.

### Beispiele

Zeigt, wie der Inhalt eines Microsoft Word-Dokuments mithilfe von Stream im Klartext geladen wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
doc.Save(ArtifactsDir + "PlainTextDocument.LoadFromStream.docx");

using (FileStream stream = new FileStream(ArtifactsDir + "PlainTextDocument.LoadFromStream.docx", FileMode.Open))
{
    PlainTextDocument plaintext = new PlainTextDocument(stream);

    Assert.AreEqual("Hello world!", plaintext.Text.Trim());
}
```

### Siehe auch

* class [PlainTextDocument](../)
* namensraum [Aspose.Words](../../plaintextdocument/)
* Montage [Aspose.Words](../../../)

---

## PlainTextDocument(Stream, LoadOptions) {#constructor_1}

Erstellt ein Nur-Text-Dokument aus einem Stream. Ermöglicht die Angabe zusätzlicher Optionen wie z. B. eines Verschlüsselungskennworts.

```csharp
public PlainTextDocument(Stream stream, LoadOptions loadOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | Stream | Der Stream, aus dem der Text extrahiert werden soll. |
| loadOptions | LoadOptions | Zusätzliche Optionen zum Laden eines Dokuments. Kann null sein. |

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Das Dokumentformat wird nicht erkannt oder nicht unterstützt. |
| [FileCorruptedException](../../filecorruptedexception/) | Das Dokument scheint beschädigt zu sein und kann nicht geladen werden. |
| Exception | Es gibt ein Problem mit dem Dokument und es sollte den Aspose.Words-Entwicklern gemeldet werden. |
| IOException | Es liegt eine Ein-/Ausgabeausnahme vor. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Das Dokument ist verschlüsselt und zum Öffnen ist ein Kennwort erforderlich, aber Sie haben ein falsches Kennwort angegeben. |
| ArgumentNullException | Der Stream darf nicht null sein. |
| NotSupportedException | Der Stream unterstützt kein Lesen oder Suchen. |
| ObjectDisposedException | Der Stream ist ein verworfenes Objekt. |

### Bemerkungen

Das Dokument muss am Anfang des Streams gespeichert werden. Der Stream muss eine zufällige Positionierung unterstützen.

### Beispiele

Zeigt, wie der Inhalt eines verschlüsselten Microsoft Word-Dokuments mithilfe von Stream im Klartext geladen wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "PlainTextDocument.LoadFromStreamWithOptions.docx", saveOptions);

LoadOptions loadOptions = new LoadOptions();
loadOptions.Password = "MyPassword";

using (FileStream stream = new FileStream(ArtifactsDir + "PlainTextDocument.LoadFromStreamWithOptions.docx", FileMode.Open))
{
    PlainTextDocument plaintext = new PlainTextDocument(stream, loadOptions);

    Assert.AreEqual("Hello world!", plaintext.Text.Trim());
}
```

### Siehe auch

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [PlainTextDocument](../)
* namensraum [Aspose.Words](../../plaintextdocument/)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
