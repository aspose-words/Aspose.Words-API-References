---
title: MailMergeOptions.TrimWhitespaces
linktitle: TrimWhitespaces
articleTitle: TrimWhitespaces
second_title: Aspose.Words för .NET
description: Optimera din dokumentkoppling med egenskapen TrimWhitespaces. Hantera enkelt inledande och efterföljande mellanslag för renare och mer professionella dokument.
type: docs
weight: 110
url: /sv/net/aspose.words.lowcode/mailmergeoptions/trimwhitespaces/
---
## MailMergeOptions.TrimWhitespaces property

Hämtar eller anger ett värde som anger om efterföljande och inledande blanksteg ska tas bort från värden för koppling av dokument.

```csharp
public bool TrimWhitespaces { get; set; }
```

## Anmärkningar

Standardvärdet är`sann` .

## Exempel

Visar hur man utför en dokumentkopplingsoperation för en enskild post.

```csharp
// Det finns flera sätt att göra en dokumentkoppling:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.1.docx", fieldNames, fieldValues);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.2.docx", SaveFormat.Docx, fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.3.docx", SaveFormat.Docx, fieldNames, fieldValues, mailMergeOptions);
```

### Se även

* class [MailMergeOptions](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)
