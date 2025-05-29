---
title: BuiltInDocumentProperties.HyperlinkBase
linktitle: HyperlinkBase
articleTitle: HyperlinkBase
second_title: Aspose.Words для .NET
description: Откройте для себя свойство BuiltInDocumentProperties HyperlinkBase, позволяющее оптимизировать относительные гиперссылки в документах для бесперебойной навигации и улучшения пользовательского опыта.
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

// Вставить относительную гиперссылку на документ в локальной файловой системе с именем «Document.docx».
// При нажатии на ссылку в Microsoft Word откроется указанный документ, если он доступен.
builder.InsertHyperlink("Relative hyperlink", "Document.docx", false);

// Эта ссылка относительная. Если в той же папке нет "Document.docx"
// так как документ содержит эту ссылку, ссылка будет недействительной.
Assert.False(File.Exists(ArtifactsDir + "Document.docx"));
doc.Save(ArtifactsDir + "DocumentProperties.HyperlinkBase.BrokenLink.docx");

// Документ, на который мы пытаемся создать ссылку, находится в другом каталоге, нежели тот, в котором мы планируем сохранить документ.
 // Мы могли бы исправить такие ссылки, указав в каждой из них абсолютное имя файла.
// В качестве альтернативы мы могли бы предоставить базовую ссылку, которая будет соответствовать каждой гиперссылке с относительным именем файла
 // будет добавлен к ссылке, когда мы нажмем на нее.
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;
properties.HyperlinkBase = MyDir;

Assert.True(File.Exists(properties.HyperlinkBase + ((FieldHyperlink)doc.Range.Fields[0]).Address));

doc.Save(ArtifactsDir + "DocumentProperties.HyperlinkBase.WorkingLink.docx");
```

### Смотрите также

* class [BuiltInDocumentProperties](../)
* пространство имен [Aspose.Words.Properties](../../../aspose.words.properties/)
* сборка [Aspose.Words](../../../)
