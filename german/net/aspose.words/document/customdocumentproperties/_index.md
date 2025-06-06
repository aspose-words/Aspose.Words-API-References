---
title: Document.CustomDocumentProperties
linktitle: CustomDocumentProperties
articleTitle: CustomDocumentProperties
second_title: Aspose.Words für .NET
description: Erkunden Sie die Eigenschaft CustomDocumentProperties, um effizient auf alle benutzerdefinierten Dokumenteigenschaften zuzugreifen und sie zu verwalten und so die Funktionalität Ihres Dokuments zu verbessern.
type: docs
weight: 80
url: /de/net/aspose.words/document/customdocumentproperties/
---
## Document.CustomDocumentProperties property

Gibt eine Sammlung zurück, die alle benutzerdefinierten Dokumenteigenschaften des Dokuments darstellt.

```csharp
public CustomDocumentProperties CustomDocumentProperties { get; }
```

## Beispiele

Zeigt, wie mit integrierten Dokumenteigenschaften gearbeitet wird.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// Das Objekt „Dokument“ enthält einige seiner Metadaten in seinen Mitgliedern.
Console.WriteLine($"Document filename:\n\t \"{doc.OriginalFileName}\"");

// Das Dokument speichert auch Metadaten in seinen integrierten Eigenschaften.
// Jede integrierte Eigenschaft ist ein Mitglied des Objekts „BuiltInDocumentProperties“ des Dokuments.
Console.WriteLine("Built-in Properties:");
foreach (DocumentProperty docProperty in doc.BuiltInDocumentProperties)
{
    Console.WriteLine(docProperty.Name);
    Console.WriteLine($"\tType:\t{docProperty.Type}");

    // Einige Eigenschaften können mehrere Werte speichern.
    if (docProperty.Value is ICollection<object>)
    {
        foreach (object value in docProperty.Value as ICollection<object>)
            Console.WriteLine($"\tValue:\t\"{value}\"");
    }
    else
    {
        Console.WriteLine($"\tValue:\t\"{docProperty.Value}\"");
    }
}
```

### Siehe auch

* class [CustomDocumentProperties](../../../aspose.words.properties/customdocumentproperties/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
