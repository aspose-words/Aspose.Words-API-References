---
title: Document.Compliance
linktitle: Compliance
articleTitle: Compliance
second_title: Aspose.Words für .NET
description: Stellen Sie mühelos sicher, dass Ihre OOXML-Dokumente die Compliance-Standards erfüllen. Unser Tool analysiert Inhalte, um die OOXML-Konformität zu überprüfen und die Dokumentintegrität zu verbessern.
type: docs
weight: 70
url: /de/net/aspose.words/document/compliance/
---
## Document.Compliance property

Ruft die OOXML-Konformitätsversion ab, die aus dem geladenen Dokumentinhalt ermittelt wurde. Ist nur für OOXML-Dokumente sinnvoll.

```csharp
public OoxmlCompliance Compliance { get; }
```

## Bemerkungen

Wenn Sie ein neues leeres Dokument erstellt oder ein Nicht-OOXML-Dokument geladen haben, gibt x000d_ dasEcma376_2006 Wert.

## Beispiele

Zeigt, wie die Open Office XML-kompatible Version eines geladenen Dokuments gelesen wird.

```csharp
// Die Compliance-Version variiert zwischen Dokumenten, die mit unterschiedlichen Versionen von Microsoft Word erstellt wurden.
Document doc = new Document(MyDir + "Document.doc");
Assert.AreEqual(doc.Compliance, OoxmlCompliance.Ecma376_2006);

doc = new Document(MyDir + "Document.docx");
Assert.AreEqual(doc.Compliance, OoxmlCompliance.Iso29500_2008_Transitional);
```

### Siehe auch

* enum [OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
