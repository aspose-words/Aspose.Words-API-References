---
title: PdfEncryptionDetails.Permissions
linktitle: Permissions
articleTitle: Permissions
second_title: Aspose.Words für .NET
description: PdfEncryptionDetails Permissions eigendom. Gibt die Vorgänge an die einem Benutzer für ein verschlüsseltes PDFDokument gestattet sind. Der Standardwert istDisallowAll  in C#.
type: docs
weight: 30
url: /de/net/aspose.words.saving/pdfencryptiondetails/permissions/
---
## PdfEncryptionDetails.Permissions property

Gibt die Vorgänge an, die einem Benutzer für ein verschlüsseltes PDF-Dokument gestattet sind. Der Standardwert istDisallowAll .

```csharp
public PdfPermissions Permissions { get; set; }
```

## Beispiele

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

* enum [PdfPermissions](../../pdfpermissions/)
* class [PdfEncryptionDetails](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
