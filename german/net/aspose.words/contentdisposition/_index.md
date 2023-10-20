---
title: ContentDisposition Enum
linktitle: ContentDisposition
articleTitle: ContentDisposition
second_title: Aspose.Words für .NET
description: Aspose.Words.ContentDisposition opsomming. Listet verschiedene Möglichkeiten zur Darstellung des Dokuments im ClientBrowser auf in C#.
type: docs
weight: 340
url: /de/net/aspose.words/contentdisposition/
---
## ContentDisposition enumeration

Listet verschiedene Möglichkeiten zur Darstellung des Dokuments im Client-Browser auf.

```csharp
public enum ContentDisposition
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Attachment | `0` | Senden Sie das Dokument an den Browser und präsentieren Sie eine Option zum Speichern des Dokuments auf der Festplatte oder zum Öffnen in der Anwendung , die mit der Erweiterung des Dokuments verknüpft ist. |
| Inline | `1` | Senden Sie das Dokument an den Browser und bieten Sie eine Option zum Speichern des Dokuments auf der Festplatte oder zum Öffnen im Browser an. |

## Bemerkungen

Beachten Sie, dass das tatsächliche Verhalten im Client-Browser durch die Sicherheitskonfiguration des Browsers beeinflusst werden kann.

## Beispiele

Zeigt, wie Sie einen Seriendruck durchführen und das Dokument anschließend im Client-Browser speichern.

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

// Das Dokument an den Client-Browser senden.
Assert.That(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null),
    Throws.TypeOf<ArgumentNullException>()); //Wird ausgelöst, weil HttpResponse im Test null ist.

// Wir müssen diese Antwort manuell schließen, um sicherzustellen, dass wir dem Dokument nach dem Speichern keinen überflüssigen Inhalt hinzufügen.
Assert.That(() => response.End(), Throws.TypeOf<NullReferenceException>());
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
