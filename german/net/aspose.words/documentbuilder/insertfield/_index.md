---
title: DocumentBuilder.InsertField
second_title: Aspose.Words für .NET-API-Referenz
description: DocumentBuilder methode. Fügt ein WordFeld in ein Dokument ein und aktualisiert optional das Feldergebnis.
type: docs
weight: 300
url: /de/net/aspose.words/documentbuilder/insertfield/
---
## InsertField(FieldType, bool) {#insertfield}

Fügt ein Word-Feld in ein Dokument ein und aktualisiert optional das Feldergebnis.

```csharp
public Field InsertField(FieldType fieldType, bool updateField)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldType | FieldType | Der Typ des anzuhängenden Felds. |
| updateField | Boolean | Gibt an, ob das Feld sofort aktualisiert werden soll. |

### Rückgabewert

EIN[`Field`](../../../aspose.words.fields/field/) Objekt, das das eingefügte Feld darstellt.

### Bemerkungen

Diese Methode fügt ein Feld in ein Dokument ein. Aspose.Words kann Felder der meisten Typen aktualisieren, aber nicht alle. Weitere Einzelheiten finden Sie unter the `InsertField` Überlast.

### Beispiele

Zeigt, wie ein Feld mithilfe von FieldType in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie zwei Felder ein, während Sie ein Flag übergeben, das bestimmt, ob sie aktualisiert werden, wenn der Builder sie einfügt.
// In einigen Fällen kann das Aktualisieren von Feldern rechenintensiv sein, und es kann eine gute Idee sein, die Aktualisierung zu verschieben.
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

    // Wir müssen diese Felder mit den Aktualisierungsmethoden manuell aktualisieren.
    doc.Range.Fields[0].Update();

    Assert.AreEqual("John Doe", doc.Range.Fields[0].Result);

    doc.UpdateFields();

    Assert.AreEqual("1", doc.Range.Fields[1].Result);
}
```

### Siehe auch

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)

---

## InsertField(string) {#insertfield_1}

Fügt ein Word-Feld in ein Dokument ein und aktualisiert das Feldergebnis.

```csharp
public Field InsertField(string fieldCode)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldCode | String | Der einzufügende Feldcode (ohne geschweifte Klammern). |

### Rückgabewert

EIN[`Field`](../../../aspose.words.fields/field/) Objekt, das das eingefügte Feld darstellt.

### Bemerkungen

Diese Methode fügt ein Feld in ein Dokument ein und aktualisiert das Feldergebnis sofort. Aspose.Words kann Felder der meisten Typen aktualisieren, aber nicht alle. Weitere Einzelheiten finden Sie unter the `InsertField` Überlast.

### Beispiele

Zeigt, wie ein Feld mithilfe eines Feldcodes in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Diese Überladung der InsertField-Methode aktualisiert automatisch eingefügte Felder.
Assert.That(DateTime.Parse(field.Result), Is.EqualTo(DateTime.Today).Within(1).Days);
```

Zeigt, wie man Felder einfügt und den Cursor des Document Builders darauf bewegt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField(@"MERGEFIELD MyMergeField1 \* MERGEFORMAT");
builder.InsertField(@"MERGEFIELD MyMergeField2 \* MERGEFORMAT");

// Bewegen Sie den Cursor zum ersten MERGEFIELD.
builder.MoveToMergeField("MyMergeField1", true, false);

// Beachten Sie, dass der Cursor unmittelbar nach dem ersten MERGEFIELD und vor dem zweiten platziert wird.
Assert.AreEqual(doc.Range.Fields[1].Start, builder.CurrentNode);
Assert.AreEqual(doc.Range.Fields[0].End, builder.CurrentNode.PreviousSibling);

// Wenn wir den Feldcode oder den Inhalt des Felds mit dem Builder bearbeiten möchten,
// sein Cursor müsste sich in einem Feld befinden.
// Um es in einem Feld zu platzieren, müssten wir die MoveTo-Methode des Dokumentenerstellers aufrufen
// und übergeben Sie den Start- oder Trennknoten des Felds als Argument.
builder.Write(" Text between our merge fields. ");

