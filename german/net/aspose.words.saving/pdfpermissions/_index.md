---
title: PdfPermissions Enum
linktitle: PdfPermissions
articleTitle: PdfPermissions
second_title: Aspose.Words für .NET
description: Aspose.Words.Saving.PdfPermissions opsomming. Gibt die Vorgänge an die einem Benutzer für ein verschlüsseltes PDFDokument gestattet sind in C#.
type: docs
weight: 5510
url: /de/net/aspose.words.saving/pdfpermissions/
---
## PdfPermissions enumeration

Gibt die Vorgänge an, die einem Benutzer für ein verschlüsseltes PDF-Dokument gestattet sind.

```csharp
[Flags]
public enum PdfPermissions
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| DisallowAll | `0` | Verbietet alle Vorgänge am PDF-Dokument. Dies ist der Standardwert. |
| AllowAll | `FFFF` | Ermöglicht alle Vorgänge am PDF-Dokument. |
| ContentCopy | `10` | Kopieren oder extrahieren Sie Text und Grafiken anderweitig aus dem Dokument durch andere Vorgänge als die, die von gesteuert werdenContentCopyForAccessibility . |
| ContentCopyForAccessibility | `200` | Text und Grafiken extrahieren (zur Unterstützung der Barrierefreiheit für Benutzer mit Behinderungen oder für andere Zwecke). |
| ModifyContents | `8` | Ändern Sie den Inhalt des Dokuments durch andere Vorgänge als die, die von gesteuert werden.ModifyAnnotations ,FillIn , UndDocumentAssembly . |
| ModifyAnnotations | `20` | Textanmerkungen hinzufügen oder ändern, interaktive Formularfelder ausfüllen und ggfModifyContents is auch interaktive Formularfelder (einschließlich Signaturfelder) festlegen, erstellen oder ändern. |
| FillIn | `100` | Füllen Sie vorhandene interaktive Formularfelder (einschließlich Signaturfelder) aus, auch wennModifyContents ist klar. |
| DocumentAssembly | `400` | Bauen Sie das Dokument zusammen (fügen Sie Seiten ein, drehen Sie sie oder löschen Sie sie und erstellen Sie Dokumentgliederungselemente oder Miniaturbilder), auch wennModifyContents ist klar. |
| Printing | `4` | Drucken Sie das Dokument aus (evtl. nicht in der höchsten Qualitätsstufe, je nachdem, ob HighResolutionPrinting ist ebenfalls gesetzt). |
| HighResolutionPrinting | `804` | Drucken Sie das Dokument in einer Darstellung aus, aus der basierend auf einem implementierten Algorithmus eine originalgetreue digitale Kopie des PDF-Inhalts generiert werden könnte. Wenn dieses Flag gelöscht ist (and Printing festgelegt ist), soll das Drucken auf eine Darstellung des Erscheinungsbilds auf niedriger Ebene beschränkt sein, möglicherweise mit verminderter Qualität. |

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
