---
title: XmlDataSource Class
linktitle: XmlDataSource
articleTitle: XmlDataSource
second_title: Aspose.Words для .NET
description: Откройте для себя мощные отчеты с Aspose.Words.XmlDataSource. Простой доступ к данным XML для бесшовной интеграции в ваши отчеты и улучшения визуализации данных.
type: docs
weight: 5490
url: /ru/net/aspose.words.reporting/xmldatasource/
---
## XmlDataSource class

Предоставляет доступ к данным XML-файла или потока для использования в отчете.

Чтобы узнать больше, посетите[Механизм отчетов LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) документальная статья.

```csharp
public class XmlDataSource
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [XmlDataSource](xmldatasource/#constructor)(*Stream*) | Создает новый источник данных с данными из потока XML, используя параметры по умолчанию для загрузки данных XML. |
| [XmlDataSource](xmldatasource/#constructor_4)(*string*) | Создает новый источник данных с данными из XML-файла, используя параметры по умолчанию для загрузки XML-данных. |
| [XmlDataSource](xmldatasource/#constructor_2)(*Stream, Stream*) | Создает новый источник данных с данными из потока XML, используя поток определения схемы XML. Параметры по умолчанию используются для загрузки данных XML. |
| [XmlDataSource](xmldatasource/#constructor_1)(*Stream, [XmlDataLoadOptions](../xmldataloadoptions/)*) | Создает новый источник данных с данными из потока XML, используя указанные параметры загрузки данных XML. |
| [XmlDataSource](xmldatasource/#constructor_6)(*string, string*) | Создает новый источник данных с данными из XML-файла, используя файл определения схемы XML. Параметры по умолчанию используются для загрузки XML-данных. |
| [XmlDataSource](xmldatasource/#constructor_5)(*string, [XmlDataLoadOptions](../xmldataloadoptions/)*) | Создает новый источник данных с данными из XML-файла, используя указанные параметры загрузки XML-данных. |
| [XmlDataSource](xmldatasource/#constructor_3)(*Stream, Stream, [XmlDataLoadOptions](../xmldataloadoptions/)*) | Создает новый источник данных с данными из потока XML, используя поток определения схемы XML. Указанные параметры используются для загрузки данных XML. |
| [XmlDataSource](xmldatasource/#constructor_7)(*string, string, [XmlDataLoadOptions](../xmldataloadoptions/)*) | Создает новый источник данных с данными из XML-файла, используя файл определения схемы XML. Указанные параметры используются для загрузки XML-данных. |

## Примечания

Чтобы получить доступ к данным соответствующего файла или потока при формировании отчета, передайте экземпляр этого класса как источник данных одному из[`ReportingEngine`](../reportingengine/) .BuildReport перегрузки.

В шаблонных документах, если элемент XML верхнего уровня содержит только список элементов одного типа, `XmlDataSource` экземпляр следует обрабатывать так же, как если бы это был DataTable экземпляр. В противном случае,`XmlDataSource` экземпляр следует обрабатывать так же, как если бы это был DataRow Экземпляр . Для получения дополнительной информации см. справочник по синтаксису шаблонов (https://docs.aspose.com/display/wordsnet/Template+Syntax).

Когда XML Schema Definition передается конструктору этого класса, типы данных значений простых XML-элементов и атрибутов определяются в соответствии со схемой. Таким образом, в шаблонных документах можно работать с типизированными значениями , а не только со строками.

Когда XML Schema Definition не передается конструктору этого класса, типы данных значений простых XML-элементов и атрибутов определяются автоматически по их строковым представлениям. Таким образом, в шаблонных документах вы можете работать с типизированными значениями и в этом случае. Движок способен автоматически распознавать значения следующих типов:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Обратите внимание, что для работы автоматического распознавания типов данных строковые представления значений простых XML-элементов и атрибутов должны быть сформированы с использованием инвариантных настроек культуры.

Чтобы переопределить поведение по умолчанию при загрузке XML-данных, инициализируйте и передайте[`XmlDataLoadOptions`](../xmldataloadoptions/) Экземпляр в конструктор этого класса.

## Примеры

Покажите, как использовать XML в качестве источника данных (строки).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

XmlDataSource dataSource = new XmlDataSource(MyDir + "List of people.xml");
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataString.docx");
```

Покажите, как использовать XML в качестве источника данных (потока).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

using (FileStream stream = File.OpenRead(MyDir + "List of people.xml"))
{
    XmlDataSource dataSource = new XmlDataSource(stream);
    BuildReport(doc, dataSource, "persons");
}

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataStream.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Reporting](../../aspose.words.reporting/)
* сборка [Aspose.Words](../../)
