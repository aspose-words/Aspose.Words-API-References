---
title: PlainTextDocument
linktitle: PlainTextDocument
articleTitle: PlainTextDocument
second_title: Aspose.Words für .NET
description: Erstellen Sie mühelos reine Textdokumente mit unserem PlainTextDocument-Konstruktor. Profitieren Sie von der automatischen Dateiformaterkennung für eine nahtlose Integration!
type: docs
weight: 10
url: /de/net/aspose.words/plaintextdocument/plaintextdocument/
---
## PlainTextDocument(*string*) {#constructor_2}

Erstellt ein reines Textdokument aus einer Datei. Das Dateiformat wird automatisch erkannt.

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
| Exception | Es liegt ein Problem mit dem Dokument vor und sollte den Entwicklern von Aspose.Words gemeldet werden. |
| IOException | Es liegt eine Eingabe-/Ausgabeausnahme vor. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Das Dokument ist verschlüsselt und erfordert zum Öffnen ein Kennwort, Sie haben jedoch ein falsches Kennwort eingegeben. |
| ArgumentException | Der Name der Datei darf nicht null oder eine leere Zeichenfolge sein. |

## Beispiele

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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## PlainTextDocument(*string, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_3}

Erstellt ein reines Textdokument aus einer Datei. Ermöglicht die Angabe zusätzlicher Optionen wie z. B. eines Verschlüsselungskennworts.

```csharp
public PlainTextDocument(string fileName, LoadOptions loadOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Name der Datei, aus der der Text extrahiert werden soll. |
| loadOptions | LoadOptions | Zusätzliche Optionen beim Laden eines Dokuments. Kann sein`null`. |

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Das Dokumentformat wird nicht erkannt oder nicht unterstützt. |
| [FileCorruptedException](../../filecorruptedexception/) | Das Dokument scheint beschädigt zu sein und kann nicht geladen werden. |
| Exception | Es liegt ein Problem mit dem Dokument vor und sollte den Entwicklern von Aspose.Words gemeldet werden. |
| IOException | Es liegt eine Eingabe-/Ausgabeausnahme vor. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Das Dokument ist verschlüsselt und erfordert zum Öffnen ein Kennwort, Sie haben jedoch ein falsches Kennwort eingegeben. |
| ArgumentException | Der Name der Datei darf nicht null oder eine leere Zeichenfolge sein. |

## Beispiele

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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## PlainTextDocument(*Stream*) {#constructor}

Erstellt ein reines Textdokument aus einem Stream. Das Dateiformat wird automatisch erkannt.

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
| Exception | Es liegt ein Problem mit dem Dokument vor und sollte den Entwicklern von Aspose.Words gemeldet werden. |
| IOException | Es liegt eine Eingabe-/Ausgabeausnahme vor. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Das Dokument ist verschlüsselt und erfordert zum Öffnen ein Kennwort, Sie haben jedoch ein falsches Kennwort eingegeben. |
| ArgumentNullException | Der Stream darf nicht null sein. |
| NotSupportedException | Der Stream unterstützt weder Lesen noch Suchen. |
| ObjectDisposedException | Der Stream ist ein verworfenes Objekt. |

## Bemerkungen

Das Dokument muss am Anfang des Streams gespeichert werden. Der Stream muss eine zufällige Positionierung unterstützen.

## Beispiele

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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## PlainTextDocument(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_1}

Erstellt ein reines Textdokument aus einem Stream. Ermöglicht die Angabe zusätzlicher Optionen wie z. B. eines Verschlüsselungskennworts.

```csharp
public PlainTextDocument(Stream stream, LoadOptions loadOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | Stream | Der Stream, aus dem der Text extrahiert werden soll. |
| loadOptions | LoadOptions | Zusätzliche Optionen beim Laden eines Dokuments. Kann sein`null`. |

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Das Dokumentformat wird nicht erkannt oder nicht unterstützt. |
| [FileCorruptedException](../../filecorruptedexception/) | Das Dokument scheint beschädigt zu sein und kann nicht geladen werden. |
| Exception | Es liegt ein Problem mit dem Dokument vor und sollte den Entwicklern von Aspose.Words gemeldet werden. |
| IOException | Es liegt eine Eingabe-/Ausgabeausnahme vor. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Das Dokument ist verschlüsselt und erfordert zum Öffnen ein Kennwort, Sie haben jedoch ein falsches Kennwort eingegeben. |
| ArgumentNullException | Der Stream darf nicht null sein. |
| NotSupportedException | Der Stream unterstützt weder Lesen noch Suchen. |
| ObjectDisposedException | Der Stream ist ein verworfenes Objekt. |

## Bemerkungen

Das Dokument muss am Anfang des Streams gespeichert werden. Der Stream muss eine zufällige Positionierung unterstützen.

## Beispiele

Zeigt, wie der Inhalt eines verschlüsselten Microsoft Word-Dokuments mithilfe eines Streams im Klartext geladen wird.

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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
