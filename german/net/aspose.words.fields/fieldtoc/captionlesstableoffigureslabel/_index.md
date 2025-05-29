---
title: FieldToc.CaptionlessTableOfFiguresLabel
linktitle: CaptionlessTableOfFiguresLabel
articleTitle: CaptionlessTableOfFiguresLabel
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „FieldToc CaptionlessTableOfFiguresLabel“, um Ihr Abbildungsverzeichnis anzupassen. Verwalten Sie Sequenzkennungen ganz einfach ohne Beschriftungen!
type: docs
weight: 30
url: /de/net/aspose.words.fields/fieldtoc/captionlesstableoffigureslabel/
---
## FieldToc.CaptionlessTableOfFiguresLabel property

Ruft den Namen der Sequenzkennung ab oder legt ihn fest, die beim Erstellen eines Abbildungsverzeichnisses verwendet wird, das weder Beschriftung noch Nummer der Bildunterschrift enthält.

```csharp
public string CaptionlessTableOfFiguresLabel { get; set; }
```

## Beispiele

Zeigt, wie der Name der Sequenzkennung festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);
fieldToc.CaptionlessTableOfFiguresLabel = "Test";

Assert.AreEqual(" TOC  \\a Test", fieldToc.GetFieldCode());
```

### Siehe auch

* class [FieldToc](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
