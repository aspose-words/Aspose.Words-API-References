---
title: InsertField
second_title: Aspose.Words für .NET-API-Referenz
description: Fügt ein Feld in diesen Absatz ein.
type: docs
weight: 270
url: /de/net/aspose.words/paragraph/insertfield/
---
## InsertField(FieldType, bool, Node, bool) {#insertfield}

Fügt ein Feld in diesen Absatz ein.

```csharp
public Field InsertField(FieldType fieldType, bool updateField, Node refNode, bool isAfter)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldType | FieldType | Der Typ des einzufügenden Felds. |
| updateField | Boolean | Gibt an, ob das Feld sofort aktualisiert werden soll. |
| refNode | Node | Referenzknoten innerhalb dieses Absatzes (wenn refNode null ist, wird es an das Ende des Absatzes angehängt). |
| isAfter | Boolean | Ob das Feld nach oder vor dem Referenzknoten eingefügt werden soll. |

### Rückgabewert

EIN[`Field`](../../../aspose.words.fields/field/) Objekt, das das eingefügte Feld darstellt.

### Beispiele

Zeigt verschiedene Möglichkeiten zum Hinzufügen von Feldern zu einem Absatz.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Nachfolgend finden Sie drei Möglichkeiten, ein Feld in einen Absatz einzufügen.
// 1 - Fügt ein AUTHOR-Feld in einen Absatz nach einem der untergeordneten Knoten des Absatzes ein:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Fügen Sie ein QUOTE-Feld nach einem der untergeordneten Knoten des Absatzes ein:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Füge ein QUOTE-Feld vor einem der untergeordneten Knoten des Absatzes ein,
// und es dazu bringen, einen Platzhalterwert anzuzeigen:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Dieses Feld zeigt seinen Platzhalterwert an, bis wir ihn aktualisieren.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### Siehe auch

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [Node](../../node/)
* class [Paragraph](../)
* namensraum [Aspose.Words](../../paragraph/)
* Montage [Aspose.Words](../../../)

---

## InsertField(string, Node, bool) {#insertfield_1}

Fügt ein Feld in diesen Absatz ein.

```csharp
public Field InsertField(string fieldCode, Node refNode, bool isAfter)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldCode | String | Der einzufügende Feldcode (ohne geschweifte Klammern). |
| refNode | Node | Referenzknoten innerhalb dieses Absatzes (wenn refNode null ist, wird es an das Ende des Absatzes angehängt). |
| isAfter | Boolean | Ob das Feld nach oder vor dem Referenzknoten eingefügt werden soll. |

### Rückgabewert

EIN[`Field`](../../../aspose.words.fields/field/) Objekt, das das eingefügte Feld darstellt.

### Beispiele

Zeigt verschiedene Möglichkeiten zum Hinzufügen von Feldern zu einem Absatz.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Nachfolgend finden Sie drei Möglichkeiten, ein Feld in einen Absatz einzufügen.
// 1 - Fügt ein AUTHOR-Feld in einen Absatz nach einem der untergeordneten Knoten des Absatzes ein:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Fügen Sie ein QUOTE-Feld nach einem der untergeordneten Knoten des Absatzes ein:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Füge ein QUOTE-Feld vor einem der untergeordneten Knoten des Absatzes ein,
// und es dazu bringen, einen Platzhalterwert anzuzeigen:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Dieses Feld zeigt seinen Platzhalterwert an, bis wir ihn aktualisieren.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### Siehe auch

* class [Field](../../../aspose.words.fields/field/)
* class [Node](../../node/)
* class [Paragraph](../)
* namensraum [Aspose.Words](../../paragraph/)
* Montage [Aspose.Words](../../../)

---

## InsertField(string, string, Node, bool) {#insertfield_2}

Fügt ein Feld in diesen Absatz ein.

```csharp
public Field InsertField(string fieldCode, string fieldValue, Node refNode, bool isAfter)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldCode | String | Der einzufügende Feldcode (ohne geschweifte Klammern). |
| fieldValue | String | Der einzufügende Feldwert. Übergeben Sie null für Felder, die keinen Wert haben. |
| refNode | Node | Referenzknoten innerhalb dieses Absatzes (wenn refNode null ist, wird es an das Ende des Absatzes angehängt). |
| isAfter | Boolean | Ob das Feld nach oder vor dem Referenzknoten eingefügt werden soll. |

### Rückgabewert

EIN[`Field`](../../../aspose.words.fields/field/) Objekt, das das eingefügte Feld darstellt.

### Beispiele

Zeigt verschiedene Möglichkeiten zum Hinzufügen von Feldern zu einem Absatz.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Nachfolgend finden Sie drei Möglichkeiten, ein Feld in einen Absatz einzufügen.
// 1 - Fügt ein AUTHOR-Feld in einen Absatz nach einem der untergeordneten Knoten des Absatzes ein:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Fügen Sie ein QUOTE-Feld nach einem der untergeordneten Knoten des Absatzes ein:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Füge ein QUOTE-Feld vor einem der untergeordneten Knoten des Absatzes ein,
// und es dazu bringen, einen Platzhalterwert anzuzeigen:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Dieses Feld zeigt seinen Platzhalterwert an, bis wir ihn aktualisieren.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### Siehe auch

* class [Field](../../../aspose.words.fields/field/)
* class [Node](../../node/)
* class [Paragraph](../)
* namensraum [Aspose.Words](../../paragraph/)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
