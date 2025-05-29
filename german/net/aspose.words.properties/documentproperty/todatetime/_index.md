---
title: DocumentProperty.ToDateTime
linktitle: ToDateTime
articleTitle: ToDateTime
second_title: Aspose.Words für .NET
description: Konvertieren Sie DocumentProperty mühelos in UTC DateTime. Greifen Sie auf genaue Zeitstempel zu und verbessern Sie Ihr Datenmanagement mit unserer zuverlässigen Methode.
type: docs
weight: 80
url: /de/net/aspose.words.properties/documentproperty/todatetime/
---
## DocumentProperty.ToDateTime method

Gibt den Eigenschaftswert zurück als**Datum/Uhrzeit** in UTC.

```csharp
public DateTime ToDateTime()
```

## Bemerkungen

Löst eine Ausnahme aus, wenn der Eigenschaftstyp nichtDateTime.

Microsoft Word speichert für benutzerdefinierte Datumseigenschaften nur den Datumsteil (keine Uhrzeit).

## Beispiele

Zeigt, wie eine benutzerdefinierte Dokumenteigenschaft erstellt wird, die ein Datum und eine Uhrzeit enthält.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);
DateTime authorizationDate = doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime();
Console.WriteLine($"Document authorized on {authorizationDate}");
```

Zeigt verschiedene Methoden zur Typkonvertierung benutzerdefinierter Dokumenteigenschaften.

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

### Siehe auch

* class [DocumentProperty](../)
* namensraum [Aspose.Words.Properties](../../../aspose.words.properties/)
* Montage [Aspose.Words](../../../)
