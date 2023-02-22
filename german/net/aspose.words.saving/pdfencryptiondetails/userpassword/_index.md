---
title: PdfEncryptionDetails.UserPassword
second_title: Aspose.Words für .NET-API-Referenz
description: PdfEncryptionDetails eigendom. Gibt das Benutzerkennwort an das zum Öffnen des verschlüsselten PDFDokuments erforderlich ist.
type: docs
weight: 40
url: /de/net/aspose.words.saving/pdfencryptiondetails/userpassword/
---
## PdfEncryptionDetails.UserPassword property

Gibt das Benutzerkennwort an, das zum Öffnen des verschlüsselten PDF-Dokuments erforderlich ist.

```csharp
public string UserPassword { get; set; }
```

### Bemerkungen

Das Benutzerpasswort wird benötigt, um ein verschlüsseltes PDF-Dokument zum Anzeigen zu öffnen. Die in angegebenen Berechtigungen[`Permissions`](../permissions/) wird von der Lesesoftware erzwungen.

Das Benutzerpasswort kann null oder eine leere Zeichenkette sein, in diesem Fall wird vom Benutzer kein Passwort verlangt, wenn das PDF-Dokument öffnet. Das Benutzerpasswort darf nicht mit dem Besitzerpasswort identisch sein.

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

* class [PdfEncryptionDetails](../)
* namensraum [Aspose.Words.Saving](../../pdfencryptiondetails/)
* Montage [Aspose.Words](../../../)


