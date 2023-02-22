---
title: MailMerge.DeleteFields
second_title: Aspose.Words för .NET API Referens
description: MailMerge metod. Tar bort sammanslagningsrelaterade fält från dokumentet.
type: docs
weight: 170
url: /sv/net/aspose.words.mailmerging/mailmerge/deletefields/
---
## MailMerge.DeleteFields method

Tar bort sammanslagningsrelaterade fält från dokumentet.

```csharp
public void DeleteFields()
```

### Anmärkningar

Den här metoden tar bort MERGEFIELD- och NEXT-fälten från dokumentet.

Den här metoden kan vara användbar om din sammanslagningsoperation inte alltid behöver för att fylla i alla fält i dokumentet. Använd den här metoden för att ta bort alla återstående sammanslagningsfält.

### Exempel

Visar hur man tar bort alla MERGEFIELDs från ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.Writeln(",");
builder.Writeln("Greetings!");

Assert.AreEqual(
    "Dear \u0013 MERGEFIELD FirstName \u0014«FirstName»\u0015 \u0013 MERGEFIELD LastName \u0014«LastName»\u0015,\rGreetings!", 
    doc.GetText().Trim());

doc.MailMerge.DeleteFields();

Assert.AreEqual("Dear  ,\rGreetings!", doc.GetText().Trim());
```

### Se även

* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../mailmerge/)
* hopsättning [Aspose.Words](../../../)


