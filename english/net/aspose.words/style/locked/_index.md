---
title: Style.Locked
linktitle: Locked
articleTitle: Locked
second_title: Aspose.Words for .NET
description: Discover the Style Locked property: control style locking for enhanced design flexibility and consistency in your projects. Unlock your creativity today!
type: docs
weight: 120
url: /net/aspose.words/style/locked/
---
## Style.Locked property

Specifies whether this style is locked.

```csharp
public bool Locked { get; set; }
```

## Examples

Shows how to lock style.

```csharp
Document doc = new Document();

Style styleHeading1 = doc.Styles[StyleIdentifier.Heading1];
if (!styleHeading1.Locked)
    styleHeading1.Locked = true;

doc.Save(ArtifactsDir + "Styles.LockStyle.docx");
```

### See Also

* class [Style](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
