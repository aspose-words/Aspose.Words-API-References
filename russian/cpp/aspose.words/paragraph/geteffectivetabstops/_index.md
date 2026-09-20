---
title: "Aspose::Words::Paragraph::GetEffectiveTabStops method"
linktitle: "GetEffectiveTabStops"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Paragraph::GetEffectiveTabStops method. Возвращает массив всех табуляций, применённых к этому абзацу, включая применённые косвенно стилями или списками в C++."
type: docs
weight: 26000
url: /ru/cpp/aspose.words/paragraph/geteffectivetabstops/
---
## Paragraph::GetEffectiveTabStops method


Возвращает массив всех табуляций, применённых к этому абзацу, включая косвенно применённые стилями или списками.

```cpp
System::ArrayPtr<System::SharedPtr<Aspose::Words::TabStop>> Aspose::Words::Paragraph::GetEffectiveTabStops()
```


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

* Class [TabStop](../../tabstop/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
