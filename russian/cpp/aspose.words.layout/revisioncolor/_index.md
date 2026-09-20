---
title: "Aspose::Words::Layout::RevisionColor enum"
linktitle: "RevisionColor"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Layout::RevisionColor enum. Позволяет указать цвет правок документа в C++."
type: docs
weight: 11000
url: /ru/cpp/aspose.words.layout/revisioncolor/
---
## RevisionColor enum


Позволяет задать цвет ревизий документа.

```cpp
enum class RevisionColor
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Авто | 0 | По умолчанию. |
| Черный | 1 | Представляет цвет 000000. |
| Синий | 2 | Представляет цвет 2e97d3. |
| BrightGreen | 3 | Представляет цвет 84a35b. |
| ClassicBlue | 4 | Представляет цвет 0000ff. |
| ClassicRed | 5 | Представляет цвет ff0000. |
| DarkBlue | 6 | Представляет цвет 376e96. |
| DarkRed | 7 | Представляет цвет 881824. |
| DarkYellow | 8 | Представляет цвет e09a2b. |
| Gray25 | 9 | Представляет цвет a0a3a9. |
| Gray50 | 10 | Представляет цвет 50565e. |
| Green | 11 | Представляет цвет 2c6234. |
| Pink | 12 | Представляет цвет ce338f. |
| Red | 13 | Представляет цвет b5082e. |
| Teal | 14 | Представляет цвет 1b9cab. |
| Turquoise | 15 | Представляет цвет 3eafc2. |
| Violet | 16 | Представляет цвет 633277. |
| White | 17 | Представляет цвет ffffff. |
| Yellow | 18 | Представляет цвет fad272. |
| LightPink | 19 | Представляет цвет fce6f4. |
| LightBlue | 20 | Представляет цвет e1f2fa. |
| LightYellow | 21 | Представляет цвет fef4de. |
| Светло-фиолетовый | 22 | Представляет цвет eadfef. |
| Светло-оранжевый | 23 | Представляет цвет fce3d0. |
| Светло-зелёный | 24 | Представляет цвет e9f8ce. |
| Серый | 25 | Представляет цвет efeded. |
| БезВыделения | 26 | Для выделения изменений ревизий цвет не используется. |
| ПоАвтору | 27 | Ревизии каждого автора получают собственный цвет для выделения из предопределённого набора контрастных цветов. |


## Примеры



Показывает, как изменить внешний вид правок в отрендеренном выходном документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте правку, затем измените цвет всех правок на зелёный.
builder->Writeln(u"This is not a revision.");
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"This is a revision.");
doc->StopTrackRevisions();
builder->Writeln(u"This is not a revision.");

// Удалите полосу, которая появляется слева от каждой исправленной строки.
doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::BrightGreen);
doc->get_LayoutOptions()->get_RevisionOptions()->set_ShowRevisionBars(false);
doc->get_LayoutOptions()->get_RevisionOptions()->set_RevisionBarsPosition(Aspose::Words::Drawing::HorizontalAlignment::Right);

doc->Save(get_ArtifactsDir() + u"Revision.LayoutOptionsRevisions.pdf");
```

## См. также

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
