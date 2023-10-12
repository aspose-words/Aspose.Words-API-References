---
title: Class FieldGreetingLine
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Fields.FieldGreetingLine klas. Implementiert das GREETINGLINEFeld.
type: docs
weight: 1980
url: /de/net/aspose.words.fields/fieldgreetingline/
---
## FieldGreetingLine class

Implementiert das GREETINGLINE-Feld.

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
| [AlternateText](../../aspose.words.fields/fieldgreetingline/alternatetext/) { get; set; } | Ruft den in das Feld aufzunehmenden Text ab oder legt diesen fest, wenn der Name leer ist. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Ruft a ab[`FieldFormat`](../fieldformat/) Objekt, das typisierten Zugriff auf die Formatierung des Felds bietet. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer am Dokument vorgenommener Änderungen nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (sollte sein Ergebnis nicht neu berechnen). |
| [LanguageId](../../aspose.words.fields/fieldgreetingline/languageid/) { get; set; } | Ruft die Sprach-ID ab, die zum Formatieren des Namens verwendet wird, oder legt diese fest. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [NameFormat](../../aspose.words.fields/fieldgreetingline/nameformat/) { get; set; } | Ruft das Format des im Feld enthaltenen Namens ab oder legt dieses fest. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ruft Text ab, der zwischen dem Feldtrennzeichen und dem Feldende liegt, oder legt diesen fest. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann sein`Null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ruft den Microsoft Word-Feldtyp ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl der Feldcode als auch das Feldergebnis der untergeordneten Felder sind enthalten. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). |
| [GetFieldNames](../../aspose.words.fields/fieldgreetingline/getfieldnames/)() | Gibt eine Sammlung von Serienbrieffeldnamen zurück, die vom Feld verwendet werden. |
| [Remove](../../aspose.words.fields/field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte child seines übergeordneten Knotens ist, wird dessen übergeordneter Absatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben`Null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Führt das Feld unlink aus. |
| [Update](../../aspose.words.fields/field/update/)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |

### Bemerkungen

Fügt eine Begrüßungszeile für den Serienbrief ein.

### Beispiele

Zeigt, wie ein GREETINGLINE-Feld eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie eine generische Begrüßung mit einem GREETINGLINE-Feld und etwas Text danach.
FieldGreetingLine field = (FieldGreetingLine)builder.InsertField(FieldType.FieldGreetingLine, true);
builder.Writeln("\n\n\tThis is your custom greeting, created programmatically using Aspose Words!");

// Ein GREETINGLINE-Feld akzeptiert während eines Seriendrucks Werte aus einer Datenquelle, wie ein MERGEFIELD.
// Es kann auch formatieren, wie die Daten der Quelle an ihre Stelle geschrieben werden, sobald der Seriendruck abgeschlossen ist.
// Die Feldnamensammlung entspricht den Spalten aus der Datenquelle
// aus dem das Feld Werte annimmt.
Assert.AreEqual(0, field.GetFieldNames().Length);

// Um dieses Array zu füllen, müssen wir ein Format für unsere Begrüßungszeile angeben.
field.NameFormat = "<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> ";

// Jetzt akzeptiert unser Feld Werte aus diesen beiden Spalten in der Datenquelle.
Assert.AreEqual("Courtesy Title", field.GetFieldNames()[0]);
Assert.AreEqual("Last Name", field.GetFieldNames()[1]);
Assert.AreEqual(2, field.GetFieldNames().Length);

// Diese Zeichenfolge deckt alle Fälle ab, in denen die Daten der Datentabelle ungültig sind
// durch Ersetzen des fehlerhaften Namens durch eine Zeichenfolge.
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

// Diese Zeile hat einen ungültigen Wert in der Spalte „Mit freundlicher Genehmigung des Titels“, sodass unsere Begrüßung standardmäßig den alternativen Text verwendet.
table.Rows.Add("", "No", "Name");

doc.MailMerge.Execute(table);

Assert.That(doc.Range.Fields, Is.Empty);
Assert.AreEqual("Dear Mr. Doe,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Mrs. Cardholder,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Sir or Madam,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!",
    doc.GetText().Trim());
```

### Siehe auch

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)


