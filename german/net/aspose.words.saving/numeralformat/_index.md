---
title: Enum NumeralFormat
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.NumeralFormat opsomming. Gibt den Symbolsatz an der zur Darstellung von Zahlen beim Rendern in feste Seitenformate verwendet wird.
type: docs
weight: 5310
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
| ArabicIndic | `1` | Auf Arabisch verwendete Ziffern: ٠١٢٣٤٥٦٧٨٩. Unicode-Bereich U+0660 - u+0669. |
| EasternArabicIndic | `2` | In Persisch und Urdu verwendete Ziffern: ۰۱۲۳۴۵۶۷۸۹. Unicode-Bereich U+06F0 - u+06F9. |
| Context | `3` | Der Symbolsatz wird anhand des Kontexts (Gebietsschema und RTL-Eigenschaft) festgelegt. |
| System | `4` | DIESE OPTION WIRD NICHT UNTERSTÜTZT. Der Symbolsatz wird anhand der regionalen Einstellungen festgelegt. |

### Beispiele

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)


