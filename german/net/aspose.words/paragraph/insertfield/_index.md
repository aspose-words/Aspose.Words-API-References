---
title: Paragraph.InsertField
linktitle: InsertField
articleTitle: InsertField
second_title: Aspose.Words für .NET
description: Fügen Sie mit der Paragraph InsertField-Methode mühelos Felder in Absätze ein. Verbessern Sie die Funktionalität Ihres Dokuments und optimieren Sie die Inhaltsverwaltung.
type: docs
weight: 290
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
| refNode | Node | Verweisknoten innerhalb dieses Absatzes (falls*refNode* Ist`null`, wird dann an das Ende des Absatzes angehängt). |
| isAfter | Boolean | Ob das Feld nach oder vor dem Referenzknoten eingefügt werden soll. |

### Rückgabewert

A[`Field`](../../../aspose.words.fields/field/) Objekt, das das eingefügte Feld darstellt.

## Beispiele

Zeigt verschiedene Möglichkeiten zum Hinzufügen von Feldern zu einem Absatz.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Unten sind drei Möglichkeiten zum Einfügen eines Felds in einen Absatz aufgeführt.
// 1 – Fügen Sie ein AUTOR-Feld in einen Absatz nach einem der untergeordneten Knoten des Absatzes ein:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 – Fügen Sie nach einem der untergeordneten Knoten des Absatzes ein QUOTE-Feld ein:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Fügen Sie vor einem der untergeordneten Knoten des Absatzes ein QUOTE-Feld ein.
// und lasse es einen Platzhalterwert anzeigen:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Dieses Feld zeigt seinen Platzhalterwert an, bis wir es aktualisieren.
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
| refNode | Node | Verweisknoten innerhalb dieses Absatzes (falls*refNode* Ist`null`, wird dann an das Ende des Absatzes angehängt). |
| isAfter | Boolean | Ob das Feld nach oder vor dem Referenzknoten eingefügt werden soll. |

### Rückgabewert

A[`Field`](../../../aspose.words.fields/field/) Objekt, das das eingefügte Feld darstellt.

## Beispiele

Zeigt verschiedene Möglichkeiten zum Hinzufügen von Feldern zu einem Absatz.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Unten sind drei Möglichkeiten zum Einfügen eines Felds in einen Absatz aufgeführt.
// 1 – Fügen Sie ein AUTOR-Feld in einen Absatz nach einem der untergeordneten Knoten des Absatzes ein:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 – Fügen Sie nach einem der untergeordneten Knoten des Absatzes ein QUOTE-Feld ein:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Fügen Sie vor einem der untergeordneten Knoten des Absatzes ein QUOTE-Feld ein.
// und lasse es einen Platzhalterwert anzeigen:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Dieses Feld zeigt seinen Platzhalterwert an, bis wir es aktualisieren.
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
| fieldValue | String | Der einzufügende Feldwert.`null` für Felder, die keinen Wert haben. |
| refNode | Node | Verweisknoten innerhalb dieses Absatzes (falls*refNode* Ist`null`, wird dann an das Ende des Absatzes angehängt). |
| isAfter | Boolean | Ob das Feld nach oder vor dem Referenzknoten eingefügt werden soll. |

### Rückgabewert

A[`Field`](../../../aspose.words.fields/field/) Objekt, das das eingefügte Feld darstellt.

## Beispiele

Zeigt verschiedene Möglichkeiten zum Hinzufügen von Feldern zu einem Absatz.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Unten sind drei Möglichkeiten zum Einfügen eines Felds in einen Absatz aufgeführt.
// 1 – Fügen Sie ein AUTOR-Feld in einen Absatz nach einem der untergeordneten Knoten des Absatzes ein:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 – Fügen Sie nach einem der untergeordneten Knoten des Absatzes ein QUOTE-Feld ein:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Fügen Sie vor einem der untergeordneten Knoten des Absatzes ein QUOTE-Feld ein.
// und lasse es einen Platzhalterwert anzeigen:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Dieses Feld zeigt seinen Platzhalterwert an, bis wir es aktualisieren.
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
