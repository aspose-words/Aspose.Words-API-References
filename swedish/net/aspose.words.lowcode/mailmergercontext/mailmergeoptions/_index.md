---
title: MailMergerContext.MailMergeOptions
linktitle: MailMergeOptions
articleTitle: MailMergeOptions
second_title: Aspose.Words för .NET
description: Upptäck MailMergeContext MailMergeOptions-funktionen för att effektivisera din dokumentautomation och förbättra effektiviteten i ditt arbetsflöde utan ansträngning.
type: docs
weight: 20
url: /sv/net/aspose.words.lowcode/mailmergercontext/mailmergeoptions/
---
## MailMergerContext.MailMergeOptions property

Alternativ för dokumentkoppling.

```csharp
public MailMergeOptions MailMergeOptions { get; }
```

## Exempel

Visar hur man utför en dokumentkopplingsoperation för en enskild post med hjälp av kontext.

```csharp
// Det finns flera sätt att göra en dokumentkoppling:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMergerContext mailMergerContext = new MailMergerContext();
mailMergerContext.SetSimpleDataSource(fieldNames, fieldValues);
mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

MailMerger.Create(mailMergerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.MailMergeContext.docx")
    .Execute();
```

Visar hur man utför en dokumentkopplingsåtgärd för en enskild post från strömmen med hjälp av kontext.

```csharp
// Det finns flera sätt att göra en dokumentkoppling med hjälp av dokument från strömmen:
string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    MailMergerContext mailMergerContext = new MailMergerContext();
    mailMergerContext.SetSimpleDataSource(fieldNames, fieldValues);
    mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeContextStream.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Create(mailMergerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Se även

* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMergerContext](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)
