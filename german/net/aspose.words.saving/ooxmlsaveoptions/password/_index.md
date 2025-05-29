---
title: OoxmlSaveOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words für .NET
description: Sichern Sie Ihre Dokumente mit OoxmlSaveOptions! Legen Sie einfach ein Passwort für die Verschlüsselung nach ECMA376-Standard fest und sorgen Sie so für erhöhten Datenschutz.
type: docs
weight: 60
url: /de/net/aspose.words.saving/ooxmlsaveoptions/password/
---
## OoxmlSaveOptions.Password property

Ruft ein Kennwort ab bzw. legt ein Kennwort fest, um das Dokument mit dem Standardverschlüsselungsalgorithmus ECMA376 zu verschlüsseln.

```csharp
public string Password { get; set; }
```

## Bemerkungen

Um das Dokument unverschlüsselt zu speichern, sollte diese Eigenschaft`null` oder eine leere Zeichenfolge.

## Beispiele

Zeigt, wie ein kennwortverschlüsseltes Office Open XML-Dokument erstellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Password.docx", saveOptions);

// Wir können dieses Dokument nicht mit Microsoft Word öffnen oder
// Aspose.Words ohne Angabe des richtigen Passworts.
Assert.Throws<IncorrectPasswordException>(() =>
    doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Password.docx"));

// Öffnen Sie das verschlüsselte Dokument, indem Sie das richtige Passwort in einem LoadOptions-Objekt übergeben.
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Password.docx", new LoadOptions("MyPassword"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Siehe auch

* class [OoxmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
