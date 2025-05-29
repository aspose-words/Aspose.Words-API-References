---
title: FieldOptions.FieldUpdateCultureSource
linktitle: FieldUpdateCultureSource
articleTitle: FieldUpdateCultureSource
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „FieldUpdateCultureSource“ die Formatierung von Feldergebnissen verbessert, indem sie die gewünschte Kultur für optimale Klarheit und Benutzerfreundlichkeit angibt.
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

Zeigt, wie die Quelle der Kultur angegeben wird, die während einer Feldaktualisierung oder eines Seriendrucks für die Datumsformatierung verwendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Zwei Seriendruckfelder mit deutscher Gebietseinstellung einfügen.
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// Stellen Sie die aktuelle Kultur auf US-Englisch ein, nachdem Sie den ursprünglichen Wert in einer Variablen beibehalten haben.
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// Bei dieser Zusammenführung wird die Kultur des aktuellen Threads (US-Englisch) zum Formatieren des Datums verwendet.
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// Konfigurieren Sie die nächste Zusammenführung so, dass der Kulturwert aus dem Feldcode stammt. Der Wert dieser Kultur ist Deutsch.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// Das erste Zusammenführungsergebnis enthält ein Datum im englischen Format, während das zweite im deutschen Format ist.
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

// Die ursprüngliche Kultur des Threads wiederherstellen.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### Siehe auch

* enum [FieldUpdateCultureSource](../../fieldupdateculturesource/)
* class [FieldOptions](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
