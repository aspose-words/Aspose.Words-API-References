---
title: Class Style
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Style klas. Stellt einen einzelnen integrierten oder benutzerdefinierten Stil dar.
type: docs
weight: 5830
url: /de/net/aspose.words/style/
---
## Style class

Stellt einen einzelnen integrierten oder benutzerdefinierten Stil dar.

```csharp
public class Style
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Aliases](../../aspose.words/style/aliases/) { get; } | Ruft alle Aliase dieses Stils ab. Wenn style keine Aliase hat, wird ein leeres String-Array zurückgegeben. |
| [BaseStyleName](../../aspose.words/style/basestylename/) { get; set; } | Ermittelt/setzt den Namen des Stils, auf dem dieser Stil basiert. |
| [BuiltIn](../../aspose.words/style/builtin/) { get; } | Wahr, wenn dieser Stil einer der integrierten Stile in MS Word ist. |
| [Document](../../aspose.words/style/document/) { get; } | Ruft das Besitzerdokument ab. |
| [Font](../../aspose.words/style/font/) { get; } | Ruft die Zeichenformatierung des Stils ab. |
| [IsHeading](../../aspose.words/style/isheading/) { get; } | Wahr, wenn der Stil einer der integrierten Überschriftenstile ist. |
| [IsQuickStyle](../../aspose.words/style/isquickstyle/) { get; set; } | Gibt an, ob dieser Stil in der Quick Style-Galerie in der MS Word-Benutzeroberfläche angezeigt wird. |
| [LinkedStyleName](../../aspose.words/style/linkedstylename/) { get; } | Ruft den Namen des Styles ab, der mit diesem verknüpft ist. Gibt eine leere Zeichenfolge zurück, wenn keine Stile verknüpft sind. |
| [List](../../aspose.words/style/list/) { get; } | Ruft die Liste ab, die die Formatierung dieses Listenstils definiert. |
| [ListFormat](../../aspose.words/style/listformat/) { get; } | Bietet Zugriff auf die Listenformatierungseigenschaften eines Absatzstils. |
| [Name](../../aspose.words/style/name/) { get; set; } | Ruft den Namen des Stils ab oder legt ihn fest. |
| [NextParagraphStyleName](../../aspose.words/style/nextparagraphstylename/) { get; set; } | Ermittelt/legt den Namen des Stils fest, der automatisch auf einen neuen Absatz angewendet werden soll, der nach einem -Absatz eingefügt wird, der mit dem angegebenen Stil formatiert ist. |
| [ParagraphFormat](../../aspose.words/style/paragraphformat/) { get; } | Ruft die Absatzformatierung des Stils ab. |
| [StyleIdentifier](../../aspose.words/style/styleidentifier/) { get; } | Ruft den vom Gebietsschema unabhängigen Stilbezeichner für einen integrierten Stil ab. |
| [Styles](../../aspose.words/style/styles/) { get; } | Ruft die Sammlung von Stilen ab, zu denen dieser Stil gehört. |
| [Type](../../aspose.words/style/type/) { get; } | Ruft den Stiltyp ab (Absatz oder Zeichen). |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Equals](../../aspose.words/style/equals/#equals)(Style) | Vergleicht mit dem angegebenen Stil. Stile Istds werden nur für integrierte Stile verglichen. Standardstile werden nicht in den Vergleich einbezogen. Basisstil, verknüpfter Stil und nächster Absatzstil werden rekursiv verglichen. |
| [Remove](../../aspose.words/style/remove/)() | Entfernt den angegebenen Stil aus dem Dokument. |

### Beispiele

Zeigt, wie Sie ein Absatzformat mit Listenformatierung erstellen und verwenden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Einen benutzerdefinierten Absatzstil erstellen.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// Erstellen Sie eine Liste und stellen Sie sicher, dass die Absätze, die diesen Stil verwenden, diese Liste verwenden.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// Den Absatzstil auf den aktuellen Absatz des Document Builder anwenden und dann etwas Text hinzufügen.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// Ändern Sie den Stil des Document Builder in einen Stil ohne Listenformatierung und schreiben Sie einen weiteren Absatz.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

Zeigt, wie Sie einen benutzerdefinierten Stil erstellen und anwenden.

```csharp
Document doc = new Document();

Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle");
style.Font.Name = "Times New Roman";
style.Font.Size = 16;
style.Font.Color = Color.Navy;

DocumentBuilder builder = new DocumentBuilder(doc);

// Einen der Stile aus dem Dokument auf den Absatz anwenden, den der Document Builder erstellt.
builder.ParagraphFormat.Style = doc.Styles["MyStyle"];
builder.Writeln("Hello world!");

Style firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

Assert.AreEqual(style, firstParagraphStyle);

// Unseren benutzerdefinierten Stil aus der Stilsammlung des Dokuments entfernen.
doc.Styles["MyStyle"].Remove();

firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

// Jeder Text, der einen entfernten Stil verwendet hat, wird auf die Standardformatierung zurückgesetzt.
Assert.False(doc.Styles.Any(s => s.Name == "MyStyle"));
Assert.AreEqual("Times New Roman", firstParagraphStyle.Font.Name);
Assert.AreEqual(12.0d, firstParagraphStyle.Font.Size);
Assert.AreEqual(Color.Empty.ToArgb(), firstParagraphStyle.Font.Color.ToArgb());
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)


