---
title: LoadOptions.MswVersion
linktitle: MswVersion
articleTitle: MswVersion
second_title: Aspose.Words für .NET
description: Optimieren Sie das Laden von Dokumenten mit LoadOptions MswVersion. Stellen Sie die Kompatibilität mit bestimmten MS Word-Versionen sicher. Für eine nahtlose Integration wird standardmäßig Word 2019 verwendet.
type: docs
weight: 100
url: /de/net/aspose.words.loading/loadoptions/mswversion/
---
## LoadOptions.MswVersion property

Ermöglicht die Angabe, dass der Dokumentladevorgang einer bestimmten MS Word-Version entsprechen soll. Der Standardwert istWord2019

```csharp
public MsWordVersion MswVersion { get; set; }
```

## Bemerkungen

Verschiedene Word-Versionen verarbeiten bestimmte Aspekte des Dokumentinhalts und der Formatierung während des Ladevorgangs möglicherweise leicht unterschiedlich , was zu geringfügigen Unterschieden im Dokumentobjektmodell führen kann.

## Beispiele

Zeigt, wie der Ladevorgang einer bestimmten Microsoft Word-Version beim Laden von Dokumenten emuliert wird.

```csharp
// Standardmäßig lädt Aspose.Words Dokumente gemäß der Microsoft Word 2019-Spezifikation.
LoadOptions loadOptions = new LoadOptions();

Assert.AreEqual(MsWordVersion.Word2019, loadOptions.MswVersion);

// In diesem Dokument fehlt der Standard-Absatzformatierungsstil.
// Dieser Standardstil wird neu generiert, wenn wir das Dokument entweder mit Microsoft Word oder Aspose.Words laden.
loadOptions.MswVersion = MsWordVersion.Word2007;
Document doc = new Document(MyDir + "Document.docx", loadOptions);

// Der Zeilenabstand des Stils hat diesen Wert, wenn er gemäß der Microsoft Word 2007-Spezifikation geladen wird.
Assert.AreEqual(12.95d, doc.Styles.DefaultParagraphFormat.LineSpacing, 0.01d);
```

### Siehe auch

* enum [MsWordVersion](../../../aspose.words.settings/mswordversion/)
* class [LoadOptions](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
