---
title: FileFormatInfo.IsEncrypted
second_title: Aspose.Words für .NET-API-Referenz
description: FileFormatInfo eigendom. Gibt zurückWAHR wenn das Dokument verschlüsselt ist und zum Öffnen ein Passwort erfordert.
type: docs
weight: 30
url: /de/net/aspose.words/fileformatinfo/isencrypted/
---
## FileFormatInfo.IsEncrypted property

Gibt zurück`WAHR` wenn das Dokument verschlüsselt ist und zum Öffnen ein Passwort erfordert.

```csharp
public bool IsEncrypted { get; }
```

### Bemerkungen

Diese Eigenschaft hilft Ihnen dabei, verschlüsselte Dokumente von nicht verschlüsselten Dokumenten zu unterscheiden. Wenn Sie versuchen, ein verschlüsseltes Dokument mit Aspose.Words zu laden, ohne ein Kennwort anzugeben, wird eine -Ausnahme ausgelöst. Mit dieser Eigenschaft können Sie erkennen, ob für ein Dokument ein Kennwort erforderlich ist, und vor dem Laden eines Dokuments Maßnahmen ergreifen, beispielsweise den Benutzer zur Eingabe eines Kennworts auffordern.

### Beispiele

Zeigt, wie die FileFormatUtil-Klasse verwendet wird, um das Dokumentformat und die Verschlüsselung zu erkennen.

```csharp
Document doc = new Document();

// Konfigurieren Sie ein SaveOptions-Objekt, um das Dokument zu verschlüsseln
// mit einem Passwort, wenn wir es speichern, und dann das Dokument speichern.
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
* namensraum [Aspose.Words](../../fileformatinfo/)
* Montage [Aspose.Words](../../../)


