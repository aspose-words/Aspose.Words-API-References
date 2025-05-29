---
title: Document.ShadeFormData
linktitle: ShadeFormData
articleTitle: ShadeFormData
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie mit der ShadeFormData-Eigenschaft die Sichtbarkeit von Formularen durch Grauschattierungen verbessern und so die Benutzererfahrung und Zugänglichkeit verbessern.
type: docs
weight: 400
url: /de/net/aspose.words/document/shadeformdata/
---
## Document.ShadeFormData property

Gibt an, ob die graue Schattierung für Formularfelder aktiviert werden soll.

```csharp
public bool ShadeFormData { get; set; }
```

## Beispiele

Zeigt, wie Formularfelder grau schattiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world! ");
builder.InsertTextInput("My form field", TextFormFieldType.Regular, "",
    "Text contents of form field, which are shaded in grey by default.", 0);

// Wir können die graue Schattierung ausschalten, sodass der mit einem Lesezeichen versehene Text mit dem anderen Text verschmilzt.
doc.ShadeFormData = useGreyShading;
doc.Save(ArtifactsDir + "Document.ShadeFormData.docx");
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
