---
title: Field.Update
linktitle: Update
articleTitle: Update
second_title: Aspose.Words für .NET
description: Aktualisieren Sie Felder effizient mit unserer Feldaktualisierungsmethode. Verhindert Konflikte, indem sichergestellt wird, dass Felder nicht bereits verwendet werden. Optimieren Sie noch heute Ihr Datenmanagement!
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

Zeigt, wie mit FieldType ein Feld in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie zwei Felder ein und übergeben Sie dabei ein Flag, das bestimmt, ob sie beim Einfügen durch den Builder aktualisiert werden sollen.
// In einigen Fällen kann das Aktualisieren von Feldern rechenintensiv sein und es kann eine gute Idee sein, das Update zu verschieben.
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

    // Wir müssen diese Felder manuell mit den Aktualisierungsmethoden aktualisieren.
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

// Verwenden Sie einen Dokumentgenerator, um ein Feld einzufügen, das ein Ergebnis ohne angewendetes Format anzeigt.
Field field = builder.InsertField("= 2 + 3");

Assert.AreEqual("= 2 + 3", field.GetFieldCode());
Assert.AreEqual("5", field.Result);

// Wir können mithilfe der Feldeigenschaften ein Format auf das Ergebnis eines Felds anwenden.
// Unten sind drei Arten von Formaten aufgeführt, die wir auf das Ergebnis eines Felds anwenden können.
// 1 - Numerisches Format:
FieldFormat format = field.Format;
format.NumericFormat = "$###.00";
field.Update();

Assert.AreEqual("= 2 + 3 \\# $###.00", field.GetFieldCode());
Assert.AreEqual("$  5.00", field.Result);

// 2 - Datums-/Zeitformat:
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

// Wir können unsere Formate entfernen, um das Ergebnis des Felds in seine ursprüngliche Form zurückzusetzen.
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
| ignoreMergeFormat | Boolean | Wenn`WAHR` dann wird die direkte Feldergebnisformatierung unabhängig vom MERGEFORMAT-Schalter abgebrochen, andernfalls wird eine normale Aktualisierung durchgeführt. |

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

    // Wir können ein Flag in einem LoadOptions-Objekt setzen, um zu entscheiden, ob alle INCLUDEPICTURE-Felder konvertiert werden sollen
    // in Bildformen, wenn ein Dokument geladen wird, das diese enthält.
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
