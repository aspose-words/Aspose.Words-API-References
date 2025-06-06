---
title: DocumentBuilder.InsertField
linktitle: InsertField
articleTitle: InsertField
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre Dokumente mit der InsertField-Methode von DocumentBuilder. Fügen Sie mühelos Word-Felder hinzu und aktualisieren Sie sie für dynamische Inhalte und verbesserte Funktionalität.
type: docs
weight: 330
url: /de/net/aspose.words/documentbuilder/insertfield/
---
## InsertField(*[FieldType](../../../aspose.words.fields/fieldtype/), bool*) {#insertfield}

Fügt ein Word-Feld in ein Dokument ein und aktualisiert optional das Feldergebnis.

```csharp
public Field InsertField(FieldType fieldType, bool updateField)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldType | FieldType | Der Typ des anzuhängenden Feldes. |
| updateField | Boolean | Gibt an, ob das Feld sofort aktualisiert werden soll. |

### Rückgabewert

A[`Field`](../../../aspose.words.fields/field/) Objekt, das das eingefügte Feld darstellt.

## Bemerkungen

Diese Methode fügt ein Feld in ein Dokument ein. Aspose.Words kann Felder aller Typen aktualisieren, aber nicht alle. Weitere Details finden Sie im `InsertField` Überlast.

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

### Siehe auch

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertField(*string*) {#insertfield_1}

Fügt ein Word-Feld in ein Dokument ein und aktualisiert das Feldergebnis.

```csharp
public Field InsertField(string fieldCode)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldCode | String | Der einzufügende Feldcode (ohne geschweifte Klammern). |

### Rückgabewert

A[`Field`](../../../aspose.words.fields/field/) Objekt, das das eingefügte Feld darstellt.

## Bemerkungen

Diese Methode fügt ein Feld in ein Dokument ein und aktualisiert das Feldergebnis sofort. Aspose.Words kann Felder der meisten Typen aktualisieren, aber nicht alle. Weitere Details finden Sie im `InsertField` Überlast.

## Beispiele

Zeigt, wie Sie mithilfe eines Feldcodes ein Feld in ein Dokument einfügen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Diese Überladung der InsertField-Methode aktualisiert eingefügte Felder automatisch.
Assert.True((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1);
```

Zeigt, wie Felder eingefügt und der Cursor des Dokumentgenerators dorthin bewegt wird.

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
// sein Cursor müsste sich innerhalb eines Feldes befinden.
// Um es in einem Feld zu platzieren, müssen wir die MoveTo-Methode des Dokument-Generators aufrufen
// und übergeben Sie den Start- oder Trennknoten des Feldes als Argument.
builder.Write(" Text between our merge fields. ");

doc.Save(ArtifactsDir + "DocumentBuilder.MergeFields.docx");
```

### Siehe auch

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertField(*string, string*) {#insertfield_2}

Fügt ein Word-Feld in ein Dokument ein, ohne das Feldergebnis zu aktualisieren.

```csharp
public Field InsertField(string fieldCode, string fieldValue)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldCode | String | Der einzufügende Feldcode (ohne geschweifte Klammern). |
| fieldValue | String | Der einzufügende Feldwert.`null` für Felder, die keinen Wert haben. |

### Rückgabewert

A[`Field`](../../../aspose.words.fields/field/) Objekt, das das eingefügte Feld darstellt.

## Bemerkungen

Felder in Microsoft Word-Dokumenten bestehen aus einem Feldcode und einem Feldergebnis. Der Feldcode entspricht einer Formel, und das Feldergebnis entspricht dem von der Formel erzeugten Wert. Der Feldcode kann auch Feldschalter enthalten, die zusätzliche Anweisungen zum Ausführen einer bestimmten Aktion darstellen.

Sie können in Ihrem Dokument in Microsoft Word mit der Tastenkombination Alt+F9 zwischen der Anzeige von Feldfunktionen und Ergebnissen wechseln. Feldfunktionen werden in geschweiften Klammern ( { } ) angezeigt.

Um ein Feld zu erstellen, müssen Sie einen Feldtyp, einen Feldcode und einen „Platzhalter“-Feldwert angeben. Wenn Sie sich über die Syntax eines bestimmten Feldcodes nicht sicher sind, erstellen Sie das Feld zuerst in Microsoft Word und wechseln Sie, um seinen Feldcode anzuzeigen.

Aspose.Words kann Feldergebnisse für die meisten Feldtypen berechnen, diese Methode aktualisiert das Feldergebnis jedoch nicht automatisch. Da das Feldergebnis nicht automatisch berechnet wird, müssen Sie einen String-Wert (oder sogar einen leeren String) übergeben, der in das Feldergebnis eingefügt wird. Dieser Wert bleibt als Platzhalter im Feldergebnis erhalten, bis das Feld aktualisiert wird. Um das Feldergebnis zu aktualisieren, können Sie Folgendes aufrufen:[`Update`](../../../aspose.words.fields/field/update/) auf dem Feldobjekt returned an Sie oder[`UpdateFields`](../../document/updatefields/) um Felder im gesamten Dokument zu aktualisieren.

## Beispiele

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

// Verschieben Sie den Dokumentgenerator in die primäre Kopfzeile des ersten Abschnitts.
// die auf jeder Seite in diesem Abschnitt angezeigt wird.
builder.MoveToSection(0);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

// Fügen Sie ein PAGE-Feld ein, das die Nummer der aktuellen Seite anzeigt.
builder.Write("Page ");
builder.InsertField("PAGE", "");

// Konfigurieren Sie den Abschnitt so, dass die in den PAGE-Feldern angezeigte Seitenanzahl bei 5 beginnt.
// Konfigurieren Sie außerdem alle PAGE-Felder so, dass ihre Seitenzahlen mit römischen Großbuchstaben angezeigt werden.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.RestartPageNumbering = true;
pageSetup.PageStartingNumber = 5;
pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;

// Erstellen Sie eine weitere primäre Kopfzeile für den zweiten Abschnitt mit einem weiteren PAGE-Feld.
builder.MoveToSection(1);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write(" - ");
builder.InsertField("PAGE", "");
builder.Write(" - ");

// Konfigurieren Sie den Abschnitt so, dass die in den PAGE-Feldern angezeigte Seitenanzahl bei 10 beginnt.
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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
