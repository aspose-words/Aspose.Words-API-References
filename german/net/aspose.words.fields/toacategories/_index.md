---
title: Class ToaCategories
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Fields.ToaCategories klas. Stellt eine Tabelle mit Behördenkategorien dar.
type: docs
weight: 2780
url: /de/net/aspose.words.fields/toacategories/
---
## ToaCategories class

Stellt eine Tabelle mit Behördenkategorien dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public class ToaCategories
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [ToaCategories](toacategories/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| static [DefaultCategories](../../aspose.words.fields/toacategories/defaultcategories/) { get; } | Ruft die Standardtabelle der Behördenkategorien ab. |
| [Item](../../aspose.words.fields/toacategories/item/) { get; set; } | Ruft die Kategorieüberschrift nach Kategorienummer ab oder legt sie fest. |

### Beispiele

Zeigt, wie eine Reihe von Kategorien für TOA-Felder angegeben werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// TOA-Felder können ihre Einträge nach in dieser Sammlung definierten Kategorien filtern.
ToaCategories toaCategories = new ToaCategories();
doc.FieldOptions.ToaCategories = toaCategories;

// Diese Sammlung von Kategorien enthält Standardwerte, die wir mit benutzerdefinierten Werten überschreiben können.
Assert.AreEqual("Cases", toaCategories[1]);
Assert.AreEqual("Statutes", toaCategories[2]);

toaCategories[1] = "My Category 1";
toaCategories[2] = "My Category 2";

// Über diese Sammlung können wir jederzeit auf die Standardwerte zugreifen.
Assert.AreEqual("Cases", ToaCategories.DefaultCategories[1]);
Assert.AreEqual("Statutes", ToaCategories.DefaultCategories[2]);

// 2 TOA-Felder einfügen. TOA-Felder erstellen einen Eintrag für jedes TA-Feld im Dokument.
// Verwenden Sie den Schalter „\c“, um den Index einer Kategorie aus unserer Sammlung auszuwählen.
// Mit diesem Schalter nimmt ein TOA-Feld nur Einträge aus TA-Feldern auf, die
// habe auch einen „\c“-Schalter mit einem passenden Kategorieindex. Jedes TOA-Feld wird ebenfalls angezeigt
// der Name der Kategorie, auf die der Schalter „\c“ zeigt.
builder.InsertField("TOA \\c 1 \\h", null);
builder.InsertField("TOA \\c 2 \\h", null);
builder.InsertBreak(BreakType.PageBreak);

// TOA-Einträge in 2 Kategorien einfügen. Unser erstes TOA-Feld erhält einen Eintrag,
// aus dem zweiten TA-Feld, dessen Schalter „\c“ ebenfalls auf die erste Kategorie zeigt.
// Das zweite TOA-Feld enthält zwei Einträge aus den anderen beiden TA-Feldern.
builder.InsertField("TA \\c 2 \\l \"entry 1\"");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertField("TA \\c 1 \\l \"entry 2\"");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertField("TA \\c 2 \\l \"entry 3\"");

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.TOA.Categories.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)


