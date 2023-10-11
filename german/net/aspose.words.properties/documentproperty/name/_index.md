---
title: DocumentProperty.Name
second_title: Aspose.Words für .NET-API-Referenz
description: DocumentProperty eigendom. Gibt den Namen der Eigenschaft zurück.
type: docs
weight: 30
url: /de/net/aspose.words.properties/documentproperty/name/
---
## DocumentProperty.Name property

Gibt den Namen der Eigenschaft zurück.

```csharp
public string Name { get; }
```

### Bemerkungen

Kann nicht sein`Null` und darf keine leere Zeichenfolge sein.

### Beispiele

Zeigt, wie mit integrierten Dokumenteigenschaften gearbeitet wird.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// Das Objekt „Document“ enthält einige seiner Metadaten in seinen Mitgliedern.
Console.WriteLine($"Document filename:\n\t \"{doc.OriginalFileName}\"");

// Das Dokument speichert auch Metadaten in seinen integrierten Eigenschaften.
// Jede integrierte Eigenschaft ist Mitglied des „BuiltInDocumentProperties“-Objekts des Dokuments.
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


