---
title: FieldSymbol.FontSize
second_title: Aspose.Words für .NET-API-Referenz
description: FieldSymbol eigendom. Ruft die Größe der Schriftart des vom Feld abgerufenen Zeichens in Punkt ab oder legt sie fest.
type: docs
weight: 50
url: /de/net/aspose.words.fields/fieldsymbol/fontsize/
---
## FieldSymbol.FontSize property

Ruft die Größe der Schriftart des vom Feld abgerufenen Zeichens in Punkt ab oder legt sie fest.

```csharp
public string FontSize { get; set; }
```

### Beispiele

Zeigt, wie das SYMBOL-Feld verwendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nachfolgend finden Sie drei Möglichkeiten, ein SYMBOL-Feld zu verwenden, um ein einzelnes Zeichen anzuzeigen.
// 1 - Fügen Sie ein SYMBOL-Feld hinzu, das das Symbol © (Copyright) anzeigt, das durch einen ANSI-Zeichencode angegeben wird:
FieldSymbol field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// Der ANSI-Zeichencode "U+00A9" oder "169" in Ganzzahlform ist für das Copyright-Symbol reserviert.
field.CharacterCode = 0x00a9.ToString();
field.IsAnsi = true;

Assert.AreEqual(" SYMBOL  169 \\a", field.GetFieldCode());

builder.Writeln(" Line 1");

// 2 - Fügen Sie ein SYMBOL-Feld hinzu, das das Symbol ∞ (Unendlich) anzeigt, und ändern Sie sein Aussehen:
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// In Unicode belegt das Unendlichkeitszeichen den "221E"-Code.
field.CharacterCode = 0x221E.ToString();
field.IsUnicode = true;

// Ändern Sie die Schriftart unseres Symbols, nachdem Sie die Windows-Zeichentabelle verwendet haben
// um sicherzustellen, dass die Schriftart dieses Symbol darstellen kann.
field.FontName = "Calibri";
field.FontSize = "24";

// Wir können dieses Flag für große Symbole setzen, damit sie den Rest des Textes in ihrer Zeile nicht nach unten drücken.
field.DontAffectsLineSpacing = true;

Assert.AreEqual(" SYMBOL  8734 \\u \\f Calibri \\s 24 \\h", field.GetFieldCode());

builder.Writeln("Line 2");

// 3 - Fügen Sie ein SYMBOL-Feld hinzu, das das Zeichen あ anzeigt,
// mit einer Schriftart, die die Codepage Shift-JIS (Windows-932) unterstützt:
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);
field.FontName = "MS Gothic";
field.CharacterCode = 0x82A0.ToString();
field.IsShiftJis = true;

Assert.AreEqual(" SYMBOL  33440 \\f \"MS Gothic\" \\j", field.GetFieldCode());

builder.Write("Line 3");

doc.Save(ArtifactsDir + "Field.SYMBOL.docx");
```

### Siehe auch

* class [FieldSymbol](../)
* namensraum [Aspose.Words.Fields](../../fieldsymbol/)
* Montage [Aspose.Words](../../../)


