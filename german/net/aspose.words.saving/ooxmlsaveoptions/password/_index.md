---
title: OoxmlSaveOptions.Password
second_title: Aspose.Words für .NET-API-Referenz
description: OoxmlSaveOptions eigendom. Ruft ein Passwort zum Verschlüsseln des Dokuments mit dem StandardVerschlüsselungsalgorithmus ECMA376 ab bzw. legt es fest.
type: docs
weight: 50
url: /de/net/aspose.words.saving/ooxmlsaveoptions/password/
---
## OoxmlSaveOptions.Password property

Ruft ein Passwort zum Verschlüsseln des Dokuments mit dem Standard-Verschlüsselungsalgorithmus ECMA376 ab bzw. legt es fest.

```csharp
public string Password { get; set; }
```

### Bemerkungen

Um ein Dokument ohne Verschlüsselung zu speichern, sollte diese Eigenschaft vorhanden sein`Null` oder leere Zeichenfolge.

### Beispiele

Zeigt, wie ein kennwortverschlüsseltes Office Open XML-Dokument erstellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Password.docx", saveOptions);

// Wir können dieses Dokument nicht mit Microsoft Word oder öffnen
// Aspose.Words ohne Angabe des richtigen Passworts.
Assert.Throws<IncorrectPasswordException>(() =>
    doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Password.docx"));

// Öffnen Sie das verschlüsselte Dokument, indem Sie das richtige Passwort in einem LoadOptions-Objekt übergeben.
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Password.docx", new LoadOptions("MyPassword"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Siehe auch

* class [OoxmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../ooxmlsaveoptions/)
* Montage [Aspose.Words](../../../)


