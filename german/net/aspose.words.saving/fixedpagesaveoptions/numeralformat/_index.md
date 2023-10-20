---
title: FixedPageSaveOptions.NumeralFormat
linktitle: NumeralFormat
articleTitle: NumeralFormat
second_title: Aspose.Words für .NET
description: FixedPageSaveOptions NumeralFormat eigendom. Ruft ab oder legt festNumeralFormat Wird zur Darstellung von Ziffern verwendet. Standardmäßig werden europäische Ziffern verwendet in C#.
type: docs
weight: 40
url: /de/net/aspose.words.saving/fixedpagesaveoptions/numeralformat/
---
## FixedPageSaveOptions.NumeralFormat property

Ruft ab oder legt fest[`NumeralFormat`](../../numeralformat/) Wird zur Darstellung von Ziffern verwendet. Standardmäßig werden europäische Ziffern verwendet.

```csharp
public NumeralFormat NumeralFormat { get; set; }
```

## Bemerkungen

Wenn der Wert dieser Eigenschaft geändert wird und das Seitenlayout bereits erstellt wurde, dann [`UpdatePageLayout`](../../../aspose.words/document/updatepagelayout/) wird automatisch aufgerufen, um alle Änderungen zu aktualisieren.

## Beispiele

Zeigt, wie das beim Speichern als PDF verwendete Zahlenformat festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.LocaleId = new CultureInfo("ar-AR").LCID;
builder.Writeln("1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 50, 100");

// Erstellen Sie ein „PdfSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Setzen Sie die Eigenschaft „NumeralFormat“ auf „NumeralFormat.ArabicIndic“.
// Glyphen aus dem Bereich U+0660 bis U+0669 als Zahlen verwenden.
// Setzen Sie die Eigenschaft „NumeralFormat“ auf „NumeralFormat.Context“.
// Schauen Sie sich das Gebietsschema an, um zu bestimmen, wie viele Glyphen verwendet werden sollen.
// Setzen Sie die Eigenschaft „NumeralFormat“ auf „NumeralFormat.EasternArabicIndic“.
// Glyphen aus dem Bereich U+06F0 bis U+06F9 als Zahlen verwenden.
// Setzen Sie die Eigenschaft „NumeralFormat“ auf „NumeralFormat.European“, um europäische Ziffern zu verwenden.
// Setzen Sie die Eigenschaft „NumeralFormat“ auf „NumeralFormat.System“, um den Symbolsatz anhand der regionalen Einstellungen zu bestimmen.
options.NumeralFormat = numeralFormat;

doc.Save(ArtifactsDir + "PdfSaveOptions.SetNumeralFormat.pdf", options);
```

### Siehe auch

* enum [NumeralFormat](../../numeralformat/)
* class [FixedPageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
