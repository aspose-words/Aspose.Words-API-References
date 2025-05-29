---
title: XamlFlowSaveOptions.ReplaceBackslashWithYenSign
linktitle: ReplaceBackslashWithYenSign
articleTitle: ReplaceBackslashWithYenSign
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die ReplaceBackslashWithYenSign-Eigenschaft von XamlFlowSaveOptions Ihre Datenformatierung verbessert, indem sie Backslashes in Yen-Zeichen umwandelt. Standardmäßig „false“.
type: docs
weight: 50
url: /de/net/aspose.words.saving/xamlflowsaveoptions/replacebackslashwithyensign/
---
## XamlFlowSaveOptions.ReplaceBackslashWithYenSign property

Gibt an, ob Backslash-Zeichen durch Yen-Zeichen ersetzt werden sollen. Der Standardwert ist`FALSCH` .

```csharp
public bool ReplaceBackslashWithYenSign { get; set; }
```

## Bemerkungen

Standardmäßig ahmt Aspose.Words das Verhalten von MS Word nach und ersetzt Backslash-Zeichen in generierten XAML-Dokumenten nicht durch Yen-Zeichen. Frühere Versionen von Aspose.Words führten jedoch in bestimmten Szenarien solche Ersetzungen durch. Dieses Flag ermöglicht die Abwärtskompatibilität mit früheren Versionen von Aspose.Words.

## Beispiele

Zeigt, wie Backslash-Zeichen durch Yen-Zeichen ersetzt werden (XAML).

```csharp
Document doc = new Document(MyDir + "Korean backslash symbol.docx");

// Standardmäßig ahmt Aspose.Words das Verhalten von MS Word nach und ersetzt Backslash-Zeichen nicht durch Yen-Zeichen in
// generierte HTML-Dokumente. Frühere Versionen von Aspose.Words führten solche Ersetzungen jedoch in bestimmten
// Szenarien. Dieses Flag ermöglicht die Abwärtskompatibilität mit früheren Versionen von Aspose.Words.
XamlFlowSaveOptions saveOptions = new XamlFlowSaveOptions();
saveOptions.ReplaceBackslashWithYenSign = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.ReplaceBackslashWithYenSign.xaml", saveOptions);
```

### Siehe auch

* class [XamlFlowSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
