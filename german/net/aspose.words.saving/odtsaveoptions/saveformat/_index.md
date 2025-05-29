---
title: OdtSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie mit der SaveFormat-Eigenschaft von OdtSaveOptions Dokumente einfach in den Formaten Odt oder Ott speichern und so Kompatibilität und Flexibilität gewährleisten können.
type: docs
weight: 60
url: /de/net/aspose.words.saving/odtsaveoptions/saveformat/
---
## OdtSaveOptions.SaveFormat property

Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroptionsobjekt verwendet wird. Kann seinOdt oderOtt .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [OdtSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
