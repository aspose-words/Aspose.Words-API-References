---
title: Font Class
linktitle: Font
articleTitle: Font
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Font mit wichtigen Schriftattributen wie Name, Größe und Farbe, um die Formatierung und das Design Ihres Dokuments zu verbessern.
type: docs
weight: 3240
url: /de/net/aspose.words/font/
---
## Font class

Enthält Schriftattribute (Schriftname, Schriftgröße, Farbe usw.) für ein Objekt.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Schriftarten](https://docs.aspose.com/words/net/working-with-fonts/) Dokumentationsartikel.

```csharp
public class Font
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AllCaps](../../aspose.words/font/allcaps/) { get; set; } | Wahr, wenn die Schriftart ausschließlich in Großbuchstaben formatiert ist. |
| [AutoColor](../../aspose.words/font/autocolor/) { get; } | Gibt die aktuell berechnete Farbe des Textes (schwarz oder weiß) zurück, die für „Auto-Farbe“ verwendet werden soll. Wenn die Farbe nicht „auto“ ist, wird Folgendes zurückgegeben[`Color`](./color/) . |
| [Bidi](../../aspose.words/font/bidi/) { get; set; } | Gibt an, ob der Inhalt dieses Laufs von rechts nach links verlaufen soll. |
| [Bold](../../aspose.words/font/bold/) { get; set; } | Wahr, wenn die Schriftart fett formatiert ist. |
| [BoldBi](../../aspose.words/font/boldbi/) { get; set; } | Wahr, wenn der von rechts nach links verlaufende Text fett formatiert ist. |
| [Border](../../aspose.words/font/border/) { get; } | Gibt einen[`Border`](../border/) Objekt, das den Rahmen für die Schriftart angibt. |
| [Color](../../aspose.words/font/color/) { get; set; } | Ruft die Farbe der Schriftart ab oder legt sie fest. |
| [ComplexScript](../../aspose.words/font/complexscript/) { get; set; } | Gibt an, ob der Inhalt dieses Laufs bei der Festlegung der Formatierung für diesen Lauf unabhängig von seinen Unicode-Zeichenwerten als komplexer Skripttext behandelt werden soll. |
| [DoubleStrikeThrough](../../aspose.words/font/doublestrikethrough/) { get; set; } | Wahr, wenn die Schriftart als doppelt durchgestrichener Text formatiert ist. |
| [Emboss](../../aspose.words/font/emboss/) { get; set; } | Wahr, wenn die Schriftart als geprägt formatiert ist. |
| [EmphasisMark](../../aspose.words/font/emphasismark/) { get; set; } | Ruft das Hervorhebungszeichen ab oder legt es fest, das auf diese Formatierung angewendet wird. |
| [Engrave](../../aspose.words/font/engrave/) { get; set; } | Wahr, wenn die Schriftart als graviert formatiert ist. |
| [Fill](../../aspose.words/font/fill/) { get; } | Ruft die Füllformatierung für die`Font` . |
| [Hidden](../../aspose.words/font/hidden/) { get; set; } | Wahr, wenn die Schriftart als versteckter Text formatiert ist. |
| [HighlightColor](../../aspose.words/font/highlightcolor/) { get; set; } | Ruft die Hervorhebungsfarbe (Markierung) ab oder legt sie fest. |
| [Italic](../../aspose.words/font/italic/) { get; set; } | Wahr, wenn die Schriftart kursiv formatiert ist. |
| [ItalicBi](../../aspose.words/font/italicbi/) { get; set; } | Wahr, wenn der von rechts nach links verlaufende Text kursiv formatiert ist. |
| [Kerning](../../aspose.words/font/kerning/) { get; set; } | Ruft die Schriftgröße ab, bei der die Unterschneidung beginnt, oder legt diese fest. |
| [LineSpacing](../../aspose.words/font/linespacing/) { get; } | Gibt den Zeilenabstand dieser Schriftart (in Punkten) zurück. |
| [LocaleId](../../aspose.words/font/localeid/) { get; set; } | Ruft die Gebietsschemakennung (Sprache) der formatierten Zeichen ab oder legt sie fest. |
| [LocaleIdBi](../../aspose.words/font/localeidbi/) { get; set; } | Ruft die Gebietsschemakennung (Sprache) der formatierten Rechts-nach-links-Zeichen ab oder legt diese fest. |
| [LocaleIdFarEast](../../aspose.words/font/localeidfareast/) { get; set; } | Ruft die Gebietsschemakennung (Sprache) der formatierten asiatischen Zeichen ab oder legt sie fest. |
| [Name](../../aspose.words/font/name/) { get; set; } | Ruft den Namen der Schriftart ab oder legt ihn fest. |
| [NameAscii](../../aspose.words/font/nameascii/) { get; set; } | Gibt die Schriftart für lateinischen Text zurück oder legt sie fest (Zeichen mit Zeichencodes von 0 (Null) bis 127). |
| [NameBi](../../aspose.words/font/namebi/) { get; set; } | Gibt den Namen der Schriftart in einem von rechts nach links geschriebenen Sprachdokument zurück oder legt ihn fest. |
| [NameFarEast](../../aspose.words/font/namefareast/) { get; set; } | Gibt einen ostasiatischen Schriftnamen zurück oder legt ihn fest. |
| [NameOther](../../aspose.words/font/nameother/) { get; set; } | Gibt die Schriftart zurück oder legt sie fest, die für Zeichen mit Zeichencodes von 128 bis 255 verwendet wird. |
| [NoProofing](../../aspose.words/font/noproofing/) { get; set; } | Wahr, wenn für die formatierten Zeichen keine Rechtschreibprüfung durchgeführt werden soll. |
| [NumberSpacing](../../aspose.words/font/numberspacing/) { get; set; } | Ruft den Abstandstyp der angezeigten Ziffer ab oder legt ihn fest. |
| [Outline](../../aspose.words/font/outline/) { get; set; } | Wahr, wenn die Schriftart als Umriss formatiert ist. |
| [Position](../../aspose.words/font/position/) { get; set; } | Ruft die Position des Textes (in Punkten) relativ zur Grundlinie ab oder legt sie fest. Eine positive Zahl hebt den Text an, eine negative Zahl senkt ihn. |
| [Scaling](../../aspose.words/font/scaling/) { get; set; } | Ruft die Zeichenbreitenskalierung in Prozent ab oder legt sie fest. |
| [Shading](../../aspose.words/font/shading/) { get; } | Gibt einen[`Shading`](../shading/) Objekt, das sich auf die Schattierungsformatierung für die Schriftart bezieht. |
| [Shadow](../../aspose.words/font/shadow/) { get; set; } | Wahr, wenn die Schriftart als schattiert formatiert ist. |
| [Size](../../aspose.words/font/size/) { get; set; } | Ruft die Schriftgröße in Punkten ab oder legt sie fest. |
| [SizeBi](../../aspose.words/font/sizebi/) { get; set; } | Ruft die Schriftgröße in Punkten ab oder legt sie fest, die in einem von rechts nach links geschriebenen Dokument verwendet wird. |
| [SmallCaps](../../aspose.words/font/smallcaps/) { get; set; } | Wahr, wenn die Schriftart als Großbuchstaben formatiert ist. |
| [SnapToGrid](../../aspose.words/font/snaptogrid/) { get; set; } | Gibt an, ob die aktuelle Schriftart beim Layouten die Einstellungen für Dokumentrasterzeichen pro Zeile verwenden soll. |
| [Spacing](../../aspose.words/font/spacing/) { get; set; } | Gibt den Abstand (in Punkten) zwischen Zeichen zurück oder legt ihn fest. |
| [StrikeThrough](../../aspose.words/font/strikethrough/) { get; set; } | Wahr, wenn die Schriftart als durchgestrichener Text formatiert ist. |
| [Style](../../aspose.words/font/style/) { get; set; } | Ruft den auf diese Formatierung angewendeten Zeichenstil ab oder legt ihn fest. |
| [StyleIdentifier](../../aspose.words/font/styleidentifier/) { get; set; } | Ruft die gebietsschemaunabhängige Stilkennung des auf diese Formatierung angewendeten Zeichenstils ab oder legt diese fest. |
| [StyleName](../../aspose.words/font/stylename/) { get; set; } | Ruft den Namen des Zeichenstils ab, der auf diese Formatierung angewendet wird, oder legt ihn fest. |
| [Subscript](../../aspose.words/font/subscript/) { get; set; } | Wahr, wenn die Schriftart als tiefgestellt formatiert ist. |
| [Superscript](../../aspose.words/font/superscript/) { get; set; } | Wahr, wenn die Schriftart als hochgestellt formatiert ist. |
| [TextEffect](../../aspose.words/font/texteffect/) { get; set; } | Ruft den Schriftanimationseffekt ab oder legt ihn fest. |
| [ThemeColor](../../aspose.words/font/themecolor/) { get; set; } | Ruft die Designfarbe im angewendeten Farbschema ab oder legt sie fest, die mit diesem verknüpft ist.`Font` Objekt. |
| [ThemeFont](../../aspose.words/font/themefont/) { get; set; } | Ruft die Designschriftart im angewendeten Schriftartschema ab oder legt sie fest, die mit diesem verknüpft ist.`Font` Objekt. |
| [ThemeFontAscii](../../aspose.words/font/themefontascii/) { get; set; } | Ruft die Schriftart für lateinischen Text (Zeichen mit Zeichencodes von 0 (Null) bis 127) im angewendeten Schriftartschema ab oder legt sie fest.`Font` Objekt. |
| [ThemeFontBi](../../aspose.words/font/themefontbi/) { get; set; } | Ruft die Designschriftart im angewendeten Schriftartschema ab oder legt sie fest, die mit diesem verknüpft ist.`Font` Objekt in einem von rechts nach links geschriebenen Sprachdokument. |
| [ThemeFontFarEast](../../aspose.words/font/themefontfareast/) { get; set; } | Ruft die Schriftart des ostasiatischen Designs im angewendeten Schriftartenschema ab oder legt sie fest, die mit diesem verknüpft ist.`Font` Objekt. |
| [ThemeFontOther](../../aspose.words/font/themefontother/) { get; set; } | Ruft die Designschriftart ab oder legt sie fest, die für Zeichen mit Zeichencodes von 128 bis 255 im angewendeten Schriftartschema verwendet wird, das diesem zugeordnet ist.`Font` Objekt. |
| [TintAndShade](../../aspose.words/font/tintandshade/) { get; set; } | Ruft einen Double-Wert ab oder legt ihn fest, der eine Farbe aufhellt oder abdunkelt. |
| [Underline](../../aspose.words/font/underline/) { get; set; } | Ruft den Unterstreichungstyp der Schriftart ab oder legt ihn fest. |
| [UnderlineColor](../../aspose.words/font/underlinecolor/) { get; set; } | Ruft die Farbe der Unterstreichung der Schriftart ab oder legt sie fest. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [ClearFormatting](../../aspose.words/font/clearformatting/)() | Setzt die Schriftformatierung auf die Standardeinstellung zurück. |
| [HasDmlEffect](../../aspose.words/font/hasdmleffect/)(*[TextDmlEffect](../textdmleffect/)*) | Überprüft, ob ein bestimmter DrawingML-Texteffekt angewendet wird. |

## Bemerkungen

Sie erstellen keine Instanzen des`Font` Klasse direkt. Sie verwenden einfach `Font` um auf die Schrifteigenschaften der verschiedenen Objekte zuzugreifen, wie z. B.[`Run`](../run/) , [`Paragraph`](../paragraph/) ,[`Style`](../style/) ,[`DocumentBuilder`](../documentbuilder/).

## Beispiele

Zeigt, wie ein Textlauf mithilfe seiner Schriftarteigenschaft formatiert wird.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

Zeigt, wie eine von einem Rahmen umgebene Zeichenfolge in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

Zeigt, wie ein Absatzstil mit Listenformatierung erstellt und verwendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie einen benutzerdefinierten Absatzstil.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// Erstellen Sie eine Liste und stellen Sie sicher, dass die Absätze, die diesen Stil verwenden, diese Liste verwenden.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// Wenden Sie den Absatzstil auf den aktuellen Absatz des Dokumentgenerators an und fügen Sie dann etwas Text hinzu.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// Ändern Sie den Stil des Dokument-Generators in einen Stil ohne Listenformatierung und schreiben Sie einen weiteren Absatz.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
