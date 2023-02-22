---
title: StructuredDocumentTag.CalendarType
second_title: Aspose.Words für .NET-API-Referenz
description: StructuredDocumentTag eigendom. Gibt den Kalendertyp dafür an SDT . Standard istDefault
type: docs
weight: 50
url: /de/net/aspose.words.markup/structureddocumenttag/calendartype/
---
## StructuredDocumentTag.CalendarType property

Gibt den Kalendertyp dafür an **SDT** . Standard istDefault

```csharp
public SdtCalendarType CalendarType { get; set; }
```

### Bemerkungen

Der Zugriff auf diese Eigenschaft funktioniert nur fürDate SDT-Typ.

Für alle anderen SDT-Typen tritt eine Ausnahme auf.

### Beispiele

Zeigt, wie der Benutzer aufgefordert wird, ein Datum mit einem strukturierten Dokument-Tag einzugeben.

```csharp
Document doc = new Document();

// Fügen Sie ein strukturiertes Dokument-Tag ein, das den Benutzer auffordert, ein Datum einzugeben.
// In Microsoft Word wird dieses Element als "Inhaltssteuerelement für die Datumsauswahl" bezeichnet.
// Wenn wir in Microsoft Word auf den Pfeil am rechten Ende dieses Tags klicken,
// Wir sehen ein Popup in Form eines anklickbaren Kalenders.
// Wir können dieses Popup verwenden, um ein Datum auszuwählen, das das Tag anzeigen soll.
StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.Date, MarkupLevel.Inline);

// Zeigt das Datum gemäß dem saudi-arabischen Gebietsschema an.
sdtDate.DateDisplayLocale = CultureInfo.GetCultureInfo("ar-SA").LCID;

// Legen Sie das Format fest, in dem das Datum angezeigt werden soll.
sdtDate.DateDisplayFormat = "dd MMMM, yyyy";
sdtDate.DateStorageFormat = SdtDateStorageFormat.DateTime;

// Zeigt das Datum gemäß dem Hijri-Kalender an.
sdtDate.CalendarType = SdtCalendarType.Hijri;

// Bevor der Benutzer ein Datum in Microsoft Word auswählt, zeigt das Tag den Text „Klicken Sie hier, um ein Datum einzugeben.“ an.
// Legen Sie gemäß dem Kalender des Tags die Eigenschaft "FullDate" fest, damit das Tag ein Standarddatum anzeigt.
sdtDate.FullDate = new DateTime(1440, 10, 20);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(sdtDate);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Date.docx");
```

### Siehe auch

* enum [SdtCalendarType](../../sdtcalendartype/)
* class [StructuredDocumentTag](../)
* namensraum [Aspose.Words.Markup](../../structureddocumenttag/)
* Montage [Aspose.Words](../../../)


