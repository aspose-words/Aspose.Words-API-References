---
title: PdfSaveOptions.EncryptionDetails
linktitle: EncryptionDetails
articleTitle: EncryptionDetails
second_title: Aspose.Words für .NET
description: Entdecken Sie die EncryptionDetails-Eigenschaft von PdfSaveOptions, um PDF-Verschlüsselungseinstellungen einfach zu konfigurieren und sicherzustellen, dass Ihre Dokumente sicher und geschützt bleiben.
type: docs
weight: 130
url: /de/net/aspose.words.saving/pdfsaveoptions/encryptiondetails/
---
## PdfSaveOptions.EncryptionDetails property

Ruft die Details zum Verschlüsseln des PDF-Ausgabedokuments ab oder legt sie fest.

```csharp
public PdfEncryptionDetails EncryptionDetails { get; set; }
```

## Bemerkungen

Der Standardwert ist`null` und das Ausgabedokument wird nicht verschlüsselt. Wenn diese Eigenschaft auf einen gültigen Wert gesetzt ist[`PdfEncryptionDetails`](../../pdfencryptiondetails/)object, , dann wird das ausgegebene PDF-Dokument verschlüsselt.

Beim Speichern im PDF 1.7-basierten Konformitätsmodus (einschließlich PDF/UA-1) wird der Verschlüsselungsalgorithmus AES-128 verwendet. Beim Speichern im PDF 2.0-basierten Konformitätsmodus wird der Verschlüsselungsalgorithmus AES-256 verwendet.

Die Verschlüsselung ist aufgrund der PDF/A-Konformität nicht zulässig. Diese Option wird beim Speichern im PDF/A-Format ignoriert.

ContentCopyForAccessibility Die Berechtigung ist gemäß PDF/UA-Konformität erforderlich, wenn das Ausgabedokument verschlüsselt ist. Diese Berechtigung wird beim Speichern im PDF/UA-Format automatisch verwendet.

ContentCopyForAccessibility Berechtigung ist im PDF 2.0-Format veraltet. Diese Berechtigung wird beim Speichern im PDF 2.0 ignoriert.

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

* class [PdfEncryptionDetails](../../pdfencryptiondetails/)
* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
