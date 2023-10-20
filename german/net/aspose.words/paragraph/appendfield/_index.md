---
title: Paragraph.AppendField
linktitle: AppendField
articleTitle: AppendField
second_title: Aspose.Words für .NET
description: Paragraph AppendField methode. Fügt ein Feld an diesen Absatz an in C#.
type: docs
weight: 240
url: /de/net/aspose.words/paragraph/appendfield/
---
## AppendField(*[FieldType](../../../aspose.words.fields/fieldtype/), bool*) {#appendfield}

Fügt ein Feld an diesen Absatz an.

```csharp
public Field AppendField(FieldType fieldType, bool updateField)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldType | FieldType | Der Typ des anzuhängenden Felds. |
| updateField | Boolean | Gibt an, ob das Feld sofort aktualisiert werden soll. |

### Rückgabewert

A[`Field`](../../../aspose.words.fields/field/) Objekt, das das angehängte Feld darstellt.

## Beispiele

Zeigt verschiedene Möglichkeiten zum Anhängen von Feldern an einen Absatz.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// Nachfolgend finden Sie drei Möglichkeiten, ein Feld an das Ende eines Absatzes anzuhängen.
// 1 – Hängen Sie ein DATE-Feld mithilfe eines Feldtyps an und aktualisieren Sie es dann:
paragraph.AppendField(FieldType.FieldDate, true);

 // 2 – Ein TIME-Feld mithilfe eines Feldcodes anhängen:
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 – Hängen Sie ein QUOTE-Feld mithilfe eines Feldcodes an und lassen Sie es einen Platzhalterwert anzeigen:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// Dieses Feld zeigt seinen Platzhalterwert an, bis wir ihn aktualisieren.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### Siehe auch

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [Paragraph](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## AppendField(*string*) {#appendfield_1}

Fügt ein Feld an diesen Absatz an.

```csharp
public Field AppendField(string fieldCode)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldCode | String | Der anzufügende Feldcode (ohne geschweifte Klammern). |

### Rückgabewert

A[`Field`](../../../aspose.words.fields/field/) Objekt, das das angehängte Feld darstellt.

## Beispiele

Zeigt verschiedene Möglichkeiten zum Anhängen von Feldern an einen Absatz.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// Nachfolgend finden Sie drei Möglichkeiten, ein Feld an das Ende eines Absatzes anzuhängen.
// 1 – Hängen Sie ein DATE-Feld mithilfe eines Feldtyps an und aktualisieren Sie es dann:
paragraph.AppendField(FieldType.FieldDate, true);

 // 2 – Ein TIME-Feld mithilfe eines Feldcodes anhängen:
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 – Hängen Sie ein QUOTE-Feld mithilfe eines Feldcodes an und lassen Sie es einen Platzhalterwert anzeigen:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// Dieses Feld zeigt seinen Platzhalterwert an, bis wir ihn aktualisieren.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### Siehe auch

* class [Field](../../../aspose.words.fields/field/)
* class [Paragraph](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## AppendField(*string, string*) {#appendfield_2}

Fügt ein Feld an diesen Absatz an.

```csharp
public Field AppendField(string fieldCode, string fieldValue)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldCode | String | Der anzufügende Feldcode (ohne geschweifte Klammern). |
| fieldValue | String | Der anzufügende Feldwert. Passieren`Null` für Felder, die keinen Wert haben. |

### Rückgabewert

A[`Field`](../../../aspose.words.fields/field/) Objekt, das das angehängte Feld darstellt.

## Beispiele

Zeigt verschiedene Möglichkeiten zum Anhängen von Feldern an einen Absatz.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// Nachfolgend finden Sie drei Möglichkeiten, ein Feld an das Ende eines Absatzes anzuhängen.
// 1 – Hängen Sie ein DATE-Feld mithilfe eines Feldtyps an und aktualisieren Sie es dann:
paragraph.AppendField(FieldType.FieldDate, true);

 // 2 – Ein TIME-Feld mithilfe eines Feldcodes anhängen:
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 – Hängen Sie ein QUOTE-Feld mithilfe eines Feldcodes an und lassen Sie es einen Platzhalterwert anzeigen:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// Dieses Feld zeigt seinen Platzhalterwert an, bis wir ihn aktualisieren.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### Siehe auch

* class [Field](../../../aspose.words.fields/field/)
* class [Paragraph](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
