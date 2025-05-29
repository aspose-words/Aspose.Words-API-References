---
title: NumSpacing Enum
linktitle: NumSpacing
articleTitle: NumSpacing
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.NumSpacing, um den Ziffernabstand für eine verbesserte Dokumentformatierung anzupassen. Verbessern Sie noch heute Ihre Textpräsentation!
type: docs
weight: 5030
url: /de/net/aspose.words/numspacing/
---
## NumSpacing enumeration

Gibt mögliche Werte an, in denen Ziffernabstände angezeigt werden können.

```csharp
public enum NumSpacing
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Default | `0` | Gibt an, dass Ziffern in der Standardform der Schriftart angezeigt werden. |
| Proportional | `1` | Gibt an, dass die als proportional angeordnete Ziffern gestalteten Formen angezeigt werden, sofern dies von der Schriftart unterstützt wird. |
| Tabular | `2` | Gibt an, dass die als tabellarische Zahlen konzipierten Formen angezeigt werden, sofern dies von der Schriftart unterstützt wird. |

## Beispiele

Zeigt, wie der Abstandstyp der Ziffer eingestellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Dieser Effekt wird nur in neueren Versionen von MS Word unterstützt.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2019);

builder.Write("1 ");
builder.Write("This is an example");

Run run = doc.FirstSection.Body.FirstParagraph.Runs[0];
if (run.Font.NumberSpacing == NumSpacing.Default)
    run.Font.NumberSpacing = NumSpacing.Proportional;

doc.Save(ArtifactsDir + "Fonts.NumberSpacing.docx");
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
