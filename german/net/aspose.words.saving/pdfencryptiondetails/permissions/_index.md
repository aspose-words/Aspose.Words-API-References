---
title: PdfEncryptionDetails.Permissions
second_title: Aspose.Words für .NET-API-Referenz
description: PdfEncryptionDetails eigendom. Gibt die Operationen an die einem Benutzer an einem verschlüsselten PDFDokument erlaubt sind. Der Standardwert istDisallowAll .
type: docs
weight: 30
url: /de/net/aspose.words.saving/pdfencryptiondetails/permissions/
---
## PdfEncryptionDetails.Permissions property

Gibt die Operationen an, die einem Benutzer an einem verschlüsselten PDF-Dokument erlaubt sind. Der Standardwert istDisallowAll .

```csharp
public PdfPermissions Permissions { get; set; }
```

### Beispiele

Zeigt, wie Berechtigungen für ein gespeichertes PDF-Dokument festgelegt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty);

// Beginnen Sie damit, alle Berechtigungen zu verweigern.
encryptionDetails.Permissions = PdfPermissions.DisallowAll;

// Berechtigungen erweitern, um die Bearbeitung von Anmerkungen zu ermöglichen.
encryptionDetails.Permissions = PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly;

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Verschlüsselung über die Eigenschaft "EncryptionDetails" aktivieren.
saveOptions.EncryptionDetails = encryptionDetails;

// Wenn wir dieses Dokument öffnen, müssen wir das Passwort angeben, bevor wir auf seinen Inhalt zugreifen können.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### Siehe auch

* enum [PdfPermissions](../../pdfpermissions/)
* class [PdfEncryptionDetails](../)
* namensraum [Aspose.Words.Saving](../../pdfencryptiondetails/)
* Montage [Aspose.Words](../../../)


