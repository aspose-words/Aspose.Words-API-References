---
title: Paragraph.InsertField
linktitle: InsertField
articleTitle: InsertField
second_title: Aspose.Words für .NET
description: Paragraph InsertField methode. Fügt ein Feld in diesen Absatz ein in C#.
type: docs
weight: 270
url: /de/net/aspose.words/paragraph/insertfield/
---
## InsertField(*[FieldType](../../../aspose.words.fields/fieldtype/), bool, [Node](../../node/), bool*) {#insertfield}

Fügt ein Feld in diesen Absatz ein.

```csharp
public Field InsertField(FieldType fieldType, bool updateField, Node refNode, bool isAfter)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldType | FieldType | Der Typ des einzufügenden Feldes. |
| updateField | Boolean | Gibt an, ob das Feld sofort aktualisiert werden soll. |
| refNode | Node | Referenzknoten innerhalb dieses Absatzes (falls*refNode* Ist`Null`, wird dann an das Ende des Absatzes angehängt). |
| isAfter | Boolean | Ob das Feld nach oder vor dem Referenzknoten eingefügt werden soll. |

### Rückgabewert

A[`Field`](../../../aspose.words.fields/field/) Objekt, das das eingefügte Feld darstellt.

## Beispiele

Zeigt verschiedene Möglichkeiten zum Hinzufügen von Feldern zu einem Absatz.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Nachfolgend finden Sie drei Möglichkeiten, ein Feld in einen Absatz einzufügen.
// 1 – Fügen Sie ein AUTHOR-Feld in einen Absatz nach einem der untergeordneten Knoten des Absatzes ein:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 – Fügen Sie ein QUOTE-Feld nach einem der untergeordneten Knoten des Absatzes ein:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 – Fügen Sie ein QUOTE-Feld vor einem der untergeordneten Knoten des Absatzes ein.
// und einen Platzhalterwert anzeigen lassen:
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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertField(*string, [Node](../../node/), bool*) {#insertfield_1}

Fügt ein Feld in diesen Absatz ein.

```csharp
public Field InsertField(string fieldCode, Node refNode, bool isAfter)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldCode | String | Der einzufügende Feldcode (ohne geschweifte Klammern). |
| refNode | Node | Referenzknoten innerhalb dieses Absatzes (falls*refNode* Ist`Null`, wird dann an das Ende des Absatzes angehängt). |
| isAfter | Boolean | Ob das Feld nach oder vor dem Referenzknoten eingefügt werden soll. |

### Rückgabewert

A[`Field`](../../../aspose.words.fields/field/) Objekt, das das eingefügte Feld darstellt.

## Beispiele

Zeigt verschiedene Möglichkeiten zum Hinzufügen von Feldern zu einem Absatz.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Nachfolgend finden Sie drei Möglichkeiten, ein Feld in einen Absatz einzufügen.
// 1 – Fügen Sie ein AUTHOR-Feld in einen Absatz nach einem der untergeordneten Knoten des Absatzes ein:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 – Fügen Sie ein QUOTE-Feld nach einem der untergeordneten Knoten des Absatzes ein:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 – Fügen Sie ein QUOTE-Feld vor einem der untergeordneten Knoten des Absatzes ein.
// und einen Platzhalterwert anzeigen lassen:
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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertField(*string, string, [Node](../../node/), bool*) {#insertfield_2}

Fügt ein Feld in diesen Absatz ein.

```csharp
public Field InsertField(string fieldCode, string fieldValue, Node refNode, bool isAfter)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldCode | String | Der einzufügende Feldcode (ohne geschweifte Klammern). |
| fieldValue | String | Der einzufügende Feldwert. Passieren`Null` für Felder, die keinen Wert haben. |
| refNode | Node | Referenzknoten innerhalb dieses Absatzes (falls*refNode* Ist`Null`, wird dann an das Ende des Absatzes angehängt). |
| isAfter | Boolean | Ob das Feld nach oder vor dem Referenzknoten eingefügt werden soll. |

### Rückgabewert

A[`Field`](../../../aspose.words.fields/field/) Objekt, das das eingefügte Feld darstellt.

## Beispiele

Zeigt verschiedene Möglichkeiten zum Hinzufügen von Feldern zu einem Absatz.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Nachfolgend finden Sie drei Möglichkeiten, ein Feld in einen Absatz einzufügen.
// 1 – Fügen Sie ein AUTHOR-Feld in einen Absatz nach einem der untergeordneten Knoten des Absatzes ein:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 – Fügen Sie ein QUOTE-Feld nach einem der untergeordneten Knoten des Absatzes ein:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 – Fügen Sie ein QUOTE-Feld vor einem der untergeordneten Knoten des Absatzes ein.
// und einen Platzhalterwert anzeigen lassen:
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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
