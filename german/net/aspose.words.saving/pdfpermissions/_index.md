---
title: Enum PdfPermissions
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.PdfPermissions opsomming. Gibt die Operationen an die einem Benutzer an einem verschlüsselten PDFDokument erlaubt sind.
type: docs
weight: 5230
url: /de/net/aspose.words.saving/pdfpermissions/
---
## PdfPermissions enumeration

Gibt die Operationen an, die einem Benutzer an einem verschlüsselten PDF-Dokument erlaubt sind.

```csharp
[Flags]
public enum PdfPermissions
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| DisallowAll | `0` | Verbietet alle Operationen auf dem PDF-Dokument. Dies ist der Standardwert. |
| AllowAll | `FFFF` | Lässt alle Operationen auf dem PDF-Dokument zu. |
| ContentCopy | `10` | Kopieren oder anderweitiges Extrahieren von Text und Grafiken aus dem Dokument durch andere Vorgänge als die, die von gesteuert werdenContentCopyForAccessibility . |
| ContentCopyForAccessibility | `200` | Text und Grafiken extrahieren (zur Unterstützung der Zugänglichkeit für Benutzer mit Behinderungen oder für andere Zwecke). |
| ModifyContents | `8` | Ändern Sie den Inhalt des Dokuments durch andere Operationen als die, die von gesteuert werdenModifyAnnotations ,FillIn , undDocumentAssembly . |
| ModifyAnnotations | `20` | Textanmerkungen hinzufügen oder ändern, interaktive Formularfelder ausfüllen und ggfModifyContents is setzt, erstellt oder ändert auch interaktive Formularfelder (einschließlich Signaturfelder). |
| FillIn | `100` | Füllen Sie vorhandene interaktive Formularfelder (einschließlich Unterschriftsfelder) aus, auch wennModifyContents ist frei. |
| DocumentAssembly | `400` | Stellen Sie das Dokument zusammen (fügen Sie Seiten ein, drehen oder löschen Sie sie und erstellen Sie Gliederungselemente oder Thumbnail -Bilder), auch wennModifyContents ist klar. |
| Printing | `4` | Drucken Sie das Dokument (möglicherweise nicht in der höchsten Qualitätsstufe, je nachdem, ob HighResolutionPrintingist ebenfalls gesetzt). |
| HighResolutionPrinting | `804` | Drucken Sie das Dokument zu einer Darstellung aus, aus der basierend auf einem implementierungsabhängigen Algorithmus eine originalgetreue digitale Kopie des PDF-Inhalts erzeugt werden könnte. Wenn dieses Flag gelöscht ist (and Printing festgelegt ist), muss der Druck auf eine Darstellung des Aussehens auf niedriger Ebene beschränkt sein, möglicherweise von verschlechterter Qualität. |

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)


