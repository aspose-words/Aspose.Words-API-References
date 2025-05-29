---
title: Style.Locked
linktitle: Locked
articleTitle: Locked
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „Stil gesperrt“ und steuern Sie die Stilsperre für mehr Designflexibilität und Konsistenz in Ihren Projekten. Entfesseln Sie noch heute Ihre Kreativität!
type: docs
weight: 120
url: /de/net/aspose.words/style/locked/
---
## Style.Locked property

Gibt an, ob dieser Stil gesperrt ist.

```csharp
public bool Locked { get; set; }
```

## Beispiele

Zeigt, wie der Stil gesperrt wird.

```csharp
Document doc = new Document();

Style styleHeading1 = doc.Styles[StyleIdentifier.Heading1];
if (!styleHeading1.Locked)
    styleHeading1.Locked = true;

doc.Save(ArtifactsDir + "Styles.LockStyle.docx");
```

### Siehe auch

* class [Style](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
