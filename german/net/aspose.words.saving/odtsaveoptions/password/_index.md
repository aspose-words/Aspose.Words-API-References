---
title: OdtSaveOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words für .NET
description: Sichern Sie Ihre Dokumente mit der OdtSaveOptions-Kennwortfunktion. Legen Sie einfach ein Kennwort fest oder rufen Sie es ab, um eine robuste Verschlüsselung und verbesserten Datenschutz zu gewährleisten.
type: docs
weight: 50
url: /de/net/aspose.words.saving/odtsaveoptions/password/
---
## OdtSaveOptions.Password property

Ruft ein Kennwort zum Verschlüsseln des Dokuments ab oder legt es fest.

```csharp
public string Password { get; set; }
```

## Bemerkungen

Um das Dokument unverschlüsselt zu speichern, sollte diese Eigenschaft`null` oder eine leere Zeichenfolge.

## Beispiele

Zeigt, wie Sie ein gespeichertes ODT/OTT-Dokument mit einem Kennwort verschlüsseln und es dann mit Aspose.Words laden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Erstellen Sie eine neue OdtSaveOptions und übergeben Sie entweder "SaveFormat.Odt",
    // oder „SaveFormat.Ott“ als Format, in dem das Dokument gespeichert werden soll.
OdtSaveOptions saveOptions = new OdtSaveOptions(saveFormat);
saveOptions.Password = "@sposeEncrypted_1145";

string extensionString = FileFormatUtil.SaveFormatToExtension(saveFormat);

// Wenn wir dieses Dokument mit einem entsprechenden Editor öffnen,
// Es fordert uns zur Eingabe des Passworts auf, das wir im SaveOptions-Objekt angegeben haben.
doc.Save(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString, saveOptions);

FileFormatInfo docInfo = FileFormatUtil.DetectFileFormat(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString);

Assert.IsTrue(docInfo.IsEncrypted);

// Wenn wir dieses Dokument erneut mit Aspose.Words öffnen oder bearbeiten möchten,
// Wir müssen dem Ladekonstruktor ein LoadOptions-Objekt mit dem richtigen Passwort bereitstellen.
doc = new Document(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString,
    new LoadOptions("@sposeEncrypted_1145"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Siehe auch

* class [OdtSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
