---
title: Enum ContentDisposition
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.ContentDisposition enum. Enumerates different ways of presenting the document at the client browser in C#.
type: docs
weight: 330
url: /net/aspose.words/contentdisposition/
---
## ContentDisposition enumeration

Enumerates different ways of presenting the document at the client browser.

```csharp
public enum ContentDisposition
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Attachment | `0` | Send the document to the browser and present an option to save the document to disk or open in the application associated with the document's extension. |
| Inline | `1` | Send the document to the browser and presents an option to save the document to disk or open inside the browser. |

## Remarks

Note that the actual behavior on the client browser might be affected by security configuration of the browser.

## Examples

Shows how to perform a mail merge, and then save the document to the client browser.

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

// Send the document to the client browser.
Assert.That(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null),
    Throws.TypeOf<ArgumentNullException>()); //Thrown because HttpResponse is null in the test.

// We will need to close this response manually to ensure that we do not add any superfluous content to the document after saving.
Assert.That(() => response.End(), Throws.TypeOf<NullReferenceException>());
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
