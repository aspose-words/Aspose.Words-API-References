---
title: MailMerge.DeleteFields
linktitle: DeleteFields
articleTitle: DeleteFields
second_title: Aspose.Words för .NET
description: Effektivisera dina dokument enkelt med MailMerge DeleteFields-metoden, och ta bort onödiga fält för koppling av dokument för renare och mer professionella resultat.
type: docs
weight: 170
url: /sv/net/aspose.words.mailmerging/mailmerge/deletefields/
---
## MailMerge.DeleteFields method

Tar bort fält relaterade till koppling av dokument från dokumentet.

```csharp
public void DeleteFields()
```

## Anmärkningar

Den här metoden tar bort fälten MERGEFIELD och NEXT från dokumentet.

Den här metoden kan vara användbar om din dokumentkopplingsåtgärd inte alltid behöver för att fylla i alla fält i dokumentet. Använd den här metoden för att ta bort alla återstående -fält för dokumentkoppling.

## Exempel

Visar hur man tar bort alla MERGEFIELDS från ett dokument.

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
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)
