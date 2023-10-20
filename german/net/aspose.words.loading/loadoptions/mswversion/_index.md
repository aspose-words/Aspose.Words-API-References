---
title: LoadOptions.MswVersion
linktitle: MswVersion
articleTitle: MswVersion
second_title: Aspose.Words für .NET
description: LoadOptions MswVersion eigendom. Ermöglicht die Angabe dass der Dokumentladevorgang mit einer bestimmten MS WordVersion übereinstimmen soll. Der Standardwert istWord2019 in C#.
type: docs
weight: 100
url: /de/net/aspose.words.loading/loadoptions/mswversion/
---
## LoadOptions.MswVersion property

Ermöglicht die Angabe, dass der Dokumentladevorgang mit einer bestimmten MS Word-Version übereinstimmen soll. Der Standardwert istWord2019

```csharp
public MsWordVersion MswVersion { get; set; }
```

## Bemerkungen

Unterschiedliche Word-Versionen behandeln möglicherweise bestimmte Aspekte des Dokumentinhalts und der Formatierung während des Ladevorgangs geringfügig unterschiedlich , was zu geringfügigen Unterschieden im Dokumentobjektmodell führen kann.

## Beispiele

Zeigt, wie der Ladevorgang einer bestimmten Microsoft Word-Version beim Laden eines Dokuments emuliert wird.

```csharp
// Standardmäßig lädt Aspose.Words Dokumente gemäß der Microsoft Word 2019-Spezifikation.
LoadOptions loadOptions = new LoadOptions();

Assert.AreEqual(MsWordVersion.Word2019, loadOptions.MswVersion);

// In diesem Dokument fehlt der standardmäßige Absatzformatierungsstil.
// Dieser Standardstil wird neu generiert, wenn wir das Dokument entweder mit Microsoft Word oder Aspose.Words laden.
loadOptions.MswVersion = MsWordVersion.Word2007;
Document doc = new Document(MyDir + "Document.docx", loadOptions);

// Der Zeilenabstand des Stils hat diesen Wert, wenn er von der Microsoft Word 2007-Spezifikation geladen wird.
Assert.AreEqual(12.95d, doc.Styles.DefaultParagraphFormat.LineSpacing, 0.01d);
```

### Siehe auch

* enum [MsWordVersion](../../../aspose.words.settings/mswordversion/)
* class [LoadOptions](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
