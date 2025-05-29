---
title: DocumentBuilder.InsertCheckBox
linktitle: InsertCheckBox
articleTitle: InsertCheckBox
second_title: Aspose.Words för .NET
description: Lägg enkelt till interaktiva kryssrutefält med DocumentBuilder-metoden InsertCheckBox, vilket förbättrar användarengagemang i dina dokument.
type: docs
weight: 290
url: /sv/net/aspose.words/documentbuilder/insertcheckbox/
---
## InsertCheckBox(*string, bool, int*) {#insertcheckbox_1}

Infogar ett kryssrutefält på aktuell position.

```csharp
public FormField InsertCheckBox(string name, bool checkedValue, int size)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| name | String | Namnet på formulärfältet. Kan vara en tom sträng. Värde som är längre än 20 tecken kommer att avkortas. |
| checkedValue | Boolean | Kontrollerad status för kryssrutefältet i formuläret. |
| size | Int32 | Anger kryssrutans storlek i punkter. Ange 0 för MS Word för att beräkna kryssrutans storlek automatiskt. |

### Returvärde

Formulärfältnoden som just infogades.

## Anmärkningar

Om du anger ett namn för formulärfältet skapas automatiskt ett bokmärke med samma namn.

## Exempel

Visar hur man infogar kryssrutor i dokumentet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga kryssrutor av varierande storlek och standardstatus för markerade rutor.
builder.Write("Unchecked check box of a default size: ");
builder.InsertCheckBox(string.Empty, false, false, 0);
builder.InsertParagraph();

builder.Write("Large checked check box: ");
builder.InsertCheckBox("CheckBox_Default", true, true, 50);
builder.InsertParagraph();

// Formulärfält har en namngräns på 20 tecken.
builder.Write("Very large checked check box: ");
builder.InsertCheckBox("CheckBox_OnlyCheckedValue", true, 100);

Assert.AreEqual("CheckBox_OnlyChecked", doc.Range.FormFields[2].Name);

// Vi kan interagera med dessa kryssrutor i Microsoft Word genom att dubbelklicka på dem.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertCheckBox.docx");
```

### Se även

* class [FormField](../../../aspose.words.fields/formfield/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## InsertCheckBox(*string, bool, bool, int*) {#insertcheckbox}

Infogar ett kryssrutefält på aktuell position.

```csharp
public FormField InsertCheckBox(string name, bool defaultValue, bool checkedValue, int size)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| name | String | Namnet på formulärfältet. Kan vara en tom sträng. Värde som är längre än 20 tecken kommer att avkortas. |
| defaultValue | Boolean | Standardvärde för kryssrutefältet. |
| checkedValue | Boolean | Aktuell markerad status för kryssrutefältet i formuläret. |
| size | Int32 | Anger kryssrutans storlek i punkter. Ange 0 för MS Word för att beräkna kryssrutans storlek automatiskt. |

### Returvärde

Formulärfältnoden som just infogades.

## Anmärkningar

Om du anger ett namn för formulärfältet skapas automatiskt ett bokmärke med samma namn.

## Exempel

Visar hur man infogar kryssrutor i dokumentet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga kryssrutor av varierande storlek och standardstatus för markerade rutor.
builder.Write("Unchecked check box of a default size: ");
builder.InsertCheckBox(string.Empty, false, false, 0);
builder.InsertParagraph();

builder.Write("Large checked check box: ");
builder.InsertCheckBox("CheckBox_Default", true, true, 50);
builder.InsertParagraph();

// Formulärfält har en namngräns på 20 tecken.
builder.Write("Very large checked check box: ");
builder.InsertCheckBox("CheckBox_OnlyCheckedValue", true, 100);

Assert.AreEqual("CheckBox_OnlyChecked", doc.Range.FormFields[2].Name);

// Vi kan interagera med dessa kryssrutor i Microsoft Word genom att dubbelklicka på dem.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertCheckBox.docx");
```

### Se även

* class [FormField](../../../aspose.words.fields/formfield/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
