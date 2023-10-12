---
title: Document.ShadeFormData
second_title: Aspose.Words für .NET-API-Referenz
description: Document eigendom. Gibt an ob die Grauschattierung auf Formularfeldern aktiviert werden soll.
type: docs
weight: 380
url: /de/net/aspose.words/document/shadeformdata/
---
## Document.ShadeFormData property

Gibt an, ob die Grauschattierung auf Formularfeldern aktiviert werden soll.

```csharp
public bool ShadeFormData { get; set; }
```

### Beispiele

Zeigt, wie Grauschattierungen auf Formularfelder angewendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world! ");
builder.InsertTextInput("My form field", TextFormFieldType.Regular, "",
    "Text contents of form field, which are shaded in grey by default.", 0);

// Wir können die Grauschattierung deaktivieren, sodass der mit einem Lesezeichen versehene Text mit dem anderen Text verschmilzt.
doc.ShadeFormData = useGreyShading;
doc.Save(ArtifactsDir + "Document.ShadeFormData.docx");
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)


