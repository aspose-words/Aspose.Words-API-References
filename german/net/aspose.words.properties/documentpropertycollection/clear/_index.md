---
title: DocumentPropertyCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words für .NET
description: Löschen Sie mühelos alle Eigenschaften aus Ihrer DocumentPropertyCollection mit unserer Clear-Methode. Optimieren Sie noch heute Ihr Datenmanagement!
type: docs
weight: 30
url: /de/net/aspose.words.properties/documentpropertycollection/clear/
---
## DocumentPropertyCollection.Clear method

Entfernt alle Eigenschaften aus der Sammlung.

```csharp
public void Clear()
```

## Beispiele

Zeigt, wie mit den benutzerdefinierten Eigenschaften eines Dokuments gearbeitet wird.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Benutzerdefinierte Dokumenteigenschaften sind Schlüssel-Wert-Paare, die wir dem Dokument hinzufügen können.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// Die Sammlung sortiert die benutzerdefinierten Eigenschaften in alphabetischer Reihenfolge.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// Jede benutzerdefinierte Eigenschaft im Dokument drucken.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Zeigen Sie den Wert einer benutzerdefinierten Eigenschaft mithilfe eines DOCPROPERTY-Felds an.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// Diese benutzerdefinierten Eigenschaften finden wir in Microsoft Word über „Datei“ -> „Eigenschaften“ > „Erweiterte Eigenschaften“ > „Benutzerdefiniert“.
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Unten sind drei Möglichkeiten zum Entfernen benutzerdefinierter Eigenschaften aus einem Dokument aufgeführt.
// 1 - Entfernen nach Index:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - Nach Namen entfernen:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - Die gesamte Sammlung auf einmal leeren:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Siehe auch

* class [DocumentPropertyCollection](../)
* namensraum [Aspose.Words.Properties](../../../aspose.words.properties/)
* Montage [Aspose.Words](../../../)
