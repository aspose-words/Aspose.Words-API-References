---
title: WarningInfoCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „WarningInfoCollection Count“, um für eine effiziente Datenverwaltung einfach auf die Gesamtzahl der Elemente in Ihrer Sammlung zuzugreifen.
type: docs
weight: 20
url: /de/net/aspose.words/warninginfocollection/count/
---
## WarningInfoCollection.Count property

Ruft die Anzahl der in der Sammlung enthaltenen Elemente ab.

```csharp
public int Count { get; }
```

## Beispiele

Zeigt, wie Sie Warnungen zu nicht unterstützten Formaten erhalten.

```csharp
WarningInfoCollection warnings = new WarningInfoCollection();
Document doc = new Document(MyDir + "FB2 document.fb2", new LoadOptions { WarningCallback = warnings });

Assert.AreEqual("The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warnings[0].Description);
Assert.AreEqual(1, warnings.Count);
```

### Siehe auch

* class [WarningInfoCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
