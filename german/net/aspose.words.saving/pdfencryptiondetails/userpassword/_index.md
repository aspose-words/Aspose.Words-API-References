---
title: PdfEncryptionDetails.UserPassword
linktitle: UserPassword
articleTitle: UserPassword
second_title: Aspose.Words für .NET
description: PdfEncryptionDetails UserPassword eigendom. Gibt das Benutzerpasswort an das zum Öffnen des verschlüsselten PDFDokuments erforderlich ist in C#.
type: docs
weight: 40
url: /de/net/aspose.words.saving/pdfencryptiondetails/userpassword/
---
## PdfEncryptionDetails.UserPassword property

Gibt das Benutzerpasswort an, das zum Öffnen des verschlüsselten PDF-Dokuments erforderlich ist.

```csharp
public string UserPassword { get; set; }
```

## Bemerkungen

Um ein verschlüsseltes PDF-Dokument zur Ansicht zu öffnen, ist das Benutzerpasswort erforderlich. Die in angegebenen Berechtigungen[`Permissions`](../permissions/) wird von der Lesesoftware erzwungen.

Das Benutzerpasswort kann sein`Null` oder eine leere Zeichenfolge. In diesem Fall ist beim Öffnen des PDF-Dokuments kein Kennwort vom Benutzer erforderlich. Das Benutzerpasswort darf nicht mit dem Besitzerpasswort identisch sein.

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

* class [PdfEncryptionDetails](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
