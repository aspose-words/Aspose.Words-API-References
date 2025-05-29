---
title: FieldGreetingLine Class
linktitle: FieldGreetingLine
articleTitle: FieldGreetingLine
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fields.FieldGreetingLine, die für die mühelose Implementierung von GREETINGLINE-Feldern zur verbesserten Dokumentpersonalisierung entwickelt wurde.
type: docs
weight: 2390
url: /de/net/aspose.words.fields/fieldgreetingline/
---
## FieldGreetingLine class

Implementiert das Feld GREETINGLINE.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public class FieldGreetingLine : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldGreetingLine](fieldgreetingline/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AlternateText](../../aspose.words.fields/fieldgreetingline/alternatetext/) { get; set; } | Ruft den Text ab oder legt ihn fest, der in das Feld aufgenommen werden soll, wenn der Name leer ist. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Erhält eine[`FieldFormat`](../fieldformat/)Objekt, das typisierten Zugriff auf die Formatierung des Felds bietet. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer am Dokument vorgenommener Änderungen nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (das Ergebnis sollte nicht neu berechnet werden). |
| [LanguageId](../../aspose.words.fields/fieldgreetingline/languageid/) { get; set; } | Ruft die Sprach-ID ab oder legt sie fest, die zum Formatieren des Namens verwendet wird. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [NameFormat](../../aspose.words.fields/fieldgreetingline/nameformat/) { get; set; } | Ruft das Format des im Feld enthaltenen Namens ab oder legt es fest. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ruft Text ab oder legt ihn fest, der zwischen Feldtrennzeichen und Feldende steht. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann sein`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ruft den Microsoft Word-Feldtyp ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldergebnis von untergeordneten Feldern werden einbezogen. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). |
| [GetFieldNames](../../aspose.words.fields/fieldgreetingline/getfieldnames/)() | Gibt eine Sammlung von Serienbrieffeldnamen zurück, die vom Feld verwendet werden. |
| [Remove](../../aspose.words.fields/field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte Kind seines übergeordneten Knotens ist, wird dessen übergeordneter Absatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Führt die Feldverknüpfung aus. |
| [Update](../../aspose.words.fields/field/update/)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |

## Bemerkungen

Fügt eine Grußzeile für Serienbriefe ein.

## Beispiele

Zeigt, wie ein GREETINGLINE-Feld eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie eine allgemeine Begrüßung mit einem GREETINGLINE-Feld und etwas Text dahinter.
FieldGreetingLine field = (FieldGreetingLine)builder.InsertField(FieldType.FieldGreetingLine, true);
builder.Writeln("\n\n\tThis is your custom greeting, created programmatically using Aspose Words!");

// Ein GREETINGLINE-Feld akzeptiert während eines Seriendrucks Werte aus einer Datenquelle, wie ein MERGEFIELD.
// Es kann auch formatieren, wie die Daten der Quelle an ihre Stelle geschrieben werden, sobald der Seriendruck abgeschlossen ist.
// Die Feldnamensammlung entspricht den Spalten aus der Datenquelle
// aus der das Feld Werte übernimmt.
Assert.AreEqual(0, field.GetFieldNames().Length);

// Um dieses Array zu füllen, müssen wir ein Format für unsere Begrüßungszeile angeben.
field.NameFormat = "<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> ";

// Jetzt akzeptiert unser Feld Werte aus diesen beiden Spalten in der Datenquelle.
Assert.AreEqual("Courtesy Title", field.GetFieldNames()[0]);
Assert.AreEqual("Last Name", field.GetFieldNames()[1]);
Assert.AreEqual(2, field.GetFieldNames().Length);

// Diese Zeichenfolge deckt alle Fälle ab, in denen die Daten der Datentabelle ungültig sind
// indem der fehlerhafte Name durch eine Zeichenfolge ersetzt wird.
field.AlternateText = "Sir or Madam";

// Legen Sie ein Gebietsschema fest, um das Ergebnis zu formatieren.
field.LanguageId = new CultureInfo("en-US").LCID.ToString();

Assert.AreEqual(" GREETINGLINE  \\f \"<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> \" \\e \"Sir or Madam\" \\l 1033", 
    field.GetFieldCode());

// Erstellen Sie eine Datentabelle mit Spalten, deren Namen mit Elementen übereinstimmen
// aus der Feldnamensammlung des Feldes und führen Sie dann den Serienbrief aus.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// Diese Zeile hat einen ungültigen Wert in der Spalte „Höflichkeitstitel“, daher wird für unsere Begrüßung standardmäßig der alternative Text verwendet.
table.Rows.Add("", "No", "Name");

doc.MailMerge.Execute(table);

Assert.AreEqual(0, doc.Range.Fields.Count);
Assert.AreEqual("Dear Mr. Doe,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Mrs. Cardholder,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Sir or Madam,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!",
    doc.GetText().Trim());
```

### Siehe auch

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
