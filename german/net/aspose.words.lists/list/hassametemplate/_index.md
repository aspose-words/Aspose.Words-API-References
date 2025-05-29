---
title: List.HasSameTemplate
linktitle: HasSameTemplate
articleTitle: HasSameTemplate
second_title: Aspose.Words für .NET
description: Entdecken Sie die HasSameTemplate-Methode, überprüfen Sie einfach, ob zwei Listen dieselbe Vorlage verwenden, und sorgen Sie so für Konsistenz und Effizienz in Ihrem Datenmanagement.
type: docs
weight: 120
url: /de/net/aspose.words.lists/list/hassametemplate/
---
## List.HasSameTemplate method

Gibt „true“ zurück, wenn die aktuelle Liste und die angegebene Liste aus derselben Vorlage erstellt wurden.

```csharp
public bool HasSameTemplate(List other)
```

## Beispiele

Zeigt, wie Listen mit derselben ListDefId definiert werden.

```csharp
Document doc = new Document(MyDir + "Different lists.docx");

Assert.True(doc.Lists[0].HasSameTemplate(doc.Lists[1]));
Assert.False(doc.Lists[1].HasSameTemplate(doc.Lists[2]));
```

### Siehe auch

* class [List](../)
* namensraum [Aspose.Words.Lists](../../../aspose.words.lists/)
* Montage [Aspose.Words](../../../)
