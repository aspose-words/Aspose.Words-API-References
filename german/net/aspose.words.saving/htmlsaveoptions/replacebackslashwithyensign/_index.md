---
title: HtmlSaveOptions.ReplaceBackslashWithYenSign
linktitle: ReplaceBackslashWithYenSign
articleTitle: ReplaceBackslashWithYenSign
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „HtmlSaveOptions ReplaceBackslashWithYenSign“ Ihre HTML-Ausgabe verbessert, indem sie Backslashes in Yen-Zeichen umwandelt. Standardmäßig „false“.
type: docs
weight: 420
url: /de/net/aspose.words.saving/htmlsaveoptions/replacebackslashwithyensign/
---
## HtmlSaveOptions.ReplaceBackslashWithYenSign property

Gibt an, ob Backslash-Zeichen durch Yen-Zeichen ersetzt werden sollen. Der Standardwert ist`FALSCH` .

```csharp
public bool ReplaceBackslashWithYenSign { get; set; }
```

## Bemerkungen

Standardmäßig ahmt Aspose.Words das Verhalten von MS Word nach und ersetzt Backslash-Zeichen in generierten HTML-Dokumenten nicht durch Yen-Zeichen. Frühere Versionen von Aspose.Words führten jedoch in bestimmten Szenarien solche Ersetzungen durch. Dieses Flag ermöglicht die Abwärtskompatibilität mit früheren Versionen von Aspose.Words.

## Beispiele

Zeigt, wie Backslash-Zeichen durch Yen-Zeichen ersetzt werden (HTML).

```csharp
Document doc = new Document(MyDir + "Korean backslash symbol.docx");

// Standardmäßig ahmt Aspose.Words das Verhalten von MS Word nach und ersetzt Backslash-Zeichen nicht durch Yen-Zeichen in
// generierte HTML-Dokumente. Frühere Versionen von Aspose.Words führten solche Ersetzungen jedoch in bestimmten
// Szenarien. Dieses Flag ermöglicht die Abwärtskompatibilität mit früheren Versionen von Aspose.Words.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.ReplaceBackslashWithYenSign = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.ReplaceBackslashWithYenSign.html", saveOptions);
```

### Siehe auch

* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
