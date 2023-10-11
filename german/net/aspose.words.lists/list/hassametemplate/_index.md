---
title: List.HasSameTemplate
second_title: Aspose.Words für .NET-API-Referenz
description: List methode. Gibt true zurück wenn die aktuelle Liste und die angegebene Liste aus derselben Vorlage erstellt werden.
type: docs
weight: 120
url: /de/net/aspose.words.lists/list/hassametemplate/
---
## List.HasSameTemplate method

Gibt „true“ zurück, wenn die aktuelle Liste und die angegebene Liste aus derselben Vorlage erstellt werden.

```csharp
public bool HasSameTemplate(List other)
```

### Beispiele

Zeigt, wie Listen mit derselben ListDefId definiert werden.

```csharp
Document doc = new Document(MyDir + "Different lists.docx");

Assert.True(doc.Lists[0].HasSameTemplate(doc.Lists[1]));
Assert.False(doc.Lists[1].HasSameTemplate(doc.Lists[2]));
```

### Siehe auch

* class [List](../)
* namensraum [Aspose.Words.Lists](../../list/)
* Montage [Aspose.Words](../../../)


