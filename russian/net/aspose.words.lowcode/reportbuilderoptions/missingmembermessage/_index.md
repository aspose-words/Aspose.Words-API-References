---
title: ReportBuilderOptions.MissingMemberMessage
linktitle: MissingMemberMessage
articleTitle: MissingMemberMessage
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ReportBuilderOptions MissingMemberMessage. Легко настраивайте сообщения для отсутствующих ссылок на объекты, улучшая пользовательский опыт без особых усилий.
type: docs
weight: 30
url: /ru/net/aspose.words.lowcode/reportbuilderoptions/missingmembermessage/
---
## ReportBuilderOptions.MissingMemberMessage property

Возвращает или задает строковое значение, напечатанное вместо шаблонного выражения, представляющего простую ссылку на отсутствующий член объекта. Значение по умолчанию — пустая строка.

```csharp
public string MissingMemberMessage { get; set; }
```

## Примечания

Свойство должно использоваться совместно сAllowMissingMembers option. В противном случае, исключение выдается при обнаружении отсутствующего члена объекта.

Свойство влияет только на печать шаблонного выражения, представляющего простую ссылку на член объекта missing . Например, печать бинарного оператора, один из операндов которого ссылается на член объекта missing , не влияет.

Значение этого свойства не может быть установлено равным null.

### Смотрите также

* class [ReportBuilderOptions](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)
