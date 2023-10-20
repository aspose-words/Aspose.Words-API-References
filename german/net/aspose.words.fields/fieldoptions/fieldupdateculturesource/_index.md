---
title: FieldOptions.FieldUpdateCultureSource
linktitle: FieldUpdateCultureSource
articleTitle: FieldUpdateCultureSource
second_title: Aspose.Words für .NET
description: FieldOptions FieldUpdateCultureSource eigendom. Gibt an welche Kultur zum Formatieren des Feldergebnisses verwendet werden soll in C#.
type: docs
weight: 110
url: /de/net/aspose.words.fields/fieldoptions/fieldupdateculturesource/
---
## FieldOptions.FieldUpdateCultureSource property

Gibt an, welche Kultur zum Formatieren des Feldergebnisses verwendet werden soll.

```csharp
public FieldUpdateCultureSource FieldUpdateCultureSource { get; set; }
```

## Bemerkungen

Standardmäßig wird die Kultur des aktuellen Threads verwendet.

Die Einstellung betrifft nur Datums-/Uhrzeitfelder mit dem Formatschalter \\@.

## Beispiele

Zeigt, wie Sie die Quelle der Kultur angeben, die für die Datumsformatierung während einer Feldaktualisierung oder eines Seriendrucks verwendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Zwei Zusammenführungsfelder mit deutschem Gebietsschema einfügen.
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// Setze die aktuelle Kultur auf US-Englisch, nachdem der ursprüngliche Wert in einer Variablen beibehalten wurde.
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// Bei dieser Zusammenführung wird die Kultur des aktuellen Threads verwendet, um das Datum zu formatieren, US-Englisch.
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// Konfigurieren Sie die nächste Zusammenführung so, dass ihr Kulturwert aus dem Feldcode stammt. Der Wert dieser Kultur wird deutsch sein.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// Das erste Zusammenführungsergebnis enthält ein in Englisch formatiertes Datum, während das zweite in Deutsch formatiert ist.
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

// Die ursprüngliche Kultur des Threads wiederherstellen.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### Siehe auch

* enum [FieldUpdateCultureSource](../../fieldupdateculturesource/)
* class [FieldOptions](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
