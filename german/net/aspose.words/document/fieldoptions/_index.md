---
title: Document.FieldOptions
linktitle: FieldOptions
articleTitle: FieldOptions
second_title: Aspose.Words für .NET
description: Erkunden Sie die Eigenschaft „Dokument-Feldoptionen“, um die Feldverwaltung effektiv zu verwalten. Entdecken Sie einzigartige Optionen für verbesserte Dokumentkontrolle und -anpassung.
type: docs
weight: 130
url: /de/net/aspose.words/document/fieldoptions/
---
## Document.FieldOptions property

Erhält eine[`FieldOptions`](../../../aspose.words.fields/fieldoptions/) Objekt, das Optionen zur Steuerung der Feldbehandlung im Dokument darstellt.

```csharp
public FieldOptions FieldOptions { get; }
```

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

* class [FieldOptions](../../../aspose.words.fields/fieldoptions/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
