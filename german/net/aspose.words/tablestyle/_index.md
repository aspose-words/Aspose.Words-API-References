---
title: TableStyle
second_title: Aspose.Words für .NET-API-Referenz
description: Repräsentiert einen Tabellenstil.
type: docs
weight: 5920
url: /de/net/aspose.words/tablestyle/
---
## TableStyle class

Repräsentiert einen Tabellenstil.

```csharp
public class TableStyle : Style
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Aliases](../../aspose.words/style/aliases) { get; } | Ruft alle Aliase dieses Stils ab. Wenn style keine Aliase hat, wird ein leeres String-Array zurückgegeben. |
| [Alignment](../../aspose.words/tablestyle/alignment) { get; set; } | Gibt die Ausrichtung für den Tabellenstil an. |
| [AllowBreakAcrossPages](../../aspose.words/tablestyle/allowbreakacrosspages) { get; set; } | Ruft ein Flag ab oder setzt es, das angibt, ob Text in einer Tabellenzeile über einen Seitenumbruch geteilt werden darf. |
| [BaseStyleName](../../aspose.words/style/basestylename) { get; set; } | Ermittelt/setzt den Namen des Stils, auf dem dieser Stil basiert. |
| [Bidi](../../aspose.words/tablestyle/bidi) { get; set; } | Ruft ab oder legt fest, ob dies ein Stil für eine von rechts nach links verlaufende Tabelle ist. |
| [Borders](../../aspose.words/tablestyle/borders) { get; } | Ruft die Sammlung von Standardzellenrahmen für den Stil ab. |
| [BottomPadding](../../aspose.words/tablestyle/bottompadding) { get; set; } | Ruft den Abstand (in Punkt) ab oder legt ihn fest, der unter dem Inhalt von Tabellenzellen hinzugefügt werden soll. |
| [BuiltIn](../../aspose.words/style/builtin) { get; } | Wahr, wenn dieser Stil einer der integrierten Stile in MS Word ist. |
| [CellSpacing](../../aspose.words/tablestyle/cellspacing) { get; set; } | Ruft den Abstand (in Punkten) zwischen den Zellen ab oder legt ihn fest. |
| [ColumnStripe](../../aspose.words/tablestyle/columnstripe) { get; set; } | Ruft eine Anzahl von Spalten ab oder legt sie fest, die in das Banding eingeschlossen werden sollen, wenn der Stil das Banding von geraden/ungeraden Spalten angibt. |
| [ConditionalStyles](../../aspose.words/tablestyle/conditionalstyles) { get; } | Sammlung bedingter Stile, die für diesen Tabellenstil definiert werden können. |
| [Document](../../aspose.words/style/document) { get; } | Ruft das Besitzerdokument ab. |
| [Font](../../aspose.words/style/font) { get; } | Ruft die Zeichenformatierung des Stils ab. |
| [IsHeading](../../aspose.words/style/isheading) { get; } | Wahr, wenn der Stil einer der integrierten Überschriftenstile ist. |
| [IsQuickStyle](../../aspose.words/style/isquickstyle) { get; set; } | Gibt an, ob dieser Stil in der Quick Style-Galerie in der MS Word-Benutzeroberfläche angezeigt wird. |
| [LeftIndent](../../aspose.words/tablestyle/leftindent) { get; set; } | Ruft den Wert ab oder legt ihn fest, der den linken Einzug einer Tabelle darstellt. |
| [LeftPadding](../../aspose.words/tablestyle/leftpadding) { get; set; } | Ruft den Platz (in Punkten) ab oder legt ihn fest, der links vom Inhalt der Tabellenzellen hinzugefügt werden soll. |
| [LinkedStyleName](../../aspose.words/style/linkedstylename) { get; } | Ruft den Namen des Styles ab, der mit diesem verknüpft ist. Gibt eine leere Zeichenfolge zurück, wenn keine Stile verknüpft sind. |
| [List](../../aspose.words/style/list) { get; } | Ruft die Liste ab, die die Formatierung dieses Listenstils definiert. |
| [ListFormat](../../aspose.words/style/listformat) { get; } | Bietet Zugriff auf die Listenformatierungseigenschaften eines Absatzstils. |
| [Name](../../aspose.words/style/name) { get; set; } | Ruft den Namen des Stils ab oder legt ihn fest. |
| [NextParagraphStyleName](../../aspose.words/style/nextparagraphstylename) { get; set; } | Ermittelt/legt den Namen des Stils fest, der automatisch auf einen neuen Absatz angewendet werden soll, der nach einem -Absatz eingefügt wird, der mit dem angegebenen Stil formatiert ist. |
| [ParagraphFormat](../../aspose.words/style/paragraphformat) { get; } | Ruft die Absatzformatierung des Stils ab. |
| [RightPadding](../../aspose.words/tablestyle/rightpadding) { get; set; } | Ruft den Abstand (in Punkten) ab oder legt ihn fest, der rechts vom Inhalt der Tabellenzellen hinzugefügt werden soll. |
| [RowStripe](../../aspose.words/tablestyle/rowstripe) { get; set; } | Ruft eine Anzahl von Zeilen ab oder legt sie fest, die in das Banding eingeschlossen werden sollen, wenn der Stil ein Banding für ungerade/gerade Zeilen angibt. |
| [Shading](../../aspose.words/tablestyle/shading) { get; } | erhält a[`Shading`](../shading) Objekt, das sich auf die Schattierungsformatierung für Tabellenzellen bezieht. |
| [StyleIdentifier](../../aspose.words/style/styleidentifier) { get; } | Ruft den vom Gebietsschema unabhängigen Stilbezeichner für einen integrierten Stil ab. |
| [Styles](../../aspose.words/style/styles) { get; } | Ruft die Sammlung von Stilen ab, zu denen dieser Stil gehört. |
| [TopPadding](../../aspose.words/tablestyle/toppadding) { get; set; } | Ruft den Abstand (in Punkten) ab oder legt ihn fest, der über dem Inhalt von Tabellenzellen hinzugefügt werden soll. |
| [Type](../../aspose.words/style/type) { get; } | Ruft den Stiltyp ab (Absatz oder Zeichen). |
| [VerticalAlignment](../../aspose.words/tablestyle/verticalalignment) { get; set; } | Gibt die vertikale Ausrichtung der Zellen an. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Equals](../../aspose.words/style/equals)(Style) | Vergleicht mit dem angegebenen Stil. Stile Istds werden nur für integrierte Stile verglichen. Standardstile werden nicht in den Vergleich einbezogen. Basisstil, verknüpfter Stil und nächster Absatzstil werden rekursiv verglichen. |
| [Remove](../../aspose.words/style/remove)() | Entfernt den angegebenen Stil aus dem Dokument. |

### Beispiele

Zeigt, wie benutzerdefinierte Stileinstellungen für die Tabelle erstellt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Name");
builder.InsertCell();
builder.Write("مرحبًا");
builder.EndRow();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.AllowBreakAcrossPages = true;
tableStyle.Bidi = true;
tableStyle.CellSpacing = 5;
tableStyle.BottomPadding = 20;
tableStyle.LeftPadding = 5;
tableStyle.RightPadding = 10;
tableStyle.TopPadding = 20;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;
tableStyle.VerticalAlignment = CellVerticalAlignment.Center;

table.Style = tableStyle;

// Das Festlegen der Stileigenschaften einer Tabelle kann sich auf die Eigenschaften der Tabelle selbst auswirken.
Assert.True(table.Bidi);
Assert.AreEqual(5.0d, table.CellSpacing);
Assert.AreEqual("MyTableStyle1", table.StyleName);

doc.Save(ArtifactsDir + "Table.TableStyleCreation.docx");
```

### Siehe auch

* class [Style](../style)
* namensraum [Aspose.Words](../../aspose.words)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
