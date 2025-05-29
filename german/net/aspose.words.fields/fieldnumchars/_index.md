---
title: FieldNumChars Class
linktitle: FieldNumChars
articleTitle: FieldNumChars
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fields.FieldNumChars, die für die effiziente Implementierung des NUMCHARS-Felds zur verbesserten Dokumentverarbeitung entwickelt wurde.
type: docs
weight: 2620
url: /de/net/aspose.words.fields/fieldnumchars/
---
## FieldNumChars class

Implementiert das NUMCHARS-Feld.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public class FieldNumChars : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldNumChars](fieldnumchars/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Erhält eine[`FieldFormat`](../fieldformat/)Objekt, das typisierten Zugriff auf die Formatierung des Felds bietet. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer am Dokument vorgenommener Änderungen nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (das Ergebnis sollte nicht neu berechnet werden). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ruft Text ab oder legt ihn fest, der zwischen Feldtrennzeichen und Feldende steht. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann sein`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ruft den Microsoft Word-Feldtyp ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldergebnis von untergeordneten Feldern werden einbezogen. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). |
| [Remove](../../aspose.words.fields/field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte Kind seines übergeordneten Knotens ist, wird dessen übergeordneter Absatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Führt die Feldverknüpfung aus. |
| [Update](../../aspose.words.fields/field/update/)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |

## Bemerkungen

Ruft die Anzahl der Zeichen im aktuellen Dokument ab, wie im**Charaktere** Eigenschaft der integrierten Dokumenteigenschaften.

## Beispiele

Zeigt, wie man die Felder NUMCHARS, NUMWORDS, NUMPAGES und PAGE verwendet, um die Größe unserer Dokumente zu verfolgen.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;

// Unten sind drei Feldtypen aufgeführt, die wir verwenden können, um die Größe unserer Dokumente zu verfolgen.
// 1 – Verfolgen Sie die Zeichenanzahl mit einem NUMCHARS-Feld:
FieldNumChars fieldNumChars = (FieldNumChars)builder.InsertField(FieldType.FieldNumChars, true);       
builder.Writeln(" characters");

// 2 – Verfolgen Sie die Wortanzahl mit einem NUMWORDS-Feld:
FieldNumWords fieldNumWords = (FieldNumWords)builder.InsertField(FieldType.FieldNumWords, true);
builder.Writeln(" words");

// 3 - Verwenden Sie sowohl die Felder PAGE als auch NUMPAGES, um anzuzeigen, auf welcher Seite sich das Feld befindet.
// und die Gesamtzahl der Seiten im Dokument:
builder.ParagraphFormat.Alignment = ParagraphAlignment.Right;
builder.Write("Page ");
FieldPage fieldPage = (FieldPage)builder.InsertField(FieldType.FieldPage, true);
builder.Write(" of ");
FieldNumPages fieldNumPages = (FieldNumPages)builder.InsertField(FieldType.FieldNumPages, true);

Assert.AreEqual(" NUMCHARS ", fieldNumChars.GetFieldCode());
Assert.AreEqual(" NUMWORDS ", fieldNumWords.GetFieldCode());
Assert.AreEqual(" NUMPAGES ", fieldNumPages.GetFieldCode());
Assert.AreEqual(" PAGE ", fieldPage.GetFieldCode());

// Diese Felder behalten in Echtzeit keine genauen Werte bei
// während wir das Dokument programmgesteuert mit Aspose.Words oder in Microsoft Word bearbeiten.
    // Wir müssen sie jedes Mal aktualisieren, wenn wir einen aktuellen Wert sehen möchten.
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.NUMCHARS.NUMWORDS.NUMPAGES.PAGE.docx");
```

### Siehe auch

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
