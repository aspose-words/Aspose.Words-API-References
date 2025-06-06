---
title: FieldGreetingLine.LanguageId
linktitle: LanguageId
articleTitle: LanguageId
second_title: Aspose.Words per .NET
description: Scopri la proprietà LanguageId di FieldGreetingLine per gestire facilmente la formattazione dei nomi con impostazioni di lingua personalizzabili per un'esperienza utente migliorata.
type: docs
weight: 30
url: /it/net/aspose.words.fields/fieldgreetingline/languageid/
---
## FieldGreetingLine.LanguageId property

Ottiene o imposta l'ID della lingua utilizzata per formattare il nome.

```csharp
public string LanguageId { get; set; }
```

## Esempi

Mostra come inserire un campo GREETINGLINE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un saluto generico utilizzando un campo GREETINGLINE e del testo dopo di esso.
FieldGreetingLine field = (FieldGreetingLine)builder.InsertField(FieldType.FieldGreetingLine, true);
builder.Writeln("\n\n\tThis is your custom greeting, created programmatically using Aspose Words!");

// Un campo GREETINGLINE accetta valori da un'origine dati durante una stampa unione, come un MERGEFIELD.
// Può anche formattare il modo in cui i dati di origine vengono scritti al suo posto una volta completata la stampa unione.
// La raccolta dei nomi dei campi corrisponde alle colonne dell'origine dati
// da cui il campo prenderà i valori.
Assert.AreEqual(0, field.GetFieldNames().Length);

// Per popolare tale array, dobbiamo specificare un formato per la nostra riga di saluto.
field.NameFormat = "<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> ";

// Ora il nostro campo accetterà i valori da queste due colonne nell'origine dati.
Assert.AreEqual("Courtesy Title", field.GetFieldNames()[0]);
Assert.AreEqual("Last Name", field.GetFieldNames()[1]);
Assert.AreEqual(2, field.GetFieldNames().Length);

// Questa stringa coprirà tutti i casi in cui i dati della tabella dati non sono validi
// sostituendo il nome non valido con una stringa.
field.AlternateText = "Sir or Madam";

// Imposta le impostazioni locali per formattare il risultato.
field.LanguageId = new CultureInfo("en-US").LCID.ToString();

Assert.AreEqual(" GREETINGLINE  \\f \"<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> \" \\e \"Sir or Madam\" \\l 1033", 
    field.GetFieldCode());

// Crea una tabella dati con colonne i cui nomi corrispondono agli elementi
// dalla raccolta dei nomi dei campi del campo, quindi eseguire la stampa unione.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// Questa riga contiene un valore non valido nella colonna Titolo di cortesia, quindi il nostro saluto utilizzerà per impostazione predefinita il testo alternativo.
table.Rows.Add("", "No", "Name");

doc.MailMerge.Execute(table);

Assert.AreEqual(0, doc.Range.Fields.Count);
Assert.AreEqual("Dear Mr. Doe,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Mrs. Cardholder,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Sir or Madam,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!",
    doc.GetText().Trim());
```

### Guarda anche

* class [FieldGreetingLine](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
