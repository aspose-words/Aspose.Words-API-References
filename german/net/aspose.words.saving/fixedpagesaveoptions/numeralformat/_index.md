---
title: FixedPageSaveOptions.NumeralFormat
second_title: Aspose.Words für .NET-API-Referenz
description: FixedPageSaveOptions eigendom. Holt oder setztNumeralFormat wird zur Darstellung von Ziffern verwendet. Europäische Ziffern werden standardmäßig verwendet.
type: docs
weight: 40
url: /de/net/aspose.words.saving/fixedpagesaveoptions/numeralformat/
---
## FixedPageSaveOptions.NumeralFormat property

Holt oder setzt[`NumeralFormat`](../../numeralformat/) wird zur Darstellung von Ziffern verwendet. Europäische Ziffern werden standardmäßig verwendet.

```csharp
public NumeralFormat NumeralFormat { get; set; }
```

### Bemerkungen

Wenn der Wert dieser Eigenschaft geändert wird und das Seitenlayout bereits erstellt ist, dann [`UpdatePageLayout`](../../../aspose.words/document/updatepagelayout/) wird automatisch aufgerufen, um alle Änderungen zu aktualisieren.

### Beispiele

Zeigt, wie das beim Speichern im PDF-Format verwendete Zahlenformat eingestellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.LocaleId = new CultureInfo("ar-AR").LCID;
builder.Writeln("1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 50, 100");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Legen Sie die Eigenschaft „NumeralFormat“ auf „NumeralFormat.ArabicIndic“ fest
// Glyphen aus dem Bereich U+0660 bis U+0669 als Zahlen verwenden.
// Legen Sie die Eigenschaft "NumeralFormat" auf "NumeralFormat.Context" fest
// Suchen Sie das Gebietsschema, um zu bestimmen, wie viele Glyphen verwendet werden sollen.
// Legen Sie die Eigenschaft „NumeralFormat“ auf „NumeralFormat.EasternArabicIndic“ fest
// Glyphen aus dem Bereich U+06F0 bis U+06F9 als Zahlen verwenden.
// Setzen Sie die Eigenschaft "NumeralFormat" auf "NumeralFormat.European", um europäische Ziffern zu verwenden.
// Legen Sie die Eigenschaft "NumeralFormat" auf "NumeralFormat.System" fest, um den Symbolsatz aus den regionalen Einstellungen zu ermitteln.
options.NumeralFormat = numeralFormat;

doc.Save(ArtifactsDir + "PdfSaveOptions.SetNumeralFormat.pdf", options);
```

### Siehe auch

* enum [NumeralFormat](../../numeralformat/)
* class [FixedPageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../fixedpagesaveoptions/)
* Montage [Aspose.Words](../../../)


