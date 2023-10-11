---
title: OdtSaveOptions.Password
second_title: Aspose.Words für .NET-API-Referenz
description: OdtSaveOptions eigendom. Ruft ein Passwort zum Verschlüsseln des Dokuments ab oder legt es fest.
type: docs
weight: 40
url: /de/net/aspose.words.saving/odtsaveoptions/password/
---
## OdtSaveOptions.Password property

Ruft ein Passwort zum Verschlüsseln des Dokuments ab oder legt es fest.

```csharp
public string Password { get; set; }
```

### Bemerkungen

Um ein Dokument ohne Verschlüsselung zu speichern, sollte diese Eigenschaft vorhanden sein`Null` oder leere Zeichenfolge.

### Beispiele

Zeigt, wie man ein gespeichertes ODT/OTT-Dokument mit einem Passwort verschlüsselt und es dann mit Aspose.Words lädt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Erstellen Sie eine neue OdtSaveOptions und übergeben Sie entweder „SaveFormat.Odt“,
 // oder „SaveFormat.Ott“ als Format zum Speichern des Dokuments.
OdtSaveOptions saveOptions = new OdtSaveOptions(saveFormat);
saveOptions.Password = "@sposeEncrypted_1145";

string extensionString = FileFormatUtil.SaveFormatToExtension(saveFormat);

// Wenn wir dieses Dokument mit einem geeigneten Editor öffnen,
// Es wird uns zur Eingabe des Passworts auffordern, das wir im SaveOptions-Objekt angegeben haben.
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
* namensraum [Aspose.Words.Saving](../../odtsaveoptions/)
* Montage [Aspose.Words](../../../)


