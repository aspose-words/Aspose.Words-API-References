---
title: ContentDisposition Enum
linktitle: ContentDisposition
articleTitle: ContentDisposition
second_title: Aspose.Words för .NET
description: Utforska Aspose.Words.ContentDisposition-uppräkningen för att upptäcka olika dokumentpresentationsalternativ för förbättrade klientwebbläsarupplevelser.
type: docs
weight: 540
url: /sv/net/aspose.words/contentdisposition/
---
## ContentDisposition enumeration

Listar upp olika sätt att presentera dokumentet i klientens webbläsare.

```csharp
public enum ContentDisposition
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Attachment | `0` | Skicka dokumentet till webbläsaren och visa ett alternativ för att spara dokumentet på disk eller öppna det i programmet som är associerat med dokumentets tillägg. |
| Inline | `1` | Skicka dokumentet till webbläsaren och visa ett alternativ för att spara dokumentet på disk eller öppna det i webbläsaren. |

## Anmärkningar

Observera att det faktiska beteendet i klientens webbläsare kan påverkas av webbläsarens säkerhetskonfiguration.

## Exempel

Visar hur man utför en dokumentkoppling och sedan sparar dokumentet i klientens webbläsare.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD FullName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Company ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Address ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

doc.MailMerge.Execute(new string[] { "FullName", "Company", "Address", "City" },
    new object[] { "James Bond", "MI5 Headquarters", "Milbank", "London" });

// Skicka dokumentet till klientens webbläsare.
//Kastas eftersom HttpResponse är null i testet.
Assert.Throws<ArgumentNullException>(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null));

// Vi måste stänga detta svar manuellt för att säkerställa att vi inte lägger till något överflödigt innehåll i dokumentet efter att det har sparats.
Assert.Throws<NullReferenceException>(() => response.End());
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
