---
title: ContentDisposition Enum
linktitle: ContentDisposition
articleTitle: ContentDisposition
second_title: Aspose.Words für .NET
description: Erkunden Sie die Aufzählung Aspose.Words.ContentDisposition, um verschiedene Dokumentpräsentationsoptionen für ein verbessertes Client-Browser-Erlebnis zu entdecken.
type: docs
weight: 540
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
| Attachment | `0` | Senden Sie das Dokument an den Browser und zeigen Sie eine Option zum Speichern des Dokuments auf der Festplatte oder zum Öffnen in der Anwendung an, die der Erweiterung des Dokuments zugeordnet ist. |
| Inline | `1` | Sendet das Dokument an den Browser und zeigt eine Option zum Speichern des Dokuments auf der Festplatte oder zum Öffnen im Browser an. |

## Bemerkungen

Beachten Sie, dass das tatsächliche Verhalten im Client-Browser durch die Sicherheitskonfiguration des Browsers beeinflusst werden kann.

## Beispiele

Zeigt, wie Sie einen Serienbrief erstellen und das Dokument anschließend im Client-Browser speichern.

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

// Senden Sie das Dokument an den Client-Browser.
//Ausgelöst, weil HttpResponse im Test null ist.
Assert.Throws<ArgumentNullException>(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null));

// Wir müssen diese Antwort manuell schließen, um sicherzustellen, dass wir dem Dokument nach dem Speichern keinen überflüssigen Inhalt hinzufügen.
Assert.Throws<NullReferenceException>(() => response.End());
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
