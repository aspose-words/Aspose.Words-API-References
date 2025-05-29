---
title: FieldGreetingLine.AlternateText
linktitle: AlternateText
articleTitle: AlternateText
second_title: Aspose.Words för .NET
description: Upptäck hur du använder egenskapen FieldGreetingLine AlternateText för att förbättra användarupplevelsen genom att visa anpassad text när namn saknas.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldgreetingline/alternatetext/
---
## FieldGreetingLine.AlternateText property

Hämtar eller ställer in texten som ska inkluderas i fältet om namnet är tomt.

```csharp
public string AlternateText { get; set; }
```

## Exempel

Visar hur man infogar ett fält för HÄLSNINGSLINJER.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa en generisk hälsning med hjälp av ett HÄLSNINGSLINJE-fält och lite text efter det.
FieldGreetingLine field = (FieldGreetingLine)builder.InsertField(FieldType.FieldGreetingLine, true);
builder.Writeln("\n\n\tThis is your custom greeting, created programmatically using Aspose Words!");

// Ett GREEETINGLINE-fält accepterar värden från en datakälla under en dokumentkoppling, som ett MERGEFIELD.
// Den kan också formatera hur källdata skrivs på plats när dokumentkopplingen är klar.
// Fältnamnssamlingen motsvarar kolumnerna från datakällan
// som fältet kommer att ta värden från.
Assert.AreEqual(0, field.GetFieldNames().Length);

// För att fylla i den arrayen måste vi ange ett format för vår hälsningsrad.
field.NameFormat = "<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> ";

// Nu kommer vårt fält att acceptera värden från dessa två kolumner i datakällan.
Assert.AreEqual("Courtesy Title", field.GetFieldNames()[0]);
Assert.AreEqual("Last Name", field.GetFieldNames()[1]);
Assert.AreEqual(2, field.GetFieldNames().Length);

// Denna sträng täcker alla fall där datatabellens data är ogiltiga
// genom att ersätta det felaktigt utformade namnet med en sträng.
field.AlternateText = "Sir or Madam";

// Ange en språkinställning för att formatera resultatet.
field.LanguageId = new CultureInfo("en-US").LCID.ToString();

Assert.AreEqual(" GREETINGLINE  \\f \"<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> \" \\e \"Sir or Madam\" \\l 1033", 
    field.GetFieldCode());

// Skapa en datatabell med kolumner vars namn matchar element
// från fältets fältnamnssamling och utför sedan dokumentkopplingen.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// Den här raden har ett ogiltigt värde i kolumnen Titel för artighet, så vår hälsning kommer som standard att vara den alternativa texten.
table.Rows.Add("", "No", "Name");

doc.MailMerge.Execute(table);

Assert.AreEqual(0, doc.Range.Fields.Count);
Assert.AreEqual("Dear Mr. Doe,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Mrs. Cardholder,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Sir or Madam,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!",
    doc.GetText().Trim());
```

### Se även

* class [FieldGreetingLine](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
