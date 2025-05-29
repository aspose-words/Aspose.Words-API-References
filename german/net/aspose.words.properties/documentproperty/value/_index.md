---
title: DocumentProperty.Value
linktitle: Value
articleTitle: Value
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie DocumentProperty-Werte effizient verwalten können – rufen Sie Eigenschaftswerte einfach ab oder aktualisieren Sie sie für eine verbesserte Dokumentenkontrolle und Produktivität.
type: docs
weight: 50
url: /de/net/aspose.words.properties/documentproperty/value/
---
## DocumentProperty.Value property

Ruft den Wert der Eigenschaft ab oder legt ihn fest.

```csharp
public object Value { get; set; }
```

## Bemerkungen

Kann nicht sein`null`.

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

* class [DocumentProperty](../)
* namensraum [Aspose.Words.Properties](../../../aspose.words.properties/)
* Montage [Aspose.Words](../../../)
