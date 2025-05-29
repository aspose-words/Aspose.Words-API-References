---
title: FieldOptions.ToaCategories
linktitle: ToaCategories
articleTitle: ToaCategories
second_title: Aspose.Words für .NET
description: Entdecken Sie FieldOptions ToaCategories. Verwalten und passen Sie die Kategorien Ihres Rechtsgrundlagenverzeichnisses ganz einfach an, um die Organisation und Effizienz zu verbessern.
type: docs
weight: 200
url: /de/net/aspose.words.fields/fieldoptions/toacategories/
---
## FieldOptions.ToaCategories property

Ruft die Kategorien des Rechtsgrundlagenverzeichnisses ab oder legt sie fest.

```csharp
public ToaCategories ToaCategories { get; set; }
```

## Beispiele

Zeigt, wie ein Satz von Kategorien für TOA-Felder angegeben wird.

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
// haben auch einen "\c"-Schalter mit einem passenden Kategorieindex. Jedes TOA-Feld zeigt auch
// der Name der Kategorie, auf die der Schalter "\c" verweist.
builder.InsertField("TOA \\c 1 \\h", null);
builder.InsertField("TOA \\c 2 \\h", null);
builder.InsertBreak(BreakType.PageBreak);

// TOA-Einträge in zwei Kategorien einfügen. Unser erstes TOA-Feld erhält einen Eintrag,
// aus dem zweiten TA-Feld, dessen "\c"-Schalter ebenfalls auf die erste Kategorie zeigt.
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

* class [ToaCategories](../../toacategories/)
* class [FieldOptions](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
