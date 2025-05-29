---
title: StyleCollection Class
linktitle: StyleCollection
articleTitle: StyleCollection
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.StyleCollection mit einer großen Auswahl an integrierten und benutzerdefinierten Stilobjekten zur Verbesserung der Formatierung und des Designs Ihres Dokuments.
type: docs
weight: 6990
url: /de/net/aspose.words/stylecollection/
---
## StyleCollection class

Eine Sammlung von[`Style`](../style/)Objekte, die sowohl die integrierten als auch die benutzerdefinierten Stile in einem Dokument darstellen.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Stilen und Designs](https://docs.aspose.com/words/net/working-with-styles-and-themes/) Dokumentationsartikel.

```csharp
public class StyleCollection : IEnumerable<Style>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words/stylecollection/count/) { get; } | Ruft die Anzahl der Stile in der Sammlung ab. |
| [DefaultFont](../../aspose.words/stylecollection/defaultfont/) { get; } | Ruft die Standardtextformatierung des Dokuments ab. |
| [DefaultParagraphFormat](../../aspose.words/stylecollection/defaultparagraphformat/) { get; } | Ruft die Standardabsatzformatierung des Dokuments ab. |
| [Document](../../aspose.words/stylecollection/document/) { get; } | Ruft das Besitzerdokument ab. |
| [Item](../../aspose.words/stylecollection/item/) { get; } | Ruft einen Stil nach Name oder Alias ab. (3 indexers) |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words/stylecollection/add/)(*[StyleType](../styletype/), string*) | Erstellt einen neuen benutzerdefinierten Stil und fügt ihn der Sammlung hinzu. |
| [AddCopy](../../aspose.words/stylecollection/addcopy/)(*[Style](../style/)*) | Kopiert einen Stil in diese Sammlung. |
| [ClearQuickStyleGallery](../../aspose.words/stylecollection/clearquickstylegallery/)() | Entfernt alle Stile aus dem Quick Style Gallery-Bedienfeld. |
| [GetEnumerator](../../aspose.words/stylecollection/getenumerator/)() | Ruft ein Enumeratorobjekt ab, das Stile in alphabetischer Reihenfolge ihrer Namen aufzählt. |

## Beispiele

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

* class [Style](../style/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
