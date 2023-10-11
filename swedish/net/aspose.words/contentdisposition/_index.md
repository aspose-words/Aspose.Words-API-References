---
title: Enum ContentDisposition
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.ContentDisposition uppräkning. Räknar upp olika sätt att presentera dokumentet i klientens webbläsare.
type: docs
weight: 340
url: /sv/net/aspose.words/contentdisposition/
---
## ContentDisposition enumeration

Räknar upp olika sätt att presentera dokumentet i klientens webbläsare.

```csharp
public enum ContentDisposition
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Attachment | `0` | Skicka dokumentet till webbläsaren och presentera ett alternativ för att spara dokumentet på disk eller öppna i applikationen som är kopplad till dokumentets tillägg. |
| Inline | `1` | Skicka dokumentet till webbläsaren och presenterar ett alternativ för att spara dokumentet på disk eller öppna i webbläsaren. |

### Anmärkningar

Observera att det faktiska beteendet på klientens webbläsare kan påverkas av webbläsarens säkerhetskonfiguration.

### Exempel

Visar hur man utför en sammanfogning och sedan sparar dokumentet i klientens webbläsare.

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
Assert.That(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null),
    Throws.TypeOf<ArgumentNullException>()); //Kastad eftersom HttpResponse är null i testet.

// Vi kommer att behöva stänga detta svar manuellt för att säkerställa att vi inte lägger till något överflödigt innehåll i dokumentet efter att ha sparats.
Assert.That(() => response.End(), Throws.TypeOf<NullReferenceException>());
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)


