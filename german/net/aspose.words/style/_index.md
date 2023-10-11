---
title: Class Style
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Style klas. Stellt einen einzelnen integrierten oder benutzerdefinierten Stil dar.
type: docs
weight: 6130
url: /de/net/aspose.words/style/
---
## Style class

Stellt einen einzelnen integrierten oder benutzerdefinierten Stil dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Stilen und Themen](https://docs.aspose.com/words/net/working-with-styles-and-themes/) Dokumentationsartikel.

```csharp
public class Style
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Aliases](../../aspose.words/style/aliases/) { get; } | Ruft alle Aliase dieses Stils ab. Wenn der Stil keine Aliase hat, wird ein leeres String-Array zurückgegeben. |
| [AutomaticallyUpdate](../../aspose.words/style/automaticallyupdate/) { get; set; } | Gibt an, ob dieser Stil basierend auf dem entsprechenden Wert automatisch neu definiert wird. |
| [BaseStyleName](../../aspose.words/style/basestylename/) { get; set; } | Ruft den Namen des Stils ab, auf dem dieser Stil basiert, bzw. legt ihn fest. |
| [BuiltIn](../../aspose.words/style/builtin/) { get; } | True, wenn dieser Stil einer der integrierten Stile in MS Word ist. |
| [Document](../../aspose.words/style/document/) { get; } | Ruft das Eigentümerdokument ab. |
| [Font](../../aspose.words/style/font/) { get; } | Ruft die Zeichenformatierung des Stils ab. |
| [IsHeading](../../aspose.words/style/isheading/) { get; } | True, wenn der Stil einer der integrierten Überschriftenstile ist. |
| [IsQuickStyle](../../aspose.words/style/isquickstyle/) { get; set; } | Gibt an, ob dieser Stil in der Quick Style-Galerie in der MS Word-Benutzeroberfläche angezeigt wird. |
| [LinkedStyleName](../../aspose.words/style/linkedstylename/) { get; } | Ruft den Namen ab`Style` mit diesem verlinkt. Gibt eine leere Zeichenfolge zurück, wenn keine Stile verknüpft sind. |
| [List](../../aspose.words/style/list/) { get; } | Ruft die Liste ab, die die Formatierung dieses Listenstils definiert. |
| [ListFormat](../../aspose.words/style/listformat/) { get; } | Bietet Zugriff auf die Listenformatierungseigenschaften eines Absatzstils. |
| [Locked](../../aspose.words/style/locked/) { get; set; } |  |
| [Name](../../aspose.words/style/name/) { get; set; } | Ruft den Namen des Stils ab oder legt ihn fest. |
| [NextParagraphStyleName](../../aspose.words/style/nextparagraphstylename/) { get; set; } | Ruft den Namen des Stils ab bzw. legt ihn fest, der automatisch auf einen neuen Absatz angewendet werden soll, der nach einem Absatz eingefügt wird, der mit dem angegebenen Stil formatiert ist. |
| [ParagraphFormat](../../aspose.words/style/paragraphformat/) { get; } | Ruft die Absatzformatierung des Stils ab. |
| [StyleIdentifier](../../aspose.words/style/styleidentifier/) { get; } | Ruft die vom Gebietsschema unabhängige Stilkennung für einen integrierten Stil ab. |
| [Styles](../../aspose.words/style/styles/) { get; } | Ruft die Sammlung von Stilen ab, zu denen dieser Stil gehört. |
| [Type](../../aspose.words/style/type/) { get; } | Ruft den Stiltyp (Absatz oder Zeichen) ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Equals](../../aspose.words/style/equals/#equals)(Style) | Vergleicht mit dem angegebenen Stil. Istds-Stile werden nur für integrierte Stile verglichen. Standardwerte für Stile werden nicht im Vergleich berücksichtigt. Basisstil, verknüpfter Stil und Stil für den nächsten Absatz werden rekursiv verglichen. |
| [Remove](../../aspose.words/style/remove/)() | Entfernt den angegebenen Stil aus dem Dokument. |

### Beispiele

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

// Den Absatzstil auf den aktuellen Absatz des Document Builders anwenden und dann etwas Text hinzufügen.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// Ändern Sie den Stil des Document Builders in einen Stil ohne Listenformatierung und schreiben Sie einen weiteren Absatz.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

Zeigt, wie ein benutzerdefinierter Stil erstellt und angewendet wird.

```csharp
Document doc = new Document();

Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle");
style.Font.Name = "Times New Roman";
style.Font.Size = 16;
style.Font.Color = Color.Navy;
// Stil automatisch neu definieren.
style.AutomaticallyUpdate = true;

DocumentBuilder builder = new DocumentBuilder(doc);

// Einen der Stile aus dem Dokument auf den Absatz anwenden, den der Dokumentersteller erstellt.
builder.ParagraphFormat.Style = doc.Styles["MyStyle"];
builder.Writeln("Hello world!");

Style firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

Assert.AreEqual(style, firstParagraphStyle);

// Entfernen Sie unseren benutzerdefinierten Stil aus der Stilsammlung des Dokuments.
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


