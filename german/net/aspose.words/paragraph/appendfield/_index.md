---
title: AppendField
second_title: Aspose.Words für .NET-API-Referenz
description: Fügt diesem Absatz ein Feld hinzu.
type: docs
weight: 240
url: /de/net/aspose.words/paragraph/appendfield/
---
## AppendField(FieldType, bool) {#appendfield}

Fügt diesem Absatz ein Feld hinzu.

```csharp
public Field AppendField(FieldType fieldType, bool updateField)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldType | FieldType | Der Typ des anzuhängenden Felds. |
| updateField | Boolean | Gibt an, ob das Feld sofort aktualisiert werden soll. |

### Rückgabewert

EIN[`Field`](../../../aspose.words.fields/field/) Objekt, das das angehängte Feld darstellt.

### Beispiele

Zeigt verschiedene Möglichkeiten zum Anhängen von Feldern an einen Absatz.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// Nachfolgend finden Sie drei Möglichkeiten, ein Feld an das Ende eines Absatzes anzuhängen.
// 1 - Hängen Sie ein DATE-Feld mit einem Feldtyp an und aktualisieren Sie es dann:
paragraph.AppendField(FieldType.FieldDate, true);

// 2 - Ein TIME-Feld mit einem Feldcode anhängen: 
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - Hängen Sie ein QUOTE-Feld mit einem Feldcode an und lassen Sie einen Platzhalterwert anzeigen:
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
* namensraum [Aspose.Words](../../paragraph/)
* Montage [Aspose.Words](../../../)

---

## AppendField(string) {#appendfield_1}

Fügt diesem Absatz ein Feld hinzu.

```csharp
public Field AppendField(string fieldCode)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldCode | String | Der anzuhängende Feldcode (ohne geschweifte Klammern). |

### Rückgabewert

EIN[`Field`](../../../aspose.words.fields/field/) Objekt, das das angehängte Feld darstellt.

### Beispiele

Zeigt verschiedene Möglichkeiten zum Anhängen von Feldern an einen Absatz.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// Nachfolgend finden Sie drei Möglichkeiten, ein Feld an das Ende eines Absatzes anzuhängen.
// 1 - Hängen Sie ein DATE-Feld mit einem Feldtyp an und aktualisieren Sie es dann:
paragraph.AppendField(FieldType.FieldDate, true);

// 2 - Ein TIME-Feld mit einem Feldcode anhängen: 
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - Hängen Sie ein QUOTE-Feld mit einem Feldcode an und lassen Sie einen Platzhalterwert anzeigen:
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
* namensraum [Aspose.Words](../../paragraph/)
* Montage [Aspose.Words](../../../)

---

## AppendField(string, string) {#appendfield_2}

Fügt diesem Absatz ein Feld hinzu.

```csharp
public Field AppendField(string fieldCode, string fieldValue)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldCode | String | Der anzuhängende Feldcode (ohne geschweifte Klammern). |
| fieldValue | String | Der anzuhängende Feldwert. Übergeben Sie null für Felder, die keinen Wert haben. |

### Rückgabewert

EIN[`Field`](../../../aspose.words.fields/field/) Objekt, das das angehängte Feld darstellt.

### Beispiele

Zeigt verschiedene Möglichkeiten zum Anhängen von Feldern an einen Absatz.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// Nachfolgend finden Sie drei Möglichkeiten, ein Feld an das Ende eines Absatzes anzuhängen.
// 1 - Hängen Sie ein DATE-Feld mit einem Feldtyp an und aktualisieren Sie es dann:
paragraph.AppendField(FieldType.FieldDate, true);

// 2 - Ein TIME-Feld mit einem Feldcode anhängen: 
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - Hängen Sie ein QUOTE-Feld mit einem Feldcode an und lassen Sie einen Platzhalterwert anzeigen:
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
* namensraum [Aspose.Words](../../paragraph/)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
