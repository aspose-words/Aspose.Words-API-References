---
title: ReportingEngine.MissingMemberMessage
linktitle: MissingMemberMessage
articleTitle: MissingMemberMessage
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ReportingEngine MissingMemberMessage, настройте сообщения для отсутствующих членов объекта с легкостью. Улучшите пользовательский опыт без усилий!
type: docs
weight: 30
url: /ru/net/aspose.words.reporting/reportingengine/missingmembermessage/
---
## ReportingEngine.MissingMemberMessage property

Возвращает или задает строковое значение, напечатанное вместо шаблонного выражения, представляющего простую ссылку на отсутствующий член объекта. Значение по умолчанию — пустая строка.

```csharp
public string MissingMemberMessage { get; set; }
```

## Примечания

Свойство должно использоваться совместно сAllowMissingMembers option. В противном случае, исключение выдается при обнаружении отсутствующего члена объекта.

Свойство влияет только на печать шаблонного выражения, представляющего простую ссылку на член объекта missing . Например, печать бинарного оператора, один из операндов которого ссылается на член объекта missing , не влияет.

Значение этого свойства не может быть установлено равным null.

## Примеры

Показывает, как разрешить отсутствующих участников.

```csharp
DocumentBuilder builder = new DocumentBuilder();
builder.Writeln("<<[missingObject.First().id]>>");
builder.Writeln("<<foreach [in missingObject]>><<[id]>><</foreach>>");

ReportingEngine engine = new ReportingEngine { Options = ReportBuildOptions.AllowMissingMembers };
engine.MissingMemberMessage = "Missed";
engine.BuildReport(builder.Document, new DataSet(), "");
```

### Смотрите также

* class [ReportingEngine](../)
* пространство имен [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* сборка [Aspose.Words](../../../)
