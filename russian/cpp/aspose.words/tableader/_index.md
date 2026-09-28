---
title: "Aspose::Words::TabLeader enum"
linktitle: "TabLeader"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::TabLeader enum. Указывает тип линии‑заполнителя, отображаемой под символом табуляции в C++."
type: docs
weight: 121000
url: /ru/cpp/aspose.words/tableader/
---
## TabLeader enum


Указывает тип линий‑заполнителей, отображаемых под символом табуляции.

```cpp
enum class TabLeader
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| None | 0 | Линия‑заполнитель не отображается. |
| Точки | 1 | Линия‑заполнитель состоит из точек. |
| Тире | 2 | Линия‑заполнитель состоит из тире. |
| Линия | 3 | Линия‑заполнитель представляет собой одну линию. |
| Толстая | 4 | Линия‑заполнитель представляет собой одну толстую линию. |
| MiddleDot | 5 | Линия‑заполнитель состоит из средних точек. |


## Примеры



Показывает, как установить пользовательские табуляции для абзаца.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Если мы находимся в абзаце без табуляций в этой коллекции,
// курсор будет перемещаться на 36 пунктов каждый раз, когда мы нажимаем клавишу Tab в Microsoft Word.
ASSERT_EQ(0, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetEffectiveTabStops()->get_Length());

// Мы можем добавить пользовательские табуляции в Microsoft Word, если включим линейку через вкладку "View".
// Каждая единица на этой линейке соответствует двум стандартным табуляциям, что составляет 72 пункта.
// Мы можем добавить пользовательские табуляции программно, как показано.
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_TabStops();
tabStops->Add(72, Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dots);
tabStops->Add(216, Aspose::Words::TabAlignment::Center, Aspose::Words::TabLeader::Dashes);
tabStops->Add(360, Aspose::Words::TabAlignment::Right, Aspose::Words::TabLeader::Line);

// Мы можем увидеть эти табуляции в Microsoft Word, включив линейку через "View" -> "Show" -> "Ruler".
ASSERT_EQ(3, para->GetEffectiveTabStops()->get_Length());

// Любые добавленные нами символы табуляции будут использовать табуляции на линейке и могут,
// в зависимости от значения табуляционного лидера, оставлять линию между начальной и конечной точками табуляции.
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"\tTab 1\tTab 2\tTab 3"));

doc->Save(get_ArtifactsDir() + u"Paragraph.TabStops.docx");
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
