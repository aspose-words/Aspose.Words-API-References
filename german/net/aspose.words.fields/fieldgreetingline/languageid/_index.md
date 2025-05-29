---
title: FieldGreetingLine.LanguageId
linktitle: LanguageId
articleTitle: LanguageId
second_title: Aspose.Words für .NET
description: Entdecken Sie die LanguageId-Eigenschaft von FieldGreetingLine, um die Namensformatierung mit anpassbaren Spracheinstellungen für ein verbessertes Benutzererlebnis einfach zu verwalten.
type: docs
weight: 30
url: /de/net/aspose.words.fields/fieldgreetingline/languageid/
---
## FieldGreetingLine.LanguageId property

Ruft die Sprach-ID ab oder legt sie fest, die zum Formatieren des Namens verwendet wird.

```csharp
public string LanguageId { get; set; }
```

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

* class [FieldGreetingLine](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
