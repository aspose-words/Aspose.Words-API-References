---
title: FixedPageSaveOptions.NumeralFormat
linktitle: NumeralFormat
articleTitle: NumeralFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „FixedPageSaveOptions NumeralFormat“, um die Zifferndarstellung anzupassen. Wechseln Sie einfach zu europäischen Ziffern für eine verbesserte Dokumentdarstellung.
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

Wenn der Wert dieser Eigenschaft geändert wird und das Seitenlayout bereits erstellt ist, dann [`UpdatePageLayout`](../../../aspose.words/document/updatepagelayout/) wird automatisch aufgerufen, um alle Änderungen zu aktualisieren.

## Beispiele

Zeigt, wie das beim Speichern im PDF-Format verwendete Zahlenformat eingestellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.LocaleId = new CultureInfo("ar-AR").LCID;
builder.Writeln("1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 50, 100");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Setzen Sie die Eigenschaft „NumeralFormat“ auf „NumeralFormat.ArabicIndic“, um
// Verwenden Sie Glyphen aus dem Bereich U+0660 bis U+0669 als Zahlen.
// Setzen Sie die Eigenschaft "NumeralFormat" auf "NumeralFormat.Context" auf
// Suchen Sie nach dem Gebietsschema, um zu bestimmen, wie viele Glyphen verwendet werden sollen.
// Setzen Sie die Eigenschaft „NumeralFormat“ auf „NumeralFormat.EasternArabicIndic“ auf
// Verwenden Sie Glyphen aus dem Bereich U+06F0 bis U+06F9 als Zahlen.
// Setzen Sie die Eigenschaft „NumeralFormat“ auf „NumeralFormat.European“, um europäische Ziffern zu verwenden.
// Setzen Sie die Eigenschaft „NumeralFormat“ auf „NumeralFormat.System“, um den Symbolsatz aus den regionalen Einstellungen zu bestimmen.
options.NumeralFormat = numeralFormat;

doc.Save(ArtifactsDir + "PdfSaveOptions.SetNumeralFormat.pdf", options);
```

### Siehe auch

* enum [NumeralFormat](../../numeralformat/)
* class [FixedPageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
