---
title: SdtDateStorageFormat Enum
linktitle: SdtDateStorageFormat
articleTitle: SdtDateStorageFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Aspose.Words.Markup.SdtDateStorageFormat die Datumsverarbeitung in SDTs verbessert und eine nahtlose XML-Datenintegration in Ihre Dokumente gewährleistet.
type: docs
weight: 4700
url: /de/net/aspose.words.markup/sdtdatestorageformat/
---
## SdtDateStorageFormat enumeration

Gibt an, wie das Datum für ein Datums-SDT gespeichert/abgerufen wird, wenn das SDT an einen XML-Knoten im Datenspeicher des Dokuments gebunden ist.

```csharp
public enum SdtDateStorageFormat
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Date | `0` | Der Datumswert für ein Datums-SDT wird als Datum im standardmäßigen XML-Schema-Datumsformat gespeichert. |
| DateTime | `1` | Der Datumswert für ein Datums-SDT wird als Datum im standardmäßigen DateTime-Format des XML-Schemas gespeichert. |
| Text | `2` | Der Datumswert für ein Datums-SDT wird als Text gespeichert. |
| Default | `1` | StandardmäßigDateTime |

## Beispiele

Zeigt, wie der Benutzer mit einem strukturierten Dokument-Tag zur Eingabe eines Datums aufgefordert wird.

```csharp
Document doc = new Document();

// Fügen Sie ein strukturiertes Dokument-Tag ein, das den Benutzer auffordert, ein Datum einzugeben.
// In Microsoft Word wird dieses Element als „Datumsauswahl-Inhaltssteuerelement“ bezeichnet.
// Wenn wir in Microsoft Word auf den Pfeil am rechten Ende dieses Tags klicken,
// Wir sehen ein Popup in Form eines anklickbaren Kalenders.
// Wir können dieses Popup verwenden, um ein Datum auszuwählen, das das Tag anzeigen soll.
StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.Date, MarkupLevel.Inline);

// Zeigt das Datum entsprechend der saudi-arabischen Landeseinstellung an.
sdtDate.DateDisplayLocale = CultureInfo.GetCultureInfo("ar-SA").LCID;

// Legen Sie das Format fest, in dem das Datum angezeigt werden soll.
sdtDate.DateDisplayFormat = "dd MMMM, yyyy";
sdtDate.DateStorageFormat = SdtDateStorageFormat.DateTime;

// Zeigt das Datum gemäß dem Hijri-Kalender an.
sdtDate.CalendarType = SdtCalendarType.Hijri;

// Bevor der Benutzer in Microsoft Word ein Datum auswählt, zeigt das Tag den Text „Klicken Sie hier, um ein Datum einzugeben.“ an.
// Legen Sie entsprechend dem Kalender des Tags die Eigenschaft „FullDate“ fest, damit das Tag ein Standarddatum anzeigt.
sdtDate.FullDate = new DateTime(1440, 10, 20);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(sdtDate);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Date.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Markup](../../aspose.words.markup/)
* Montage [Aspose.Words](../../)
