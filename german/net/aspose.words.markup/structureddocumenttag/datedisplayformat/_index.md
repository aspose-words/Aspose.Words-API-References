---
title: StructuredDocumentTag.DateDisplayFormat
linktitle: DateDisplayFormat
articleTitle: DateDisplayFormat
second_title: Aspose.Words für .NET
description: StructuredDocumentTag DateDisplayFormat eigendom. Zeichenfolge die das Format darstellt in dem Datumsangaben angezeigt werden. Kann nicht seinNull . Das Datum für Englisch USA ist mm/tt/jjjj in C#.
type: docs
weight: 90
url: /de/net/aspose.words.markup/structureddocumenttag/datedisplayformat/
---
## StructuredDocumentTag.DateDisplayFormat property

Zeichenfolge, die das Format darstellt, in dem Datumsangaben angezeigt werden. Kann nicht sein`Null` . Das Datum für Englisch (USA) ist „mm/tt/jjjj“.

```csharp
public string DateDisplayFormat { get; set; }
```

## Bemerkungen

Der Zugriff auf diese Eigenschaft funktioniert nur fürDate SDT-Typ.

Bei allen anderen SDT-Typen tritt eine Ausnahme auf.

## Beispiele

Zeigt, wie der Benutzer mit einem strukturierten Dokument-Tag zur Eingabe eines Datums aufgefordert wird.

```csharp
Document doc = new Document();

// Fügen Sie ein strukturiertes Dokument-Tag ein, das den Benutzer zur Eingabe eines Datums auffordert.
// In Microsoft Word wird dieses Element als „Inhaltssteuerelement für die Datumsauswahl“ bezeichnet.
// Wenn wir in Microsoft Word auf den Pfeil am rechten Ende dieses Tags klicken,
// Wir sehen ein Popup in Form eines anklickbaren Kalenders.
// Wir können dieses Popup verwenden, um ein Datum auszuwählen, das das Tag anzeigen soll.
StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.Date, MarkupLevel.Inline);

// Zeigt das Datum entsprechend der saudi-arabischen Arabisch-Sprache an.
sdtDate.DateDisplayLocale = CultureInfo.GetCultureInfo("ar-SA").LCID;

// Legen Sie das Format fest, in dem das Datum angezeigt werden soll.
sdtDate.DateDisplayFormat = "dd MMMM, yyyy";
sdtDate.DateStorageFormat = SdtDateStorageFormat.DateTime;

// Zeigt das Datum gemäß dem Hijri-Kalender an.
sdtDate.CalendarType = SdtCalendarType.Hijri;

// Bevor der Benutzer ein Datum in Microsoft Word auswählt, zeigt das Tag den Text „Klicken Sie hier, um ein Datum einzugeben.“ an.
// Legen Sie entsprechend dem Kalender des Tags die Eigenschaft „FullDate“ fest, damit das Tag ein Standarddatum anzeigt.
sdtDate.FullDate = new DateTime(1440, 10, 20);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(sdtDate);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Date.docx");
```

### Siehe auch

* class [StructuredDocumentTag](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
