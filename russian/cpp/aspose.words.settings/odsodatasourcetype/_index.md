---
title: "Aspose::Words::Settings::OdsoDataSourceType enum"
linktitle: "OdsoDataSourceType"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Settings::OdsoDataSourceType enum. Указывает тип внешнего источника данных, к которому следует подключиться в рамках информации о соединении ODSO в C++."
type: docs
weight: 19000
url: /ru/cpp/aspose.words.settings/odsodatasourcetype/
---
## OdsoDataSourceType enum


Указывает тип внешнего источника данных, к которому следует подключиться в рамках информации о соединении ODSO.

```cpp
enum class OdsoDataSourceType
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Text | 0 | Указывает, что данный документ был подключён к текстовому файлу. Возможно wdMergeSubTypeOther. |
| Database | 1 | Указывает, что данный документ был подключён к базе данных. Возможно wdMergeSubTypeAccess. |
| AddressBook | 2 | Указывает, что данный документ был подключен к адресной книге контактов. Возможно wdMergeSubTypeOAL. |
| Document1 | 3 | Указывает, что данный документ был подключен к другому формату документа, поддерживаемому приложением‑производителем. Возможно wdMergeSubTypeOLEDBWord. |
| Document2 | 4 | Указывает, что данный документ был подключен к другому формату документа, поддерживаемому приложением‑производителем. Возможно wdMergeSubTypeWorks. |
| Native | 5 | Указывает, что данный документ был подключен к другому формату документа, родному приложению‑производителю. Возможно wdMergeSubTypeOLEDBText. |
| Email | 6 | Указывает, что данный документ был подключен к почтовому приложению. Возможно wdMergeSubTypeOutlook. |
| None | 7 | Тип внешнего источника данных не указан. Возможно wdMergeSubTypeWord. |
| Legacy | 8 | Указывает, что данный документ был подключен к устаревшему формату документа, поддерживаемому приложением‑производителем. Возможно wdMergeSubTypeWord2000. |
| Master | 9 | Указывает, что данный документ был подключен к источнику данных, который агрегирует другие источники данных. |
| Default | n/a | Равно [None](./). |

## Примечания


Спецификация OOXML очень расплывчата для этого перечисления. Полагаю, оно может соответствовать перечислению WdMergeSubType [http://msdn.microsoft.com/en-us/library/bb237801.aspx](http://msdn.microsoft.com/en-us/library/bb237801.aspx).

## См. также

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
