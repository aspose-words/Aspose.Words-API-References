---
title: DocumentProperty.Value
second_title: Aspose.Words für .NET-API-Referenz
description: DocumentProperty eigendom. Ruft den Wert der Eigenschaft ab oder legt ihn fest.
type: docs
weight: 50
url: /de/net/aspose.words.properties/documentproperty/value/
---
## DocumentProperty.Value property

Ruft den Wert der Eigenschaft ab oder legt ihn fest.

```csharp
public object Value { get; set; }
```

### Bemerkungen

Kann nicht Null sein.

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

* class [DocumentProperty](../)
* namensraum [Aspose.Words.Properties](../../documentproperty/)
* Montage [Aspose.Words](../../../)


