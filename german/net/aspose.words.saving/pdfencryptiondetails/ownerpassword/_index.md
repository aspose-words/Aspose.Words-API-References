---
title: PdfEncryptionDetails.OwnerPassword
second_title: Aspose.Words für .NET-API-Referenz
description: PdfEncryptionDetails eigendom. Gibt das Besitzerkennwort für das verschlüsselte PDFDokument an.
type: docs
weight: 20
url: /de/net/aspose.words.saving/pdfencryptiondetails/ownerpassword/
---
## PdfEncryptionDetails.OwnerPassword property

Gibt das Besitzerkennwort für das verschlüsselte PDF-Dokument an.

```csharp
public string OwnerPassword { get; set; }
```

### Bemerkungen

Mit dem Besitzerkennwort kann der Benutzer ein verschlüsseltes PDF-Dokument ohne die in angegebenen Zugriffsbeschränkungen öffnen[`Permissions`](../permissions/).

Das Besitzerpasswort darf nicht mit dem Benutzerpasswort identisch sein.

### Beispiele

Zeigt, wie Berechtigungen für ein gespeichertes PDF-Dokument festgelegt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// Berechtigungen erweitern, um das Bearbeiten von Anmerkungen zu ermöglichen.
PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty, PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly);

// Erstellen Sie ein „PdfSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// Verschlüsselung über die Eigenschaft „EncryptionDetails“ aktivieren.
saveOptions.EncryptionDetails = encryptionDetails;

// Wenn wir dieses Dokument öffnen, müssen wir das Passwort angeben, bevor wir auf den Inhalt zugreifen können.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### Siehe auch

* class [PdfEncryptionDetails](../)
* namensraum [Aspose.Words.Saving](../../pdfencryptiondetails/)
* Montage [Aspose.Words](../../../)