doc.Save(ArtifactsDir + "DocumentBuilder.MergeFields.docx");
```

### Siehe auch

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)

---

## InsertField(string, string) {#insertfield_2}

Fügt ein Word-Feld in ein Dokument ein, ohne das Feldergebnis zu aktualisieren.

```csharp
public Field InsertField(string fieldCode, string fieldValue)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldCode | String | Der einzufügende Feldcode (ohne geschweifte Klammern). |
| fieldValue | String | Der einzufügende Feldwert. Übergeben Sie null für Felder, die keinen Wert haben. |

### Rückgabewert

EIN[`Field`](../../../aspose.words.fields/field/) Objekt, das das eingefügte Feld darstellt.

### Bemerkungen

Felder in Microsoft Word-Dokumenten bestehen aus einem Feldcode und einem Feldergebnis. Der Feldcode ist wie eine Formel und das Feldergebnis ist wie der Wert, den die Formel erzeugt. Der Feldcode kann auch Feldswitches enthalten, die wie zusätzliche Anweisungen zum Ausführen einer bestimmten Aktion sind.

Sie können zwischen der Anzeige von Feldcodes und Ergebnissen in Ihrem Dokument in Microsoft Word wechseln, indem Sie die Tastenkombination Alt+F9 verwenden. Feldcodes werden zwischen geschweiften Klammern ( { } ) angezeigt.

Um ein Feld zu erstellen, müssen Sie einen Feldtyp, einen Feldcode und einen „Platzhalter“-Feldwert angeben. Wenn Sie sich bezüglich einer bestimmten Feldcodesyntax nicht sicher sind, erstellen Sie das Feld zuerst in Microsoft Word und wechseln Sie, um seinen Feldcode anzuzeigen .

Aspose.Words kann Feldergebnisse für die meisten Feldtypen berechnen, aber diese Methode aktualisiert das Feldergebnis nicht automatisch. Da das Feldergebnis nicht automatisch berechnet wird, wird erwartet, dass Sie einen Zeichenfolgenwert (oder sogar eine leere Zeichenfolge) übergeben, der in das Feldergebnis eingefügt wird. Dieser Wert verbleibt als Platzhalter im Feldergebnis, bis das Feld ist updated. Um das Feldergebnis zu aktualisieren, können Sie aufrufen[`Update`](../../../aspose.words.fields/field/update/)auf dem Feldobjekt return an Sie oder[`UpdateFields`](../../document/updatefields/) um Felder im gesamten Dokument zu aktualisieren.

### Beispiele

Zeigt, wie die Seitennummerierung in einem Abschnitt eingerichtet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 3.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("Section 2, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 3.");

// Verschieben Sie den Document Builder in die primäre Kopfzeile des ersten Abschnitts,
// die jede Seite in diesem Abschnitt anzeigen wird.
builder.MoveToSection(0);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

// Fügen Sie ein PAGE-Feld ein, das die Nummer der aktuellen Seite anzeigt.
builder.Write("Page ");
builder.InsertField("PAGE", "");

// Konfigurieren Sie den Abschnitt so, dass die Seitenzahl, die die PAGE-Felder anzeigen, bei 5 beginnt.
// Konfigurieren Sie außerdem alle PAGE-Felder so, dass ihre Seitenzahlen mit römischen Großbuchstaben angezeigt werden.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.RestartPageNumbering = true;
pageSetup.PageStartingNumber = 5;
pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;

// Erstellen Sie einen weiteren primären Header für den zweiten Abschnitt mit einem weiteren PAGE-Feld.
builder.MoveToSection(1);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write(" - ");
builder.InsertField("PAGE", "");
builder.Write(" - ");

// Konfigurieren Sie den Abschnitt so, dass die Seitenzahl, die die PAGE-Felder anzeigen, bei 10 beginnt.
// Konfigurieren Sie außerdem alle PAGE-Felder so, dass ihre Seitenzahlen mit arabischen Zahlen angezeigt werden.
pageSetup = doc.Sections[1].PageSetup;
pageSetup.PageStartingNumber = 10;
pageSetup.RestartPageNumbering = true;
pageSetup.PageNumberStyle = NumberStyle.Arabic;

doc.Save(ArtifactsDir + "PageSetup.PageNumbering.docx");
```

### Siehe auch

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)


