---
title: DocumentBuilder.InsertCheckBox
linktitle: InsertCheckBox
articleTitle: InsertCheckBox
second_title: Aspose.Words für .NET
description: Fügen Sie mit der InsertCheckBox-Methode von DocumentBuilder mühelos interaktive Kontrollkästchen-Formularfelder hinzu und verbessern Sie so die Benutzerinteraktion mit Ihren Dokumenten.
type: docs
weight: 290
url: /de/net/aspose.words/documentbuilder/insertcheckbox/
---
## InsertCheckBox(*string, bool, int*) {#insertcheckbox_1}

Fügt an der aktuellen Position ein Kontrollkästchen-Formularfeld ein.

```csharp
public FormField InsertCheckBox(string name, bool checkedValue, int size)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | String | Der Name des Formularfelds. Kann eine leere Zeichenfolge sein. Werte mit mehr als 20 Zeichen werden abgeschnitten. |
| checkedValue | Boolean | Überprüfter Status des Kontrollkästchen-Formularfelds. |
| size | Int32 | Gibt die Größe des Kontrollkästchens in Punkt an. Geben Sie 0 für MS Word an, um die Größe des Kontrollkästchens automatisch zu berechnen. |

### Rückgabewert

Der gerade eingefügte Formularfeldknoten.

## Bemerkungen

Wenn Sie einen Namen für das Formularfeld angeben, wird automatisch ein Lesezeichen mit demselben Namen erstellt.

## Beispiele

Zeigt, wie Kontrollkästchen in das Dokument eingefügt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Kontrollkästchen unterschiedlicher Größe und mit standardmäßig aktiviertem Status einfügen.
builder.Write("Unchecked check box of a default size: ");
builder.InsertCheckBox(string.Empty, false, false, 0);
builder.InsertParagraph();

builder.Write("Large checked check box: ");
builder.InsertCheckBox("CheckBox_Default", true, true, 50);
builder.InsertParagraph();

// Die Namenslänge von Formularfeldern ist auf 20 Zeichen begrenzt.
builder.Write("Very large checked check box: ");
builder.InsertCheckBox("CheckBox_OnlyCheckedValue", true, 100);

Assert.AreEqual("CheckBox_OnlyChecked", doc.Range.FormFields[2].Name);

// Wir können mit diesen Kontrollkästchen in Microsoft Word interagieren, indem wir darauf doppelklicken.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertCheckBox.docx");
```

### Siehe auch

* class [FormField](../../../aspose.words.fields/formfield/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertCheckBox(*string, bool, bool, int*) {#insertcheckbox}

Fügt an der aktuellen Position ein Kontrollkästchen-Formularfeld ein.

```csharp
public FormField InsertCheckBox(string name, bool defaultValue, bool checkedValue, int size)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | String | Der Name des Formularfelds. Kann eine leere Zeichenfolge sein. Werte mit mehr als 20 Zeichen werden abgeschnitten. |
| defaultValue | Boolean | Standardwert des Kontrollkästchen-Formularfelds. |
| checkedValue | Boolean | Aktueller aktivierter Status des Kontrollkästchen-Formularfelds. |
| size | Int32 | Gibt die Größe des Kontrollkästchens in Punkt an. Geben Sie 0 für MS Word an, um die Größe des Kontrollkästchens automatisch zu berechnen. |

### Rückgabewert

Der gerade eingefügte Formularfeldknoten.

## Bemerkungen

Wenn Sie einen Namen für das Formularfeld angeben, wird automatisch ein Lesezeichen mit demselben Namen erstellt.

## Beispiele

Zeigt, wie Kontrollkästchen in das Dokument eingefügt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Kontrollkästchen unterschiedlicher Größe und mit standardmäßig aktiviertem Status einfügen.
builder.Write("Unchecked check box of a default size: ");
builder.InsertCheckBox(string.Empty, false, false, 0);
builder.InsertParagraph();

builder.Write("Large checked check box: ");
builder.InsertCheckBox("CheckBox_Default", true, true, 50);
builder.InsertParagraph();

// Die Namenslänge von Formularfeldern ist auf 20 Zeichen begrenzt.
builder.Write("Very large checked check box: ");
builder.InsertCheckBox("CheckBox_OnlyCheckedValue", true, 100);

Assert.AreEqual("CheckBox_OnlyChecked", doc.Range.FormFields[2].Name);

// Wir können mit diesen Kontrollkästchen in Microsoft Word interagieren, indem wir darauf doppelklicken.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertCheckBox.docx");
```

### Siehe auch

* class [FormField](../../../aspose.words.fields/formfield/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
