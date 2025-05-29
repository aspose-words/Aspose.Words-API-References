---
title: FieldSymbol.DontAffectsLineSpacing
linktitle: DontAffectsLineSpacing
articleTitle: DontAffectsLineSpacing
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die FieldSymbol-Eigenschaft „DontAffectsLineSpacing“ den Zeicheneinfluss auf den Zeilenabstand von Absätzen steuert. Optimieren Sie noch heute Ihre Dokumentformatierung!
type: docs
weight: 30
url: /de/net/aspose.words.fields/fieldsymbol/dontaffectslinespacing/
---
## FieldSymbol.DontAffectsLineSpacing property

Ruft ab oder legt fest, ob das vom Feld abgerufene Zeichen den Zeilenabstand des Absatzes beeinflusst.

```csharp
public bool DontAffectsLineSpacing { get; set; }
```

## Beispiele

Zeigt, wie das SYMBOL-Feld verwendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Unten sind drei Möglichkeiten aufgeführt, ein SYMBOL-Feld zum Anzeigen eines einzelnen Zeichens zu verwenden.
// 1 – Fügen Sie ein SYMBOL-Feld hinzu, das das ©-Symbol (Copyright) anzeigt, angegeben durch einen ANSI-Zeichencode:
FieldSymbol field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// Der ANSI-Zeichencode „U+00A9“ oder „169“ in Ganzzahlform ist für das Copyright-Symbol reserviert.
field.CharacterCode = 0x00a9.ToString();
field.IsAnsi = true;

Assert.AreEqual(" SYMBOL  169 \\a", field.GetFieldCode());

builder.Writeln(" Line 1");

// 2 – Fügen Sie ein SYMBOL-Feld hinzu, das das Symbol ∞ (Unendlichkeit) anzeigt, und ändern Sie sein Erscheinungsbild:
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// In Unicode belegt das Unendlichkeitssymbol den Code „221E“.
field.CharacterCode = 0x221E.ToString();
field.IsUnicode = true;

// Ändern Sie die Schriftart unseres Symbols, nachdem Sie die Windows-Zeichentabelle verwendet haben
// um sicherzustellen, dass die Schriftart dieses Symbol darstellen kann.
field.FontName = "Calibri";
field.FontSize = "24";

// Wir können dieses Flag für große Symbole setzen, damit sie den restlichen Text in ihrer Zeile nicht nach unten drücken.
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
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
