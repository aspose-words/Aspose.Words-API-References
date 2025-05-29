---
title: FieldSymbol Class
linktitle: FieldSymbol
articleTitle: FieldSymbol
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fields.FieldSymbol für eine effiziente SYMBOL-Feldimplementierung und verbessern Sie Ihre Dokumentverarbeitungsfunktionen.
type: docs
weight: 2870
url: /de/net/aspose.words.fields/fieldsymbol/
---
## FieldSymbol class

Implementiert ein SYMBOL-Feld.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public class FieldSymbol : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldSymbol](fieldsymbol/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CharacterCode](../../aspose.words.fields/fieldsymbol/charactercode/) { get; set; } | Ruft den Codepunktwert des Zeichens in Dezimal- oder Hexadezimalzahlen ab oder legt ihn fest. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [DontAffectsLineSpacing](../../aspose.words.fields/fieldsymbol/dontaffectslinespacing/) { get; set; } | Ruft ab oder legt fest, ob das vom Feld abgerufene Zeichen den Zeilenabstand des Absatzes beeinflusst. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [FontName](../../aspose.words.fields/fieldsymbol/fontname/) { get; set; } | Ruft den Namen der Schriftart des vom Feld abgerufenen Zeichens ab oder legt ihn fest. |
| [FontSize](../../aspose.words.fields/fieldsymbol/fontsize/) { get; set; } | Ruft die Größe der Schriftart des vom Feld abgerufenen Zeichens in Punkten ab oder legt diese fest. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Erhält eine[`FieldFormat`](../fieldformat/)Objekt, das typisierten Zugriff auf die Formatierung des Felds bietet. |
| [IsAnsi](../../aspose.words.fields/fieldsymbol/isansi/) { get; set; } | Ruft ab oder legt fest, ob der Zeichencode als Wert eines ANSI-Zeichens interpretiert wird. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer am Dokument vorgenommener Änderungen nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (das Ergebnis sollte nicht neu berechnet werden). |
| [IsShiftJis](../../aspose.words.fields/fieldsymbol/isshiftjis/) { get; set; } | Ruft ab oder legt fest, ob der Zeichencode als Wert eines SHIFT-JIS-Zeichens interpretiert wird. |
| [IsUnicode](../../aspose.words.fields/fieldsymbol/isunicode/) { get; set; } | Ruft ab oder legt fest, ob der Zeichencode als Wert eines Unicode-Zeichens interpretiert wird. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ruft Text ab oder legt ihn fest, der zwischen Feldtrennzeichen und Feldende steht. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann sein`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ruft den Microsoft Word-Feldtyp ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldergebnis von untergeordneten Feldern werden einbezogen. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). |
| [Remove](../../aspose.words.fields/field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte Kind seines übergeordneten Knotens ist, wird dessen übergeordneter Absatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Führt die Feldverknüpfung aus. |
| [Update](../../aspose.words.fields/field/update/)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |

## Bemerkungen

Ruft das Zeichen ab, dessen Codepunktwert dezimal oder hexadezimal angegeben ist.

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

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
