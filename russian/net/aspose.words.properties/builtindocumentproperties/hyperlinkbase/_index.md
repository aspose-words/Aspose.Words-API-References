---
title: BuiltInDocumentProperties.HyperlinkBase
linktitle: HyperlinkBase
articleTitle: HyperlinkBase
second_title: Aspose.Words для .NET
description: BuiltInDocumentProperties HyperlinkBase свойство. Указывает базовую строку используемую для оценки относительных гиперссылок в этом документе на С#.
type: docs
weight: 120
url: /ru/net/aspose.words.properties/builtindocumentproperties/hyperlinkbase/
---
## BuiltInDocumentProperties.HyperlinkBase property

Указывает базовую строку, используемую для оценки относительных гиперссылок в этом документе.

```csharp
public string HyperlinkBase { get; set; }
```

## Примечания

Aspose.Words не использует это свойство.

## Примеры

Показывает, как сохранить базовую часть гиперссылки в свойствах документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем относительную гиперссылку на документ в локальной файловой системе с именем «Document.docx».
// При нажатии на ссылку в Microsoft Word откроется указанный документ, если он доступен.
builder.InsertHyperlink("Relative hyperlink", "Document.docx", false);

// Эта ссылка является относительной. Если в той же папке нет «Document.docx»
// поскольку документ содержит эту ссылку, ссылка будет разорвана.
Assert.False(File.Exists(ArtifactsDir + "Document.docx"));
doc.Save(ArtifactsDir + "DocumentProperties.HyperlinkBase.BrokenLink.docx");

// Документ, на который мы пытаемся создать ссылку, находится в другом каталоге, чем тот, в котором мы планируем сохранить документ.
 // Мы могли бы исправить подобные ссылки, поместив в каждую из них абсолютное имя файла.
// В качестве альтернативы мы могли бы предоставить базовую ссылку, в которой каждая гиперссылка с относительным именем файла
 // будет добавлено к ссылке, когда мы нажмем на нее.
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;
properties.HyperlinkBase = MyDir;

Assert.True(File.Exists(properties.HyperlinkBase + ((FieldHyperlink)doc.Range.Fields[0]).Address));

doc.Save(ArtifactsDir + "DocumentProperties.HyperlinkBase.WorkingLink.docx");
```

### Смотрите также

* class [BuiltInDocumentProperties](../)
* пространство имен [Aspose.Words.Properties](../../../aspose.words.properties/)
* сборка [Aspose.Words](../../../)
