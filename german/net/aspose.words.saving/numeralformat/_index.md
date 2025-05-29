---
title: NumeralFormat Enum
linktitle: NumeralFormat
articleTitle: NumeralFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.Saving.NumeralFormat Enumeration für optimale Zahlendarstellung in festen Seitenformaten. Verbessern Sie noch heute die Darstellung Ihrer Dokumente!
type: docs
weight: 6090
url: /de/net/aspose.words.saving/numeralformat/
---
## NumeralFormat enumeration

Gibt den Symbolsatz an, der zur Darstellung von Zahlen beim Rendern in feste Seitenformate verwendet wird.

```csharp
public enum NumeralFormat
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| European | `0` | Europäische Ziffern: 0123456789. |
| ArabicIndic | `1` | Im Arabischen verwendete Ziffern: ٠١٢٣٤٥٦٧٨٩. Unicode-Bereich U+0660 – u+0669. |
| EasternArabicIndic | `2` | Im Persischen und Urdu verwendete Ziffern: ۰۱۲۳۴۵۶۷۸۹. Unicode-Bereich U+06F0 – u+06F9. |
| Context | `3` | Der Symbolsatz wird aus dem Kontext (Gebietsschema und RTL-Eigenschaft) bestimmt. |
| System | `4` | DIESE OPTION WIRD NICHT UNTERSTÜTZT. Der Symbolsatz wird über die regionalen Einstellungen festgelegt. |

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
