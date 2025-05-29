---
title: FileFormatInfo.IsEncrypted
linktitle: IsEncrypted
articleTitle: IsEncrypted
second_title: Aspose.Words für .NET
description: Ermitteln Sie mit der FileFormatInfo-Eigenschaft „IsEncrypted“, ob Ihr Dokument sicher ist. Sie gibt „true“ zurück, wenn für den Zugriff auf verschlüsselte Dateien ein Kennwort erforderlich ist.
type: docs
weight: 40
url: /de/net/aspose.words/fileformatinfo/isencrypted/
---
## FileFormatInfo.IsEncrypted property

Rückgaben`WAHR` wenn das Dokument verschlüsselt ist und zum Öffnen ein Kennwort erforderlich ist.

```csharp
public bool IsEncrypted { get; }
```

## Bemerkungen

Diese Eigenschaft hilft Ihnen, verschlüsselte von unverschlüsselten Dokumenten zu trennen. Wenn Sie versuchen, ein verschlüsseltes Dokument mit Aspose.Words ohne Angabe eines Kennworts zu laden, wird eine -Ausnahme ausgelöst. Mithilfe dieser Eigenschaft können Sie feststellen, ob für ein Dokument ein Kennwort erforderlich ist und vor dem Laden des Dokuments entsprechende Maßnahmen ergreifen, z. B. den Benutzer zur Kennworteingabe auffordern.

## Beispiele

Zeigt, wie die FileFormatUtil-Klasse zum Erkennen des Dokumentformats und der Verschlüsselung verwendet wird.

```csharp
Document doc = new Document();

// Konfigurieren Sie ein SaveOptions-Objekt, um das Dokument zu verschlüsseln
// mit einem Passwort, wenn wir es speichern, und speichern Sie dann das Dokument.
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// Überprüfen Sie den Dateityp unseres Dokuments und seinen Verschlüsselungsstatus.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDocumentEncryption.odt");

Assert.AreEqual(".odt", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.True(info.IsEncrypted);
```

### Siehe auch

* class [FileFormatInfo](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
