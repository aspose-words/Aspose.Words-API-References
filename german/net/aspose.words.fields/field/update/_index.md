---
title: Field.Update
linktitle: Update
articleTitle: Update
second_title: Aspose.Words für .NET
description: Field Update methode. Führt die Feldaktualisierung durch. Wird ausgelöst wenn das Feld bereits aktualisiert wird in C#.
type: docs
weight: 140
url: /de/net/aspose.words.fields/field/update/
---
## Update() {#update}

Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird.

```csharp
public void Update()
```

## Beispiele

Zeigt, wie man mithilfe von FieldType ein Feld in ein Dokument einfügt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Zwei Felder einfügen und dabei ein Flag übergeben, das bestimmt, ob sie aktualisiert werden, wenn der Builder sie einfügt.
// In manchen Fällen kann das Aktualisieren von Feldern rechenintensiv sein, und es kann eine gute Idee sein, die Aktualisierung zu verschieben.
doc.BuiltInDocumentProperties.Author = "John Doe";
builder.Write("This document was written by ");
builder.InsertField(FieldType.FieldAuthor, updateInsertedFieldsImmediately);

builder.InsertParagraph();
builder.Write("\nThis is page ");
builder.InsertField(FieldType.FieldPage, updateInsertedFieldsImmediately);

Assert.AreEqual(" AUTHOR ", doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(" PAGE ", doc.Range.Fields[1].GetFieldCode());

if (updateInsertedFieldsImmediately)
{
    Assert.AreEqual("John Doe", doc.Range.Fields[0].Result);
    Assert.AreEqual("1", doc.Range.Fields[1].Result);
}
else
{
    Assert.AreEqual(string.Empty, doc.Range.Fields[0].Result);
    Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);

    // Wir müssen diese Felder mithilfe der Aktualisierungsmethoden manuell aktualisieren.
    doc.Range.Fields[0].Update();

    Assert.AreEqual("John Doe", doc.Range.Fields[0].Result);

    doc.UpdateFields();

    Assert.AreEqual("1", doc.Range.Fields[1].Result);
}
```

Zeigt, wie Feldergebnisse formatiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Verwenden Sie einen Dokument-Builder, um ein Feld einzufügen, das ein Ergebnis ohne angewendetes Format anzeigt.
Field field = builder.InsertField("= 2 + 3");

Assert.AreEqual("= 2 + 3", field.GetFieldCode());
Assert.AreEqual("5", field.Result);

// Wir können mithilfe der Eigenschaften des Felds ein Format auf das Ergebnis eines Felds anwenden.
// Nachfolgend sind drei Arten von Formaten aufgeführt, die wir auf das Ergebnis eines Felds anwenden können.
// 1 - Numerisches Format:
FieldFormat format = field.Format;
format.NumericFormat = "$###.00";
field.Update();

Assert.AreEqual("= 2 + 3 \\# $###.00", field.GetFieldCode());
Assert.AreEqual("$  5.00", field.Result);

// 2 - Datums-/Uhrzeitformat:
field = builder.InsertField("DATE");
format = field.Format;
format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());
Console.WriteLine($"Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

// 3 - Allgemeines Format:
field = builder.InsertField("= 25 + 33");
format = field.Format;
format.GeneralFormats.Add(GeneralFormat.LowercaseRoman);
format.GeneralFormats.Add(GeneralFormat.Upper);
field.Update();

int index = 0;
using (IEnumerator<GeneralFormat> generalFormatEnumerator = format.GeneralFormats.GetEnumerator())
    while (generalFormatEnumerator.MoveNext())
        Console.WriteLine($"General format index {index++}: {generalFormatEnumerator.Current}");

Assert.AreEqual("= 25 + 33 \\* roman \\* Upper", field.GetFieldCode());
Assert.AreEqual("LVIII", field.Result);
Assert.AreEqual(2, format.GeneralFormats.Count);
Assert.AreEqual(GeneralFormat.LowercaseRoman, format.GeneralFormats[0]);

// Wir können unsere Formate entfernen, um das Ergebnis des Feldes in seine ursprüngliche Form zurückzusetzen.
format.GeneralFormats.Remove(GeneralFormat.LowercaseRoman);
format.GeneralFormats.RemoveAt(0);
Assert.AreEqual(0, format.GeneralFormats.Count);
field.Update();

Assert.AreEqual("= 25 + 33  ", field.GetFieldCode());
Assert.AreEqual("58", field.Result);
Assert.AreEqual(0, format.GeneralFormats.Count);
```

### Siehe auch

* class [Field](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)

---

## Update(*bool*) {#update_1}

Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird.

```csharp
public void Update(bool ignoreMergeFormat)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| ignoreMergeFormat | Boolean | Wenn`WAHR` dann wird die Formatierung der direkten Feldergebnisse unabhängig vom MERGEFORMAT-Schalter aufgegeben, andernfalls wird eine normale Aktualisierung durchgeführt. |

## Beispiele

Zeigt, wie INCLUDEPICTURE-Felder beim Laden eines Dokuments beibehalten oder verworfen werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldIncludePicture includePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
includePicture.SourceFullName = ImageDir + "Transparent background logo.png";
includePicture.Update(true);

using (MemoryStream docStream = new MemoryStream())
{
    doc.Save(docStream, new OoxmlSaveOptions(SaveFormat.Docx));

    // Wir können in einem LoadOptions-Objekt ein Flag setzen, um zu entscheiden, ob alle INCLUDEPICTURE-Felder konvertiert werden sollen
    // in Bildformen konvertieren, wenn ein Dokument geladen wird, das diese enthält.
    LoadOptions loadOptions = new LoadOptions
    {
        PreserveIncludePictureField = preserveIncludePictureField
    };

    doc = new Document(docStream, loadOptions);

    if (preserveIncludePictureField)
    {
        Assert.True(doc.Range.Fields.Any(f => f.Type == FieldType.FieldIncludePicture));

        doc.UpdateFields();
        doc.Save(ArtifactsDir + "Field.PreserveIncludePicture.docx");
    }
    else
    {
        Assert.False(doc.Range.Fields.Any(f => f.Type == FieldType.FieldIncludePicture));
    }
}
```

### Siehe auch

* class [Field](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
