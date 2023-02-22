---
title: Document.BuiltInDocumentProperties
second_title: Aspose.Words für .NET-API-Referenz
description: Document eigendom. Gibt eine Sammlung zurück die alle integrierten Dokumenteigenschaften des Dokuments darstellt.
type: docs
weight: 40
url: /de/net/aspose.words/document/builtindocumentproperties/
---
## Document.BuiltInDocumentProperties property

Gibt eine Sammlung zurück, die alle integrierten Dokumenteigenschaften des Dokuments darstellt.

```csharp
public BuiltInDocumentProperties BuiltInDocumentProperties { get; }
```

### Beispiele

Zeigt, wie Sie mit integrierten Dokumenteigenschaften arbeiten.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// Das "Document"-Objekt enthält einige seiner Metadaten in seinen Mitgliedern.
Console.WriteLine($"Document filename:\n\t \"{doc.OriginalFileName}\"");

// Das Dokument speichert auch Metadaten in seinen eingebauten Eigenschaften.
// Jede eingebaute Eigenschaft ist ein Mitglied des "BuiltInDocumentProperties"-Objekts des Dokuments.
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

* class [BuiltInDocumentProperties](../../../aspose.words.properties/builtindocumentproperties/)
* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)


