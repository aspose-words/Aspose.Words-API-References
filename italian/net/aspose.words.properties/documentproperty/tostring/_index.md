---
title: DocumentProperty.ToString
second_title: Aspose.Words per .NET API Reference
description: DocumentProperty metodo. Restituisce il valore della proprietà come una stringa formattata in base alle impostazioni internazionali correnti.
type: docs
weight: 110
url: /it/net/aspose.words.properties/documentproperty/tostring/
---
## DocumentProperty.ToString method

Restituisce il valore della proprietà come una stringa formattata in base alle impostazioni internazionali correnti.

```csharp
public override string ToString()
```

### Osservazioni

Converte una proprietà booleana in "Y" o "N". Converte una proprietà di data in una stringa di data breve. Per tutti gli altri tipi converte una proprietà utilizzando Object.ToString().

### Esempi

Mostra vari metodi di conversione del tipo delle proprietà personalizzate del documento.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

DateTime authDate = DateTime.Today;
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", authDate);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

Assert.AreEqual(true, properties["Authorized"].ToBool());
Assert.AreEqual("John Doe", properties["Authorized By"].ToString());
Assert.AreEqual(authDate, properties["Authorized Date"].ToDateTime());
Assert.AreEqual(1, properties["Authorized Revision"].ToInt());
Assert.AreEqual(123.45d, properties["Authorized Amount"].ToDouble());
```

Mostra come lavorare con le proprietà personalizzate del documento.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// Ogni documento contiene una raccolta di proprietà personalizzate che, come le proprietà integrate, sono coppie chiave-valore.
 // Il documento ha un elenco fisso di proprietà integrate. L'utente crea tutte le proprietà personalizzate.
Assert.AreEqual("Value of custom document property", doc.CustomDocumentProperties["CustomProperty"].ToString());

doc.CustomDocumentProperties.Add("CustomProperty2", "Value of custom document property #2");

Console.WriteLine("Custom Properties:");
foreach (var customDocumentProperty in doc.CustomDocumentProperties)
{
    Console.WriteLine(customDocumentProperty.Name);
    Console.WriteLine($"\tType:\t{customDocumentProperty.Type}");
    Console.WriteLine($"\tValue:\t\"{customDocumentProperty.Value}\"");
}
```

### Guarda anche

* class [DocumentProperty](../)
* spazio dei nomi [Aspose.Words.Properties](../../documentproperty/)
* assemblea [Aspose.Words](../../../)


