---
title: PdfSaveOptions.EncryptionDetails
linktitle: EncryptionDetails
articleTitle: EncryptionDetails
second_title: Aspose.Words für .NET
description: PdfSaveOptions EncryptionDetails eigendom. Ruft die Details zum Verschlüsseln des ausgegebenen PDFDokuments ab oder legt diese fest in C#.
type: docs
weight: 130
url: /de/net/aspose.words.saving/pdfsaveoptions/encryptiondetails/
---
## PdfSaveOptions.EncryptionDetails property

Ruft die Details zum Verschlüsseln des ausgegebenen PDF-Dokuments ab oder legt diese fest.

```csharp
public PdfEncryptionDetails EncryptionDetails { get; set; }
```

## Bemerkungen

Der Standardwert ist`Null` und das Ausgabedokument wird nicht verschlüsselt. Wenn diese Eigenschaft auf einen gültigen Wert gesetzt ist[`PdfEncryptionDetails`](../../pdfencryptiondetails/) object, dann wird das ausgegebene PDF-Dokument verschlüsselt.

Der AES-128-Verschlüsselungsalgorithmus wird beim Speichern in einer auf PDF 1.7 basierenden Kompatibilität (einschließlich PDF/UA-1) verwendet. Der AES-256-Verschlüsselungsalgorithmus wird beim Speichern in einer auf PDF 2.0 basierenden Kompatibilität verwendet.

Die Verschlüsselung ist durch die PDF/A-Konformität verboten. Diese Option wird beim Speichern in PDF/A ignoriert.

ContentCopyForAccessibility Die Berechtigung ist gemäß PDF/UA-Compliance erforderlich, wenn das Ausgabedokument verschlüsselt ist. Diese Berechtigung wird beim Speichern in PDF/UA automatisch verwendet.

ContentCopyForAccessibility Die Berechtigung ist im PDF 2.0-Format veraltet. Diese Berechtigung wird beim Speichern in PDF 2.0 ignoriert.

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

* class [PdfEncryptionDetails](../../pdfencryptiondetails/)
* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
