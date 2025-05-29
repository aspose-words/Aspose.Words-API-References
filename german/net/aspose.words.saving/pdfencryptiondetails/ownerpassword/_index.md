---
title: PdfEncryptionDetails.OwnerPassword
linktitle: OwnerPassword
articleTitle: OwnerPassword
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die OwnerPassword-Funktion Ihre verschlüsselten PDF-Dateien schützt und nur autorisierten Zugriff gewährleistet. Schützen Sie Ihre Dokumente mühelos!
type: docs
weight: 20
url: /de/net/aspose.words.saving/pdfencryptiondetails/ownerpassword/
---
## PdfEncryptionDetails.OwnerPassword property

Gibt das Besitzerkennwort für das verschlüsselte PDF-Dokument an.

```csharp
public string OwnerPassword { get; set; }
```

## Bemerkungen

Das Besitzerkennwort ermöglicht dem Benutzer das Öffnen eines verschlüsselten PDF-Dokuments ohne jegliche Zugriffsbeschränkungen , die in[`Permissions`](../permissions/).

Das Besitzerkennwort darf nicht mit dem Benutzerkennwort identisch sein.

## Beispiele

Zeigt, wie Berechtigungen für ein gespeichertes PDF-Dokument festgelegt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// Erweitern Sie die Berechtigungen, um das Bearbeiten von Anmerkungen zu ermöglichen.
PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty, PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly);

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// Aktivieren Sie die Verschlüsselung über die Eigenschaft „EncryptionDetails“.
saveOptions.EncryptionDetails = encryptionDetails;

// Wenn wir dieses Dokument öffnen, müssen wir das Passwort eingeben, bevor wir auf seinen Inhalt zugreifen können.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### Siehe auch

* class [PdfEncryptionDetails](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
