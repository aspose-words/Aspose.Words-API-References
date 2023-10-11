---
title: Enum ShadowType
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.ShadowType перечисление. Указывает тип тени фигуры.
type: docs
weight: 1240
url: /ru/net/aspose.words.drawing/shadowtype/
---
## ShadowType enumeration

Указывает тип тени фигуры.

```csharp
public enum ShadowType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| ShadowMixed | `-2` | Ни один из предустановленных настроек теней. |
| Shadow1 | `1` | Первый тип тени. |
| Shadow10 | `10` | Десятый тип тени. |
| Shadow11 | `11` | Одиннадцатый тип тени. |
| Shadow12 | `12` | Двенадцатый тип тени. |
| Shadow13 | `13` | Тринадцатый тип тени. |
| Shadow14 | `14` | Четырнадцатый тип тени. |
| Shadow15 | `15` | Пятнадцатый тип тени. |
| Shadow16 | `16` | Шестнадцатый тип тени. |
| Shadow17 | `17` | Семнадцатый тип тени. |
| Shadow18 | `18` | Восемнадцатый тип тени. |
| Shadow19 | `19` | Девятнадцатый тип тени. |
| Shadow2 | `2` | Второй тип тени. |
| Shadow20 | `20` | Двадцатый тип тени. |
| Shadow21 | `21` | Двадцать первый тип тени. |
| Shadow22 | `22` | Двадцать второй тип тени. |
| Shadow23 | `23` | Двадцать третий тип тени. |
| Shadow24 | `24` | Двадцать четвёртый теневой тип. |
| Shadow25 | `25` | Двадцать пятый тип тени. |
| Shadow26 | `26` | Двадцать шестой тип тени. |
| Shadow27 | `27` | Двадцать седьмой теневой тип. |
| Shadow28 | `28` | Двадцать восьмой тип тени. |
| Shadow29 | `29` | Двадцать девятый тип тени. |
| Shadow3 | `3` | Третий тип тени. |
| Shadow30 | `30` | Тридцатый тип тени. |
| Shadow31 | `31` | Тридцать первый тип тени. |
| Shadow32 | `32` | Тридцать второй тип тени. |
| Shadow33 | `33` | Тридцать третий тип тени. |
| Shadow34 | `34` | Тридцать четвёртый теневой тип. |
| Shadow35 | `35` | Тридцать пятый тип тени. |
| Shadow36 | `36` | Тридцать шестой теневой тип. |
| Shadow37 | `37` | Тридцать седьмой теневой тип. |
| Shadow38 | `38` | Тридцать восьмой тип тени. |
| Shadow39 | `39` | Тридцать девятый тип тени. |
| Shadow4 | `4` | Четвертый тип тени. |
| Shadow40 | `40` | Сороковой тип тени. |
| Shadow41 | `41` | Сорок первый теневой тип. |
| Shadow42 | `42` | Сорок второй тип тени. |
| Shadow43 | `43` | Сорок третий теневой тип. |
| Shadow5 | `5` | Пятый тип тени. |
| Shadow6 | `6` | Шестой тип тени. |
| Shadow7 | `7` | Седьмой тип тени. |
| Shadow8 | `8` | Восьмой тип тени. |
| Shadow9 | `9` | Девятый тип тени. |

### Примечания

ShadowType — это не простой атрибут, а пресет, который задает сразу несколько атрибутов, формирующих внешний вид тени.

### Примеры

Показывает, как работать с форматированием тени для фигуры.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];

if (shape.ShadowFormat.Visible && shape.ShadowFormat.Type == ShadowType.Shadow2)                
    shape.ShadowFormat.Type = ShadowType.Shadow7;

if (shape.ShadowFormat.Type == ShadowType.ShadowMixed)            
    shape.ShadowFormat.Clear();
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)


